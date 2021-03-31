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
# <a name="implementing-iwicdevelopraw"></a>Implementando IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

A interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expõe opções de processamento específicas ao processamento bruto de imagens. Todos os codecs brutos devem dar suporte à interface **IWICDevelopRaw** . Alguns codecs brutos podem não ser capazes de dar suporte a cada configuração exposta por essa interface, mas você deve dar suporte a todas as configurações que seu codec é capaz de executar. No mínimo, todos os codecs brutos devem implementar os métodos [**setrotação**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) e [**setrenderingmode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .

Além disso, alguns métodos e interfaces opcionais para outros codecs são altamente recomendados para codecs brutos. Isso inclui os métodos [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) e [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) na classe de decodificador de nível de contêiner e a interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na classe de decodificação de nível de quadro.

As configurações definidas usando os métodos [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) devem ser mantidas pelo codec de forma consistente com a maneira como outros metadados são persistidos, mas você nunca deve substituir as configurações originais "como capturadas". Ao persistir os metadados e implementar [**parameterset**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) e [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), você permite que aplicativos de processamento brutos recuperem e apliquem configurações de processamento entre as sessões.

A principal finalidade da interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) é permitir que os desenvolvedores de aplicativos criem uma interface do usuário para ajustar os parâmetros brutos que funcionarão da maneira mais consistente possível entre codecs diferentes. Suponha que um usuário final ajustará os parâmetros usando um controle deslizante, com seus valores mínimo e máximo mapeados para os intervalos mínimo e máximo para o parâmetro. Para dar suporte a isso, você deve fazer todos os esforços para tratar todos os intervalos de parâmetro como lineares. Para garantir que os controles deslizantes não sejam excessivamente confidenciais, você também deve oferecer suporte a um intervalo maior possível para cada parâmetro, cobrindo pelo menos 50% do intervalo máximo possível. Por exemplo, se o intervalo máximo possível de contraste for de cinza puro para puro preto e branco, com o valor padrão sendo mapeado para 0,0, o intervalo mínimo com suporte de um codec será de pelo menos meio entre o valor padrão e o cinza puro no nível inferior (– 1,0), para pelo menos meio entre o valor padrão e o preto puro e o branco no alto fim (+ 1,0).


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



