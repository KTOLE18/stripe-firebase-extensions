<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@stripe/firestore-stripe-payments](./firestore-stripe-payments.md)

## firestore-stripe-payments package

## Classes

|  Class | Description |
|  --- | --- |
|  [StripePayments](./firestore-stripe-payments.stripepayments.md) | Holds the configuration and other state information of the SDK. An instance of this class must be passed to almost all the other APIs of this library. Do not directly call the constructor. Use the [getStripePayments()](./firestore-stripe-payments.getstripepayments.md) function to obtain an instance. |
|  [StripePaymentsError](./firestore-stripe-payments.stripepaymentserror.md) | An error thrown by this SDK. |

## Functions

|  Function | Description |
|  --- | --- |
|  [createCheckoutSession(payments, params, options)](./firestore-stripe-payments.createcheckoutsession.md) | Creates a new Stripe checkout session with the given parameters. Returned session contains a session ID and a session URL that can be used to redirect the user to complete the checkout. User must be currently signed in with Firebase Auth to call this API. If a timeout occurs while waiting for the session to be created and acknowledged by Stripe, rejects with a <code>deadline-exceeded</code> error. Default timeout duration is [CREATE\_SESSION\_TIMEOUT\_MILLIS](./firestore-stripe-payments.create_session_timeout_millis.md)<!-- -->. |
|  [getCurrentUserSubscription(payments, subscriptionId)](./firestore-stripe-payments.getcurrentusersubscription.md) | Retrieves an existing Stripe subscription for the currently signed in user from the database. |
|  [getCurrentUserSubscriptions(payments, options)](./firestore-stripe-payments.getcurrentusersubscriptions.md) | Retrieves existing Stripe subscriptions for the currently signed in user from the database. |
|  [getPrice(payments, productId, priceId)](./firestore-stripe-payments.getprice.md) | Retrieves a Stripe price from the database. |
|  [getPrices(payments, productId)](./firestore-stripe-payments.getprices.md) | Retrieves all Stripe prices associated with the specified product. |
|  [getProduct(payments, productId, options)](./firestore-stripe-payments.getproduct.md) | Retrieves a Stripe product from the database. |
|  [getProducts(payments, options)](./firestore-stripe-payments.getproducts.md) | Retrieves a Stripe product from the database. |
|  [getStripePayments(app, options)](./firestore-stripe-payments.getstripepayments.md) | Serves as the main entry point to this library. Initializes the client SDK, and returns a handle object that can be passed into other APIs. |
|  [onCurrentUserSubscriptionUpdate(payments, onUpdate, onError)](./firestore-stripe-payments.oncurrentusersubscriptionupdate.md) | Registers a listener to receive subscription update events for the currently signed in user. If the user is not signed in throws an <code>unauthenticated</code> error, and no listener is registered.<!-- -->Upon successful registration, the <code>onUpdate</code> callback will fire once with the current state of all the subscriptions. From then onwards, each update to a subscription will fire the <code>onUpdate</code> callback with the latest state of the subscriptions. |

## Interfaces

|  Interface | Description |
|  --- | --- |
|  [CommonLineItemParams](./firestore-stripe-payments.commonlineitemparams.md) | Parameters common across all line item types. |
|  [CommonSessionCreateParams](./firestore-stripe-payments.commonsessioncreateparams.md) | Parameters common across all session types. |
|  [CreateCheckoutSessionOptions](./firestore-stripe-payments.createcheckoutsessionoptions.md) | Optional settings for the [createCheckoutSession()](./firestore-stripe-payments.createcheckoutsession.md) function. |
|  [GetProductOptions](./firestore-stripe-payments.getproductoptions.md) | Optional parameters for the [getProduct()](./firestore-stripe-payments.getproduct.md) function. |
|  [GetProductsOptions](./firestore-stripe-payments.getproductsoptions.md) | Optional parameters for the [getProducts()](./firestore-stripe-payments.getproducts.md) function. |
|  [GetSubscriptionsOptions](./firestore-stripe-payments.getsubscriptionsoptions.md) | Optional parameters for the [getCurrentUserSubscriptions()](./firestore-stripe-payments.getcurrentusersubscriptions.md) function. |
|  [LineItem](./firestore-stripe-payments.lineitem.md) | Interface of a Stripe line item associated with a checkout session. A line item represents an individual item purchased using the session. |
|  [LineItemSessionCreateParams](./firestore-stripe-payments.lineitemsessioncreateparams.md) | Parameters for createing a session with one or more line items. |
|  [Price](./firestore-stripe-payments.price.md) | Interface of a Stripe Price object stored in the app database. |
|  [PriceIdLineItemParams](./firestore-stripe-payments.priceidlineitemparams.md) | Parameters for createing a line item with a Stripe price ID. |
|  [PriceIdSessionCreateParams](./firestore-stripe-payments.priceidsessioncreateparams.md) | Parameters for createing a session with a Stripe price ID. |
|  [Product](./firestore-stripe-payments.product.md) | Interface of a Stripe Product stored in the app database. |
|  [Session](./firestore-stripe-payments.session.md) | Interface of Stripe checkout session. |
|  [StripePaymentsOptions](./firestore-stripe-payments.stripepaymentsoptions.md) | Configuration options that indicate how the Stripe payments extension has been set up. |
|  [Subscription](./firestore-stripe-payments.subscription.md) | Interface of a Stripe Subscription stored in the app database. |
|  [SubscriptionSnapshot](./firestore-stripe-payments.subscriptionsnapshot.md) | Represents the current state of a set of subscriptions owned by a user. |

## Variables

|  Variable | Description |
|  --- | --- |
|  [CREATE\_SESSION\_TIMEOUT\_MILLIS](./firestore-stripe-payments.create_session_timeout_millis.md) |  |

## Type Aliases

|  Type Alias | Description |
|  --- | --- |
|  [LineItemParams](./firestore-stripe-payments.lineitemparams.md) | Parameters for creating a new line item. |
|  [PaymentMethodType](./firestore-stripe-payments.paymentmethodtype.md) | Supported payment methods. |
|  [SessionCreateParams](./firestore-stripe-payments.sessioncreateparams.md) | Parameters for creating a new session. |
|  [StripePaymentsErrorCode](./firestore-stripe-payments.stripepaymentserrorcode.md) | Union of possible error codes. |
|  [SubscriptionChangeType](./firestore-stripe-payments.subscriptionchangetype.md) | Different types of changes that may occur on a subscription object. |
|  [SubscriptionStatus](./firestore-stripe-payments.subscriptionstatus.md) | Possible states a subscription can be in. |
|  [WhereFilter](./firestore-stripe-payments.wherefilter.md) | A filter constraint that can be applied to database queries. Consists of a field name (in Firestore dotted notation), a Firestore filter operator, and a value. |

