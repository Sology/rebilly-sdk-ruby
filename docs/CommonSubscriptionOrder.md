# RebillySdk::CommonSubscriptionOrder

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [****](.md) | The order identifier string. | [optional] 
**order_type** | **String** | Specifies the type of order, a subscription or a one-time purchase.  | [optional] [default to &#x27;subscription-order&#x27;]
**billing_status** | **String** | The billing status of the most recent invoice.  It may help you determine if you should change the service status such as suspending the service.  | [optional] 
**website_id** | [****](.md) | The website identifier string. | [optional] 
**currency** | [****](.md) | The order&#x27;s currency. | [optional] 
**initial_invoice_id** | [****](.md) | The initial invoice identifier string. | [optional] 
**recent_invoice_id** | [****](.md) | Most recently issued invoice identifier string. It might not be &#x60;paid&#x60; yet. | [optional] 
**items** | [**Array&lt;CommonOrderItems&gt;**](CommonOrderItems.md) |  | [optional] 
**delivery_address** | [****](.md) | Order delivery address. | [optional] 
**billing_address** | [****](.md) | Order billing address. | [optional] 
**activation_time** | [****](.md) | Order activation time. | [optional] 
**void_time** | [****](.md) | Order void time. | [optional] 
**coupon_ids** | **Array&lt;String&gt;** | A list of coupons to redeem on the customer and restrict to this subscription. Read more about [coupons here](https://docs.rebilly.com/docs/dashboard/marketing/coupons-and-discounts/).  This parameter respects the following logic:  - When not passed then applied coupons will not be changed.  - When empty array passed then all applied coupon redemptions will be canceled.  - When list of coupons is passed then not applied yet coupons will be applied, already applied coupons will not change their state, applied coupons that are not presented in passed list will be canceled.  If list of applied coupons on pending order will be changed due to this param during update order,  Invoice for the order will be reissued.  | [optional] 
**po_number** | **String** | Purchase order number, will be displayed on the issued invoices. | [optional] 
**shipping** | [**Shipping**](Shipping.md) |  | [optional] 
**notes** | **String** | Notes for the customer which will be displayed on the order invoice. | [optional] 
**status** | **String** | The status of the subscription service. A subscription starts in the &#x60;pending&#x60; status, and will become &#x60;active&#x60; when the service period begins.  | [optional] 
**in_trial** | **BOOLEAN** | True if the subscription is currently in a trial period. | [optional] 
**trial** | [**CommonSubscriptionOrderTrial**](CommonSubscriptionOrderTrial.md) |  | [optional] 
**is_trial_only** | **BOOLEAN** | Whether a subscription ends after a trial period. Recurring settings are ignored if it&#x27;s &#x60;true&#x60;. | [optional] [default to false]
**invoice_time_shift** | [****](.md) | You can shift issue time and due time of invoices for this subscription. This setting overrides plan settings. To use plan settings, set &#x60;null&#x60;. To use multiple plans in one subscription they all must have the same billing period, this property allows to subscribe to different plans.  | [optional] 
**recurring_interval** | [**CommonSubscriptionOrderRecurringInterval**](CommonSubscriptionOrderRecurringInterval.md) |  | [optional] 
**autopay** | **BOOLEAN** | Autopay determines if a payment attempt will be automatic. | [optional] [default to true]
**start_time** | **DateTime** | Subscription start time.  When the value is sent as null, it will use the current time. This value can&#x27;t be in past more than one service period. | [optional] 
**end_time** | [****](.md) | Subscription end time. | [optional] 
**renewal_time** | **DateTime** | Subscription renewal time. | [optional] 
**rebill_number** | **Integer** | The current period number. | [optional] 
**line_items** | [****](.md) | Subscription line items which queue until the next renewal (or interim) invoice is issued for the subscription. | [optional] 
**line_item_subtotal** | [**CommonSubscriptionOrderLineItemSubtotal**](CommonSubscriptionOrderLineItemSubtotal.md) |  | [optional] 

