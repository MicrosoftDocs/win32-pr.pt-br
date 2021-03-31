---
description: Implementando IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implementando IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683dc2baf0496694943b7640d3f3ed521dc477a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172059"
---
# <a name="implementing-iwicdevelopraw"></a><span data-ttu-id="87d5d-103">Implementando IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="87d5d-103">Implementing IWICDevelopRaw</span></span>

## <a name="iwicdevelopraw"></a><span data-ttu-id="87d5d-104">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="87d5d-104">IWICDevelopRaw</span></span>

<span data-ttu-id="87d5d-105">A interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expõe opções de processamento específicas ao processamento bruto de imagens.</span><span class="sxs-lookup"><span data-stu-id="87d5d-105">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface exposes processing options specific to raw image processing.</span></span> <span data-ttu-id="87d5d-106">Todos os codecs brutos devem dar suporte à interface **IWICDevelopRaw** .</span><span class="sxs-lookup"><span data-stu-id="87d5d-106">All raw codecs must support the **IWICDevelopRaw** interface.</span></span> <span data-ttu-id="87d5d-107">Alguns codecs brutos podem não ser capazes de dar suporte a cada configuração exposta por essa interface, mas você deve dar suporte a todas as configurações que seu codec é capaz de executar.</span><span class="sxs-lookup"><span data-stu-id="87d5d-107">Some raw codecs may not be able to support every setting exposed by this interface, but you should support all the settings that your codec is capable of performing.</span></span> <span data-ttu-id="87d5d-108">No mínimo, todos os codecs brutos devem implementar os métodos [**setrotação**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) e [**setrenderingmode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .</span><span class="sxs-lookup"><span data-stu-id="87d5d-108">At minimum, every raw codec must implement the [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) methods.</span></span>

<span data-ttu-id="87d5d-109">Além disso, alguns métodos e interfaces opcionais para outros codecs são altamente recomendados para codecs brutos.</span><span class="sxs-lookup"><span data-stu-id="87d5d-109">Additionally, some methods and interfaces that are optional for other codecs are strongly recommended for raw codecs.</span></span> <span data-ttu-id="87d5d-110">Isso inclui os métodos [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) e [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) na classe de decodificador de nível de contêiner e a interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na classe de decodificação de nível de quadro.</span><span class="sxs-lookup"><span data-stu-id="87d5d-110">These include the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) and [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) methods on the container-level decoder class, and the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface on the frame-level decode class.</span></span>

<span data-ttu-id="87d5d-111">As configurações definidas usando os métodos [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) devem ser mantidas pelo codec de forma consistente com a maneira como outros metadados são persistidos, mas você nunca deve substituir as configurações originais "como capturadas".</span><span class="sxs-lookup"><span data-stu-id="87d5d-111">Settings set by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) methods should be persisted by the codec in a way that’s consistent with the way other metadata is persisted, but you should never overwrite the original "As Shot" settings.</span></span> <span data-ttu-id="87d5d-112">Ao persistir os metadados e implementar [**parameterset**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) e [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), você permite que aplicativos de processamento brutos recuperem e apliquem configurações de processamento entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="87d5d-112">By persisting the metadata and implementing [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) and [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), you enable raw processing applications to retrieve and apply processing settings across sessions.</span></span>

