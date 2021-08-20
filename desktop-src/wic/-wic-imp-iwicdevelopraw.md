---
description: Implementando IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implementando IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68a78705fcfb53651d1099d01d17d9ddff554df9632a5cc322db229bc04d38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965005"
---
# <a name="implementing-iwicdevelopraw"></a>Implementando IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

A interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expõe opções de processamento específicas ao processamento de imagem bruto. Todos os codecs brutos devem dar suporte à interface **IWICDevelopRaw.** Alguns codecs brutos podem não ser capazes de dar suporte a todas as configurações expostas por essa interface, mas você deve dar suporte a todas as configurações que seu codec é capaz de executar. No mínimo, cada codec bruto deve implementar os [**métodos SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) e [**SetRenderMode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode)

Além disso, alguns métodos e interfaces opcionais para outros codecs são altamente recomendados para codecs brutos. Eles incluem os métodos [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) e [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) na classe de decodificador no nível do contêiner e a interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na classe de decodificar no nível do quadro.

Configurações definidos usando os métodos [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) devem ser persistido pelo codec de uma maneira consistente com a maneira como outros metadados são persistentes, mas você nunca deve substituir as configurações originais de "As Shot". Ao persistir os metadados e implementar [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) e [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), você permite que aplicativos de processamento bruto recuperem e apliquem configurações de processamento entre sessões.

