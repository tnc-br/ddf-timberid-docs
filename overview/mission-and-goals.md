# ✨ Mission and Goals

### The long term goal of the Digitais da Floresta platform is to

## <mark style="color:blue;">Increase timber supply chain transparency</mark> in the <mark style="color:green;">Brazilian Amazon</mark> using <mark style="color:yellow;">data-driven insights</mark> to <mark style="color:red;">support rain-forest preservation</mark>



TimberID provides a key component of this platform by centralizing timber identification and analysis.

#### **Components**

<div data-full-width="false">

<figure><img src="../.gitbook/assets/arch.png" alt=""><figcaption><p>Component diagram for TimberID</p></figcaption></figure>

</div>

TimberID has three high level components:

1. A Web UI is used to track and store both reference and untrusted samples (Isotope Tracking frontend)
2. A Variational Inference tensorflow ML model that uses these timber reference samples to create a ground truth isoscape (ML Isoscape Model)
3. A backend analytics engine that runs on seized timber to perform origin verification and other analysis. This layer also provides an Earth Engine based API for further research. (Insights and Analytics)

The fourth component shown above, the Transparency Application is a future part of the Digitais da Floresta platform that uses the generated insights from TimberID (along with insights from other applications) to create actionable insights for target users.

The ultimate goal is for consumers to visit a portal that gives them actionable information on where to buy sustainable wood products. Or similarly, how to choose wood sustainably for products they buy. Retailers may use this portal to understand which suppliers ensure legal sustainable timber products. And policy makers can understand the broad picture and how they may act to impact the overall supplier ecosystem.