-   [QueryRawCapabilitiesInfo](#queryrawcapabilitiesinfo)
-   [Parameterset](#loadparameterset)
-   [GetCurrentParameterSet](#getcurrentparameterset)
-   [Definir/GetExposureCompensation](#setgetexposurecompensation)
-   [Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/GetContrast](#setgetcontrast)
-   [Set/getgama](#setgetgamma)
-   [Set/getnitidez](#setgetsharpness)
-   [Set/GetSaturation](#setgetsaturation)
-   [Definir/getmatiz](#setgettint)
-   [Definir/GetNoiseReduction](#setgetnoisereduction)
-   [SetDestinationColorContext](#setdestinationcolorcontext)
-   [Definir/GetToneCurve](#setgettonecurve)
-   [Definir/getrotation](#setgetrotation)
-   [Set/getrenderingmode](#setgetrendermode)
-   [SetNotificationCallback](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>QueryRawCapabilitiesInfo

[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) retorna o conjunto de recursos com suporte para esse arquivo bruto. A estrutura [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) é definida da seguinte maneira:


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



A enumeração [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) usada nesta estrutura é definida como:


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



O campo final é uma enumeração [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , definida como:


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a>Parameterset

O [**parameterset**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) permite que o usuário especifique se deseja usar as configurações de captura, usar configurações ajustadas pelo usuário ou solicitar que o decodificador corrija a imagem automaticamente.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) retorna um **IPropertyBag2** com o conjunto de parâmetros atual. Em seguida, o chamador pode passar esse parâmetro definido para o codificador a ser usado como as opções de codificador.

### <a name="setgetexposurecompensation"></a>Definir/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) e [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicam a compensação de exposição a ser aplicada à saída final. O intervalo válido para EV é de – 5,0 a + 5,0 paradas.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin

Todas essas funções fornecem maneiras de obter e definir o ponto branco, como um valor RGB, um valor nomeado predefinido ou como um valor de Kelvin. O intervalo aceitável para Kelvin é 1.500 – 30.000.

### <a name="setgetcontrast"></a>Set/GetContrast

[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) e [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicam a quantidade de contraste a ser aplicada à saída. O intervalo válido para especificar o contraste é – 1,0 a + 1,0, com o contraste padrão sendo 0,0.

### <a name="setgetgamma"></a>Set/getgama

[**Getgama**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) e [**setgama**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicam o gama a ser aplicado. O intervalo válido para gama é de 0,2 a 5,0, com 1,0 sendo o padrão. Normalmente, o gama é implementado usando a função de energia gama tradicional (uma função de energia linear com lucro de Unity). O brilho aumenta com o aumento de gama e diminui conforme o gama se aproxima de zero. (Observe que o valor mínimo é diferente de zero, porque zero resultaria em um erro de divisão por zero nos cálculos de gama tradicionais. O limite mínimo lógico é 1/máx. é por isso que o mínimo é 0,2.)

### <a name="setgetsharpness"></a>Set/getnitidez

[**Getnitidez**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) e [**setnitidez**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicam a quantidade de nitidez a ser aplicada. O intervalo válido é de – 1,0 a + 1,0, com 0,0 sendo a quantidade padrão de nitidez e – 1,0 indicando nenhuma nitidez.

### <a name="setgetsaturation"></a>Set/GetSaturation

[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) e [**setsaturação**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicam a quantidade de saturação a ser aplicada. O intervalo válido para especificar a saturação é de – 1,0 a + 1,0, com 0,0 sendo saturação normal, – 1,0 representando a dessaturação completa e + 1,0, representando a saturação completa.

### <a name="setgettint"></a>Definir/getmatiz

[**Getmatiz**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) e [**settonalidade**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicam a tonalidade a ser aplicada, em uma inclinação verde/magenta. O intervalo válido é de – 1,0 a + 1,0, sendo que verde está no lado negativo da escala e magenta no positivo. A escala de tonalidade é definida como ortogonal à temperatura de cor.

### <a name="setgetnoisereduction"></a>Definir/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) e [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicam a quantidade de redução de ruído a ser aplicada. O intervalo válido para é de – 1,0 a + 1,0, com 0,0 indicando a quantidade padrão de redução de ruído, – 1,0 indicando nenhuma redução de ruído e + 1,0, indicando a redução máxima de ruído.

### <a name="setdestinationcolorcontext"></a>SetDestinationColorContext

[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) especifica o perfil de cor a ser aplicado à imagem. Você pode chamar [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) para recuperar o perfil de cor atual.

### <a name="setgettonecurve"></a>Definir/GetToneCurve

[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) e [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) especifique a curva de Tom a ser aplicada. Assuma a interpolação linear entre pontos. O **pToneCurve** é uma estrutura [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) , que contém uma matriz de estruturas [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) e uma contagem do número de pontos na matriz.


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



Um [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contém um valor de entrada e um valor de saída.


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



Quando o chamador passa **NULL** no parâmetro *pToneCurve* , você deve passar de volta o tamanho necessário para o [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) no parâmetro *pcbActualToneCurveBufferSize* .

### <a name="setgetrotation"></a>Definir/getrotation

[**Getrotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) e [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicam o grau de rotação a ser aplicado. Uma rotação de 90,0 especificaria uma rotação de 90 graus no sentido horário. (A diferença entre usar **SetRotation** e definir a rotação usando o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) é que o ângulo de rotação definido usando **SetRotation** deve ser persistido pelo codec, ao passo que definir a rotação por meio de **CopyPixels** apenas gira a imagem na memória.

### <a name="setgetrendermode"></a>Set/getrenderingmode

[**Getprocessmode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) e [**setrenderingmode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicam o nível de qualidade exigido pelo chamador. Quando um usuário estiver ajustando parâmetros, o aplicativo deverá exibir uma aproximação muito rápida da aparência da imagem real se as alterações forem aplicadas. Para essa finalidade, a imagem geralmente é exibida na resolução da tela ou menos, em vez da resolução de imagem real, para fornecer comentários imediatos ao usuário. Isso ocorre quando um aplicativo solicita qualidade de modo de rascunho, então isso deve ser muito rápido. Quando o usuário fez todas as alterações, as exibiu no modo de rascunho e decidiu decodificar a imagem completa com as configurações atuais, o aplicativo solicita uma decodificação de melhor qualidade. Normalmente, isso também é solicitado para impressão. Onde é necessária uma compensação razoável entre a velocidade de uma qualidade, o aplicativo solicita a qualidade normal.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registra uma função de retorno de chamada para o decodificador chamar quando qualquer um dos parâmetros de processamento brutos for alterado. A assinatura para [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) tem apenas um método, chamado [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify). **Notify** tem um único parâmetro, que é uma máscara que indica qual dos parâmetros de processamento brutos foram alterados.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Uma operação ou é executada nos valores a seguir para o NotificationMask.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Implementando um codificador de WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