Uma finalidade principal da interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) é permitir que os desenvolvedores de aplicativos criem uma interface do usuário para ajustar parâmetros brutos que funcionarão da maneira mais consistente possível em diferentes codecs. Suponha que um usuário final ajuste os parâmetros usando um controle deslizante, com seus valores mínimo e máximo mapeados para os intervalos mínimo e máximo para o parâmetro. Para dar suporte a isso, você deve fazer todos os esforços para tratar todos os intervalos de parâmetros como lineares. Para garantir que os controles deslizantes não sejam muito confidenciais, você também deve dar suporte à maior variedade possível para cada parâmetro, abrangendo pelo menos 50% do intervalo máximo possível. Por exemplo, se o intervalo máximo possível de contraste for de cinza puro a preto e branco puros, com o valor padrão sendo mapeado para 0,0, o intervalo mínimo com suporte de um codec será de pelo menos a metade entre o valor padrão e o cinza puro na extremidade baixa (–1,0), até pelo menos a metade entre o valor padrão e preto e branco puros no alto(+1,0).


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
-   [LoadParameterSet](#loadparameterset)
-   [GetCurrentParameterSet](#getcurrentparameterset)
-   [Set/GetExposureCompensation](#setgetexposurecompensation)
-   [Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/GetContrast](#setgetcontrast)
-   [Set/GetGamma](#setgetgamma)
-   [Set/GetSharpness](#setgetsharpness)
-   [Set/GetS saturação](#setgetsaturation)
-   [Set/GetTint](#setgettint)
-   [Set/GetNoiseReduction](#setgetnoisereduction)
-   [SetDestinationColorContext](#setdestinationcolorcontext)
-   [Set/GetToneCurve](#setgettonecurve)
-   [Set/GetRotation](#setgetrotation)
-   [Set/GetRenderMode](#setgetrendermode)
-   [SetNotificationCallback](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>QueryRawCapabilitiesInfo

[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) retorna o conjunto de recursos com suporte para esse arquivo bruto. A [**estrutura WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) é definida da seguinte forma:


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



A [**enumeração WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) usada nesta estrutura é definida como:


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



O campo final é uma [**enumeração WICRawRotationCapabilities,**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) definida como:


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a>LoadParameterSet

[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) permite que o usuário especifique se deve usar as configurações de As Shot, usar configurações ajustadas pelo usuário ou solicitar que o decodificador corrija automaticamente a imagem.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) retorna **um IPropertyBag2** com o parâmetro atual definido. O chamador pode passar esse parâmetro definido para o codificador a ser usado como as opções do codificador.

### <a name="setgetexposurecompensation"></a>Set/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) e [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicam a compensação de exposição a ser aplicada à saída final. O intervalo válido para EV é –5,0 a +5,0 paradas.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin

Todas essas funções fornecem maneiras de obter e definir o ponto em branco, como um valor RGB, uma predefinição chamada valor ou como um valor DeIa. O intervalo aceitável para Ela é de 1.500 a 30.000.

### <a name="setgetcontrast"></a>Set/GetContrast

[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) e [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicam a quantidade de contraste a ser aplicada à saída. O intervalo válido para especificar o contraste é –1,0 a +1,0, com o contraste padrão sendo 0,0.

### <a name="setgetgamma"></a>Set/GetGamma

[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) e [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicam o Gama a ser aplicado. O intervalo válido para Gama é de 0,2 a 5,0, sendo 1,0 o padrão. O Gama normalmente é implementado usando a função de energia gama tradicional (uma função de energia linear com ganho de unidade). O brilho aumenta com o aumento de Gama e diminui à medida que o Gama se aproxima de zero. (Observe que o valor mínimo é não zero, porque zero resultaria em um erro de divisão por zero em cálculos gama tradicionais. O limite mínimo lógico é 1/máx. Por isso, o mínimo é 0,2.)

### <a name="setgetsharpness"></a>Set/GetSharpness

[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) e [**SetSharpness indicam**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) a quantidade de ajuste a ser aplicada. O intervalo válido é de –1,0 a +1,0, sendo 0,0 a quantidade padrão de ajuste e –1,0 indicando nenhuma desagundo.

### <a name="setgetsaturation"></a>Set/GetS saturação

[**GetS saturação**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) e [**SetS saturação**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicam a quantidade de saturação a ser aplicada. O intervalo válido para especificar saturação é –1,0 a +1,0, com 0,0 sendo saturação normal, -1,0 representando a saturação completa e +1,0 representando saturação completa.

### <a name="setgettint"></a>Set/GetTint

[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) e [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicam a tonalidade a ser aplicada, em um desvio verde/magenta. O intervalo válido é –1,0 a +1,0, com verde no lado negativo da escala e magenta no positivo. A escala de tonalidade é definida como ortogonal para a temperatura da cor.

### <a name="setgetnoisereduction"></a>Set/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) e [**SetNoiseReduction indicam**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) a quantidade de redução de ruído a ser aplicada. O intervalo válido para é –1,0 a +1,0, com 0,0 indicando a quantidade padrão de redução de ruído, –1,0 indicando nenhuma redução de ruído e +1,0 indicando a redução máxima de ruído.

### <a name="setdestinationcolorcontext"></a>SetDestinationColorContext

[**SetDestinationColorContext especifica**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) o perfil de cor a ser aplicado à imagem. Você pode chamar [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) para recuperar o perfil de cor atual.

### <a name="setgettonecurve"></a>Set/GetToneCurve

[**GetToneCurve e**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) especificam a curva de tom a ser aplicada. Suponha a interpolação linear entre pontos. O **pToneCurve** é uma estrutura [**WICRawToneCurve,**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) que contém uma matriz de estruturas [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) e uma contagem do número de pontos na matriz.


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



Quando o chamador passar **NULL** no parâmetro *pToneCurve,* você deverá passar de volta o tamanho necessário para [**o WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) no parâmetro *pcbActualToneCurveBufferSize.*

### <a name="setgetrotation"></a>Set/GetRotation

[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) e [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicam o grau de rotação a ser aplicado. Uma rotação de 90,0 especificaria uma rotação de 90 graus no sentido horário. (A diferença entre usar **SetRotation** e definir a rotação usando o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) é que o conjunto de ângulos de rotação usando **SetRotation** deve ser persistido pelo codec, enquanto definir a rotação por meio de **CopyPixels** gira apenas a imagem na memória.

### <a name="setgetrendermode"></a>Set/GetRenderMode

[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) e [**SetRenderMode indicam o**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) nível de qualidade da saída que o chamador requer. Quando um usuário estiver ajustando parâmetros, o aplicativo deverá exibir uma aproximação muito rápida da aparência da imagem real se as alterações são aplicadas. Para essa finalidade, a imagem geralmente é exibida na resolução da tela ou menos, em vez da resolução de imagem real, para fornecer comentários imediatos ao usuário. Isso é quando um aplicativo solicita a qualidade do Modo de Rascunho, portanto, isso deve ser muito rápido. Quando o usuário tiver feito todas as alterações, visualizado-as no modo de rascunho e decidir decodificar a imagem completa com as configurações atuais, o aplicativo solicitará uma decodificação de Melhor Qualidade. Isso geralmente também é solicitado para impressão. Quando uma troca razoável entre a velocidade e uma qualidade é necessária, o aplicativo solicita Qualidade Normal.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registra uma função de retorno de chamada para o decodificador chamar quando qualquer um dos parâmetros de processamento bruto é alterado. A assinatura do [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) tem apenas um método, chamado [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify). **Notify** tem um único parâmetro, que é uma máscara que indica quais dos parâmetros de processamento brutos foram alterados.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Uma operação OR é executada nos valores a seguir para o NotificationMask.


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

**Conceitual**
</dt> <dt>

[Implementando IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Implementando um codificador WIC-Enabled aplicativo](-wic-implementingwicencoder.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