<span data-ttu-id="87d5d-113">A principal finalidade da interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) é permitir que os desenvolvedores de aplicativos criem uma interface do usuário para ajustar os parâmetros brutos que funcionarão da maneira mais consistente possível entre codecs diferentes.</span><span class="sxs-lookup"><span data-stu-id="87d5d-113">A main purpose of the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface is to enable application developers to build a user interface for adjusting raw parameters that will work as consistently as possible across different codecs.</span></span> <span data-ttu-id="87d5d-114">Suponha que um usuário final ajustará os parâmetros usando um controle deslizante, com seus valores mínimo e máximo mapeados para os intervalos mínimo e máximo para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="87d5d-114">Assume that an end user will adjust the parameters by using a slider control, with its minimum and maximum values mapped to the minimum and maximum ranges for the parameter.</span></span> <span data-ttu-id="87d5d-115">Para dar suporte a isso, você deve fazer todos os esforços para tratar todos os intervalos de parâmetro como lineares.</span><span class="sxs-lookup"><span data-stu-id="87d5d-115">To support this, you should make every effort to treat all parameter ranges as linear.</span></span> <span data-ttu-id="87d5d-116">Para garantir que os controles deslizantes não sejam excessivamente confidenciais, você também deve oferecer suporte a um intervalo maior possível para cada parâmetro, cobrindo pelo menos 50% do intervalo máximo possível.</span><span class="sxs-lookup"><span data-stu-id="87d5d-116">To ensure that the slider controls aren’t overly sensitive, you should also support as broad a range as possible for each parameter, covering at least 50 percent of the maximum possible range.</span></span> <span data-ttu-id="87d5d-117">Por exemplo, se o intervalo máximo possível de contraste for de cinza puro para puro preto e branco, com o valor padrão sendo mapeado para 0,0, o intervalo mínimo com suporte de um codec será de pelo menos meio entre o valor padrão e o cinza puro no nível inferior (– 1,0), para pelo menos meio entre o valor padrão e o preto puro e o branco no alto fim (+ 1,0).</span><span class="sxs-lookup"><span data-stu-id="87d5d-117">For example, if the maximum possible range of contrast is from pure gray to pure black and white, with the default value being mapped to 0.0, the minimum range supported by a codec would be from at least halfway between the default value and pure gray on the low end (–1.0), to at least halfway between the default value and pure black and white on the high end (+1.0).</span></span>


```C++
interface IWICDevelopRaw : IWICBitmapFrameDecode
{
   HRESULT QueryRawCapabilitiesInfo ( WICRawCapabilitiesInfo *pInfo );
   HRESULT LoadParameterSet ( WICRawParameterSet ParameterSet );
   HRESULT GetCurrentParameterSet ( IPropertyBag2 **ppCurrentParameterSet );
   HRESULT SetExposureCompensation ( double ev );
   HRESULT GetExposureCompensation ( double *pEV );
   HRESULT SetWhitePointRGB ( UINT Red, UINT Green, UINT Blue );
   HRESULT GetWhitePointRGB ( UINT *pRed, UINT *pGreen, UINT *pBlue );
   HRESULT SetNamedWhitePoint ( WICNamedWhitePoint WhitePoint );
   HRESULT GetNamedWhitePoint ( WICNamedWhitePoint *pWhitePoint );
   HRESULT SetWhitePointKelvin ( UINT WhitePointKelvin );
   HRESULT GetWhitePointKelvin ( UINT *pWhitePointKelvin );
   HRESULT GetKelvinRangeInfo ( UINT *pMinKelvinTemp,
               UINT *pMaxKelvinTemp,
               UINT *pKelvinTempStepValue );
   HRESULT SetContrast ( double Contrast );
   HRESULT GetContrast ( double *pContrast );
   HRESULT SetGamma ( double Gamma );
   HRESULT GetGamma ( double *pGamma );
   HRESULT SetSharpness ( double Sharpness );
   HRESULT GetSharpness ( double *pSharpness );
   HRESULT SetSaturation ( double Saturation );
   HRESULT GetSaturation ( double *pSaturation );
   HRESULT SetTint ( double Tint );
   HRESULT GetTint ( double *pTint );
   HRESULT SetNoiseReduction ( double NoiseReduction );
   HRESULT GetNoiseReduction ( double *pNoiseReduction );
   HRESULT SetDestinationColorContext (const IWICColorContext *pColorContext );
   HRESULT SetToneCurve ( UINT cbToneCurveSize,
               const WICRawToneCurve *pToneCurve );
   HRESULT GetToneCurve ( UINT cbToneCurveBufferSize,
               WICRawToneCurve *pToneCurve,
               UINT *pcbActualToneCurveBufferSize );
   HRESULT SetRotation ( double Rotation );
   HRESULT GetRotation ( double *pRotation );
   HRESULT SetRenderMode ( WICRawRenderMode RenderMode );
   HRESULT GetRenderMode ( WICRawRenderMode *pRenderMode ); 
   HRESULT SetNotificationCallback ( IWICDevelopRawNotificationCallback 
               *pCallback );
}
```



