# unity-android-sdk
Rekmob unity plugin for android.

[Home](https://github.com/rekmob/unity-android-sdk/wiki)

**Integrating the Rekmob SDK in Unity projects for Android** (English)

- [Android Banner Integration](https://github.com/rekmob/unity-android-sdk/wiki/Android-Banner-Integration)


**Unity projelerinde Android için Rekmob entegrasyonu** (Türkçe)

- [Android Banner Entegrasyonu](https://github.com/rekmob/unity-android-sdk/wiki/Android-Banner-Integration)

## API Documentation

`Plugins/RekmobAndroid/RekmobAndroid.cs` contains following methods:

```
/*
	Shows banner ad for given ad unit Id and places the ad defined location with RekmobAdPlacement instance.
	RekmobAdPlacement is an enum with values:
	TopLeft,
	TopCenter,
	TopRight,
	Centered,
	BottomLeft,
	BottomCenter,
	BottomRight
*/	
public static void createBanner( string adUnitId, RekmobAdPlacement position )

// Hides/shows the ad banner
public static void hideBanner( bool shouldHide )

// Sets the search keywords for the banner
public static void setBannerKeywords( string keywords )

// Destroys the banner and removes it from view
public static void destroyBanner()

// Starts loading an interstitial ad
public static void requestInterstitalAd( string adUnitId )

// If an interstitial ad is loaded this will take over the screen and show the ad
public static void showInterstitalAd()


````

You can find following methods in `Plugins/RekmobAndroid/RekmobAndroidManager.cs` 

```
// Fired when a new banner ad is loaded
public void onAdLoaded( string empty )

// Fired when a banner ad fails to load
public void onAdFailed( string empty )

// Fired when a banner ad is clicked
public void onAdClicked( string empty )

// Fired when a banner ad expands to encompass a greater portion of the screen
public void onAdExpanded( string empty )

// Fired when a banner ad collapses back to its initial size
public void onAdCollapsed( string empty )



// Fired when an interstitial ad is loaded
public void onInterstitialLoaded( string empty )

// Fired when an interstitial ad fails to load
public void onInterstitialFailed( string empty )

// Fired when an interstitial ad is displayed
public void onInterstitialShown( string empty )

// Fired when an interstitial ad is clicked
public void onInterstitialClicked( string empty )

// Fired when an interstitial ad is dismissed
public void onInterstitialDismissed( string empty )

```

You can find examples how this api can be used. `Plugins/RekmobAndroid/example/RekmobUIManager.cs`


> [![Mobile Ad Network](https://rekmob.s3.amazonaws.com/img/logo.png)](https://www.rekmob.com)