-   [<span data-ttu-id="87d5d-118">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="87d5d-118">QueryRawCapabilitiesInfo</span></span>](#queryrawcapabilitiesinfo)
-   [<span data-ttu-id="87d5d-119">Parameterset</span><span class="sxs-lookup"><span data-stu-id="87d5d-119">LoadParameterSet</span></span>](#loadparameterset)
-   [<span data-ttu-id="87d5d-120">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d5d-120">GetCurrentParameterSet</span></span>](#getcurrentparameterset)
-   [<span data-ttu-id="87d5d-121">Definir/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="87d5d-121">Set/GetExposureCompensation</span></span>](#setgetexposurecompensation)
-   [<span data-ttu-id="87d5d-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="87d5d-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [<span data-ttu-id="87d5d-123">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="87d5d-123">Set/GetContrast</span></span>](#setgetcontrast)
-   [<span data-ttu-id="87d5d-124">Set/getgama</span><span class="sxs-lookup"><span data-stu-id="87d5d-124">Set/GetGamma</span></span>](#setgetgamma)
-   [<span data-ttu-id="87d5d-125">Set/getnitidez</span><span class="sxs-lookup"><span data-stu-id="87d5d-125">Set/GetSharpness</span></span>](#setgetsharpness)
-   [<span data-ttu-id="87d5d-126">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="87d5d-126">Set/GetSaturation</span></span>](#setgetsaturation)
-   [<span data-ttu-id="87d5d-127">Definir/getmatiz</span><span class="sxs-lookup"><span data-stu-id="87d5d-127">Set/GetTint</span></span>](#setgettint)
-   [<span data-ttu-id="87d5d-128">Definir/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="87d5d-128">Set/GetNoiseReduction</span></span>](#setgetnoisereduction)
-   [<span data-ttu-id="87d5d-129">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="87d5d-129">SetDestinationColorContext</span></span>](#setdestinationcolorcontext)
-   [<span data-ttu-id="87d5d-130">Definir/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="87d5d-130">Set/GetToneCurve</span></span>](#setgettonecurve)
-   [<span data-ttu-id="87d5d-131">Definir/getrotation</span><span class="sxs-lookup"><span data-stu-id="87d5d-131">Set/GetRotation</span></span>](#setgetrotation)
-   [<span data-ttu-id="87d5d-132">Set/getrenderingmode</span><span class="sxs-lookup"><span data-stu-id="87d5d-132">Set/GetRenderMode</span></span>](#setgetrendermode)
-   [<span data-ttu-id="87d5d-133">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="87d5d-133">SetNotificationCallback</span></span>](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a><span data-ttu-id="87d5d-134">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="87d5d-134">QueryRawCapabilitiesInfo</span></span>

<span data-ttu-id="87d5d-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) retorna o conjunto de recursos com suporte para esse arquivo bruto.</span><span class="sxs-lookup"><span data-stu-id="87d5d-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) returns the set of supported capabilities for this raw file.</span></span> <span data-ttu-id="87d5d-136">A estrutura [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="87d5d-136">The [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) structure is defined as follows:</span></span>


```C++
struct WICRawCapabilitiesInfo
{
   UINT cbSize;
   UINT CodecMajorVersion;
   UINT CodecMinorVersion;
   WICRawCapabilities ExposureCompensationSupport;
   WICRawCapabilities ContrastSupport;
   WICRawCapabilities RGBWhitePointSupport;
   WICRawCapabilities NamedWhitePointSupport;
   UINT NamedWhitePointSupportMask;
   WICRawCapabilities KelvinWhitePointSupport;
   WICRawCapabilities GammaSupport;
   WICRawCapabilities TintSupport;
   WICRawCapabilities SaturationSupport;
   WICRawCapabilities SharpnessSupport;
   WICRawCapabilities NoiseReductionSupport;
   WICRawCapabilities DestinationColorProfileSupport;
   WICRawCapabilities ToneCurveSupport;
   WICRawRotationCapabilities RotationSupport;              
}
```



<span data-ttu-id="87d5d-137">A enumeração [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) usada nesta estrutura é definida como:</span><span class="sxs-lookup"><span data-stu-id="87d5d-137">The [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) enumeration used in this structure is defined as:</span></span>


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



<span data-ttu-id="87d5d-138">O campo final é uma enumeração [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , definida como:</span><span class="sxs-lookup"><span data-stu-id="87d5d-138">The final field is a [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) enumeration, defined as:</span></span>


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a><span data-ttu-id="87d5d-139">Parameterset</span><span class="sxs-lookup"><span data-stu-id="87d5d-139">LoadParameterSet</span></span>

<span data-ttu-id="87d5d-140">O [**parameterset**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) permite que o usuário especifique se deseja usar as configurações de captura, usar configurações ajustadas pelo usuário ou solicitar que o decodificador corrija a imagem automaticamente.</span><span class="sxs-lookup"><span data-stu-id="87d5d-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) enables the user to specify whether to use As Shot settings, use user-adjusted settings, or request the decoder to auto-correct the image.</span></span>


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a><span data-ttu-id="87d5d-141">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d5d-141">GetCurrentParameterSet</span></span>

<span data-ttu-id="87d5d-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) retorna um **IPropertyBag2** com o conjunto de parâmetros atual.</span><span class="sxs-lookup"><span data-stu-id="87d5d-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) returns an **IPropertyBag2** with the current parameter set.</span></span> <span data-ttu-id="87d5d-143">Em seguida, o chamador pode passar esse parâmetro definido para o codificador a ser usado como as opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="87d5d-143">The caller can then pass this parameter set to the encoder to use as the encoder options.</span></span>

### <a name="setgetexposurecompensation"></a><span data-ttu-id="87d5d-144">Definir/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="87d5d-144">Set/GetExposureCompensation</span></span>

<span data-ttu-id="87d5d-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) e [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicam a compensação de exposição a ser aplicada à saída final.</span><span class="sxs-lookup"><span data-stu-id="87d5d-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) and [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicate the exposure compensation to apply to the final output.</span></span> <span data-ttu-id="87d5d-146">O intervalo válido para EV é de – 5,0 a + 5,0 paradas.</span><span class="sxs-lookup"><span data-stu-id="87d5d-146">The valid range for EV is –5.0 to +5.0 stops.</span></span>

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a><span data-ttu-id="87d5d-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="87d5d-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>

<span data-ttu-id="87d5d-148">Todas essas funções fornecem maneiras de obter e definir o ponto branco, como um valor RGB, um valor nomeado predefinido ou como um valor de Kelvin.</span><span class="sxs-lookup"><span data-stu-id="87d5d-148">These functions all provide ways to get and set the white point, either as an RGB value, a preset named value, or as a Kelvin value.</span></span> <span data-ttu-id="87d5d-149">O intervalo aceitável para Kelvin é 1.500 – 30.000.</span><span class="sxs-lookup"><span data-stu-id="87d5d-149">The acceptable range for Kelvin is 1,500 – 30,000.</span></span>

### <a name="setgetcontrast"></a><span data-ttu-id="87d5d-150">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="87d5d-150">Set/GetContrast</span></span>

<span data-ttu-id="87d5d-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) e [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicam a quantidade de contraste a ser aplicada à saída.</span><span class="sxs-lookup"><span data-stu-id="87d5d-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) and [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicate the amount of contrast to apply to the output.</span></span> <span data-ttu-id="87d5d-152">O intervalo válido para especificar o contraste é – 1,0 a + 1,0, com o contraste padrão sendo 0,0.</span><span class="sxs-lookup"><span data-stu-id="87d5d-152">The valid range to specify contrast is –1.0 to +1.0, with the default contrast being 0.0.</span></span>

### <a name="setgetgamma"></a><span data-ttu-id="87d5d-153">Set/getgama</span><span class="sxs-lookup"><span data-stu-id="87d5d-153">Set/GetGamma</span></span>

<span data-ttu-id="87d5d-154">[**Getgama**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) e [**setgama**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicam o gama a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="87d5d-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) and [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicate the Gamma to apply.</span></span> <span data-ttu-id="87d5d-155">O intervalo válido para gama é de 0,2 a 5,0, com 1,0 sendo o padrão.</span><span class="sxs-lookup"><span data-stu-id="87d5d-155">The valid range for Gamma is 0.2 to 5.0, with 1.0 being the default.</span></span> <span data-ttu-id="87d5d-156">Normalmente, o gama é implementado usando a função de energia gama tradicional (uma função de energia linear com lucro de Unity).</span><span class="sxs-lookup"><span data-stu-id="87d5d-156">Gamma typically is implemented using the traditional Gamma power function (a linear power function with unity gain).</span></span> <span data-ttu-id="87d5d-157">O brilho aumenta com o aumento de gama e diminui conforme o gama se aproxima de zero.</span><span class="sxs-lookup"><span data-stu-id="87d5d-157">Brightness is increased with increasing Gamma and decreased as Gamma approaches zero.</span></span> <span data-ttu-id="87d5d-158">(Observe que o valor mínimo é diferente de zero, porque zero resultaria em um erro de divisão por zero nos cálculos de gama tradicionais.</span><span class="sxs-lookup"><span data-stu-id="87d5d-158">(Note that the minimum value is non-zero, because zero would result in a divide-by-zero error in traditional Gamma calculations.</span></span> <span data-ttu-id="87d5d-159">O limite mínimo lógico é 1/máx. é por isso que o mínimo é 0,2.)</span><span class="sxs-lookup"><span data-stu-id="87d5d-159">The logical minimum limit is 1/max, which is why the minimum is 0.2.)</span></span>

### <a name="setgetsharpness"></a><span data-ttu-id="87d5d-160">Set/getnitidez</span><span class="sxs-lookup"><span data-stu-id="87d5d-160">Set/GetSharpness</span></span>

<span data-ttu-id="87d5d-161">[**Getnitidez**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) e [**setnitidez**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicam a quantidade de nitidez a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="87d5d-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) and [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicate the amount of sharpening to apply.</span></span> <span data-ttu-id="87d5d-162">O intervalo válido é de – 1,0 a + 1,0, com 0,0 sendo a quantidade padrão de nitidez e – 1,0 indicando nenhuma nitidez.</span><span class="sxs-lookup"><span data-stu-id="87d5d-162">The valid range is –1.0 to +1.0, with 0.0 being the default amount of sharpening, and –1.0 indicating no sharpening at all.</span></span>

### <a name="setgetsaturation"></a><span data-ttu-id="87d5d-163">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="87d5d-163">Set/GetSaturation</span></span>

<span data-ttu-id="87d5d-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) e [**setsaturação**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicam a quantidade de saturação a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="87d5d-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) and [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicate the amount of saturation to apply.</span></span> <span data-ttu-id="87d5d-165">O intervalo válido para especificar a saturação é de – 1,0 a + 1,0, com 0,0 sendo saturação normal, – 1,0 representando a dessaturação completa e + 1,0, representando a saturação completa.</span><span class="sxs-lookup"><span data-stu-id="87d5d-165">The valid range to specify saturation is –1.0 to +1.0, with 0.0 being normal saturation, –1.0 representing complete desaturation, and +1.0 representing full saturation.</span></span>

### <a name="setgettint"></a><span data-ttu-id="87d5d-166">Definir/getmatiz</span><span class="sxs-lookup"><span data-stu-id="87d5d-166">Set/GetTint</span></span>

<span data-ttu-id="87d5d-167">[**Getmatiz**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) e [**settonalidade**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicam a tonalidade a ser aplicada, em uma inclinação verde/magenta.</span><span class="sxs-lookup"><span data-stu-id="87d5d-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) and [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicate the tint to apply, on a green/magenta bias.</span></span> <span data-ttu-id="87d5d-168">O intervalo válido é de – 1,0 a + 1,0, sendo que verde está no lado negativo da escala e magenta no positivo.</span><span class="sxs-lookup"><span data-stu-id="87d5d-168">The valid range is –1.0 to +1.0, with green being on the negative side of the scale and magenta on the positive.</span></span> <span data-ttu-id="87d5d-169">A escala de tonalidade é definida como ortogonal à temperatura de cor.</span><span class="sxs-lookup"><span data-stu-id="87d5d-169">The tint scale is defined as orthogonal to color temperature.</span></span>

### <a name="setgetnoisereduction"></a><span data-ttu-id="87d5d-170">Definir/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="87d5d-170">Set/GetNoiseReduction</span></span>

<span data-ttu-id="87d5d-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) e [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicam a quantidade de redução de ruído a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="87d5d-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) and [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicate the amount of noise reduction to apply.</span></span> <span data-ttu-id="87d5d-172">O intervalo válido para é de – 1,0 a + 1,0, com 0,0 indicando a quantidade padrão de redução de ruído, – 1,0 indicando nenhuma redução de ruído e + 1,0, indicando a redução máxima de ruído.</span><span class="sxs-lookup"><span data-stu-id="87d5d-172">The valid range to is –1.0 to +1.0, with 0.0 indicating the default amount of noise reduction, –1.0 indicating no noise reduction and +1.0 indicating maximum noise reduction.</span></span>

### <a name="setdestinationcolorcontext"></a><span data-ttu-id="87d5d-173">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="87d5d-173">SetDestinationColorContext</span></span>

<span data-ttu-id="87d5d-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) especifica o perfil de cor a ser aplicado à imagem.</span><span class="sxs-lookup"><span data-stu-id="87d5d-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifies the color profile to apply to the image.</span></span> <span data-ttu-id="87d5d-175">Você pode chamar [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) para recuperar o perfil de cor atual.</span><span class="sxs-lookup"><span data-stu-id="87d5d-175">You can call [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) to retrieve the current color profile.</span></span>

### <a name="setgettonecurve"></a><span data-ttu-id="87d5d-176">Definir/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="87d5d-176">Set/GetToneCurve</span></span>

<span data-ttu-id="87d5d-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) e [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) especifique a curva de Tom a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="87d5d-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) and [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specify the tone curve to apply.</span></span> <span data-ttu-id="87d5d-178">Assuma a interpolação linear entre pontos.</span><span class="sxs-lookup"><span data-stu-id="87d5d-178">Assume linear interpolation between points.</span></span> <span data-ttu-id="87d5d-179">O **pToneCurve** é uma estrutura [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) , que contém uma matriz de estruturas [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) e uma contagem do número de pontos na matriz.</span><span class="sxs-lookup"><span data-stu-id="87d5d-179">The **pToneCurve** is a [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) structure, which contains an array of [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) structures, and a count of the number of points in the array.</span></span>


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



<span data-ttu-id="87d5d-180">Um [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contém um valor de entrada e um valor de saída.</span><span class="sxs-lookup"><span data-stu-id="87d5d-180">A [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contains an input value and an output value.</span></span>


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



<span data-ttu-id="87d5d-181">Quando o chamador passa **NULL** no parâmetro *pToneCurve* , você deve passar de volta o tamanho necessário para o [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) no parâmetro *pcbActualToneCurveBufferSize* .</span><span class="sxs-lookup"><span data-stu-id="87d5d-181">When the caller passes **NULL** in the *pToneCurve* parameter, you should pass back the required size for the [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) in the *pcbActualToneCurveBufferSize* parameter.</span></span>

### <a name="setgetrotation"></a><span data-ttu-id="87d5d-182">Definir/getrotation</span><span class="sxs-lookup"><span data-stu-id="87d5d-182">Set/GetRotation</span></span>

<span data-ttu-id="87d5d-183">[**Getrotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) e [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicam o grau de rotação a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="87d5d-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) and [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicate the degree of rotation to apply.</span></span> <span data-ttu-id="87d5d-184">Uma rotação de 90,0 especificaria uma rotação de 90 graus no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="87d5d-184">A rotation of 90.0 would specify a rotation of 90 degrees clockwise.</span></span> <span data-ttu-id="87d5d-185">(A diferença entre usar **SetRotation** e definir a rotação usando o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) é que o ângulo de rotação definido usando **SetRotation** deve ser persistido pelo codec, ao passo que definir a rotação por meio de **CopyPixels** apenas gira a imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="87d5d-185">(The difference between using **SetRotation** and setting rotation using the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method is that the rotation angle set using **SetRotation** should be persisted by the codec, while setting rotation through **CopyPixels** only rotates the image in memory.</span></span>

### <a name="setgetrendermode"></a><span data-ttu-id="87d5d-186">Set/getrenderingmode</span><span class="sxs-lookup"><span data-stu-id="87d5d-186">Set/GetRenderMode</span></span>

<span data-ttu-id="87d5d-187">[**Getprocessmode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) e [**setrenderingmode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicam o nível de qualidade exigido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="87d5d-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicate the quality level of output the caller requires.</span></span> <span data-ttu-id="87d5d-188">Quando um usuário estiver ajustando parâmetros, o aplicativo deverá exibir uma aproximação muito rápida da aparência da imagem real se as alterações forem aplicadas.</span><span class="sxs-lookup"><span data-stu-id="87d5d-188">When a user is adjusting parameters, the application should display a very fast approximation of what the actual image will look like if the changes are applied.</span></span> <span data-ttu-id="87d5d-189">Para essa finalidade, a imagem geralmente é exibida na resolução da tela ou menos, em vez da resolução de imagem real, para fornecer comentários imediatos ao usuário.</span><span class="sxs-lookup"><span data-stu-id="87d5d-189">For this purpose, the image is usually displayed at screen resolution or less, rather than the actual image resolution, to provide immediate feedback to the user.</span></span> <span data-ttu-id="87d5d-190">Isso ocorre quando um aplicativo solicita qualidade de modo de rascunho, então isso deve ser muito rápido.</span><span class="sxs-lookup"><span data-stu-id="87d5d-190">This is when an application would request Draft Mode quality, so this should be very fast.</span></span> <span data-ttu-id="87d5d-191">Quando o usuário fez todas as alterações, as exibiu no modo de rascunho e decidiu decodificar a imagem completa com as configurações atuais, o aplicativo solicita uma decodificação de melhor qualidade.</span><span class="sxs-lookup"><span data-stu-id="87d5d-191">When the user has made all changes, previewed them in draft mode, and decided to decode the full image with the current settings, the application requests a Best Quality decode.</span></span> <span data-ttu-id="87d5d-192">Normalmente, isso também é solicitado para impressão.</span><span class="sxs-lookup"><span data-stu-id="87d5d-192">This is usually also requested for printing.</span></span> <span data-ttu-id="87d5d-193">Onde é necessária uma compensação razoável entre a velocidade de uma qualidade, o aplicativo solicita a qualidade normal.</span><span class="sxs-lookup"><span data-stu-id="87d5d-193">Where a reasonable tradeoff between speed an quality is required, the application requests Normal Quality.</span></span>


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a><span data-ttu-id="87d5d-194">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="87d5d-194">SetNotificationCallback</span></span>

<span data-ttu-id="87d5d-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registra uma função de retorno de chamada para o decodificador chamar quando qualquer um dos parâmetros de processamento brutos for alterado.</span><span class="sxs-lookup"><span data-stu-id="87d5d-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registers a callback function for the decoder to call when any of the Raw processing parameters change.</span></span> <span data-ttu-id="87d5d-196">A assinatura para [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) tem apenas um método, chamado [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span><span class="sxs-lookup"><span data-stu-id="87d5d-196">The signature for the [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) has only one method, called [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span></span> <span data-ttu-id="87d5d-197">**Notify** tem um único parâmetro, que é uma máscara que indica qual dos parâmetros de processamento brutos foram alterados.</span><span class="sxs-lookup"><span data-stu-id="87d5d-197">**Notify** has a single parameter, which is a mask that indicates which of the raw processing parameters have changed.</span></span>


```C++
HRESULT Notify ( UINT NotificationMask );
```



<span data-ttu-id="87d5d-198">Uma operação ou é executada nos valores a seguir para o NotificationMask.</span><span class="sxs-lookup"><span data-stu-id="87d5d-198">An OR operation is performed on the following values for the NotificationMask.</span></span>


```C++
WICRawChangeNotification_ExposureCompensation
WICRawChangeNotification_NamedWhitePoint
WICRawChangeNotification_KelvinWhitePoint
WICRawChangeNotification_RGBWhitePoint
WICRawChangeNotification_Contrast
WICRawChangeNotification_Gamma
WICRawChangeNotification_Sharpness
WICRawChangeNotification_Saturation
WICRawChangeNotification_Tint
WICRawChangeNotification_NoiseReduction
WICRawChangeNotification_DestinationColorContext
WICRawChangeNotification_ToneCurve
WICRawChangeNotification_Rotation
WICRawChangeNotification_RenderMode
```



## <a name="related-topics"></a><span data-ttu-id="87d5d-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87d5d-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="87d5d-200">**Referência**</span><span class="sxs-lookup"><span data-stu-id="87d5d-200">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="87d5d-201">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="87d5d-201">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

<span data-ttu-id="87d5d-202">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="87d5d-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="87d5d-203">Implementando IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="87d5d-203">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="87d5d-204">Implementando um codificador de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="87d5d-204">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="87d5d-205">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="87d5d-205">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="87d5d-206">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="87d5d-206">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



