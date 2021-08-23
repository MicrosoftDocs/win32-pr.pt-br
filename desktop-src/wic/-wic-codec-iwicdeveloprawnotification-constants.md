---
description: Sinalizadores usados por IWICDevelopRawNotificationCallback para indicar quais membros foram alterados.
ms.assetid: 4e94b4f4-abd9-4395-87ec-a08e49a2cf88
title: Constantes IWICDevelopRawNotificationCallback (Wincodec.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885a99ea21ccafdb3961387013d0f6d9f466e48ffe542a3349af7e658b1b1786
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592456"
---
# <a name="iwicdeveloprawnotificationcallback-constants"></a>Constantes IWICDevelopRawNotificationCallback

Sinalizadores usados por [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) para indicar quais membros foram alterados.



| Constante/valor                                                                                                                                                                                                                                                                                                                                                                                            | Descrição                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| <span id="WICRawChangeNotification_ExposureCompensation"></span><span id="wicrawchangenotification_exposurecompensation"></span><span id="WICRAWCHANGENOTIFICATION_EXPOSURECOMPENSATION"></span><dl> <dt>**WICRawChangeNotification \_ ExposureCompensation**</dt> <dt>0x00000001</dt> </dl>             | Máscara usada para relatar uma alteração de compensação de exposição.<br/>                                                       |
| <span id="WICRawChangeNotification_NamedWhitePoint"></span><span id="wicrawchangenotification_namedwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_NAMEDWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ NamedWhitePoint**</dt> <dt>0x00000002</dt> </dl>                                 | Máscara usada para relatar uma [**alteração WICNamedWhitePoint.**](/windows/desktop/api/Wincodec/ne-wincodec-wicnamedwhitepoint)<br/>                 |
| <span id="WICRawChangeNotification_KelvinWhitePoint"></span><span id="wicrawchangenotification_kelvinwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_KELVINWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ WhitePoint**</dt> <dt>0x00000004</dt> </dl>                             | Máscara usada para relatar uma alteração de ponto branco.<br/>                                                          |
| <span id="WICRawChangeNotification_RGBWhitePoint"></span><span id="wicrawchangenotification_rgbwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_RGBWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ RGBWhitePoint**</dt> <dt>0x00000008</dt> </dl>                                         | Máscara usada para relatar uma alteração de ponto branco RGB.<br/>                                                             |
| <span id="WICRawChangeNotification_Contrast"></span><span id="wicrawchangenotification_contrast"></span><span id="WICRAWCHANGENOTIFICATION_CONTRAST"></span><dl> <dt>**WICRawChangeNotification \_ Contraste**</dt> <dt>0x00000010</dt> </dl>                                                             | Máscara usada para relatar uma alteração de contraste.<br/>                                                                    |
| <span id="WICRawChangeNotification_Gamma"></span><span id="wicrawchangenotification_gamma"></span><span id="WICRAWCHANGENOTIFICATION_GAMMA"></span><dl> <dt>**WICRawChangeNotification \_ Gama**</dt> <dt>0x00000020</dt> </dl>                                                                         | Máscara usada para relatar uma alteração gama.<br/>                                                                       |
| <span id="WICRawChangeNotification_Sharpness"></span><span id="wicrawchangenotification_sharpness"></span><span id="WICRAWCHANGENOTIFICATION_SHARPNESS"></span><dl> <dt>**WICRawChangeNotification \_ 0x00000040**</dt> <dt></dt> </dl>                                                         | Máscara usada para relatar uma alteração de sharpness.<br/>                                                                   |
| <span id="WICRawChangeNotification_Saturation"></span><span id="wicrawchangenotification_saturation"></span><span id="WICRAWCHANGENOTIFICATION_SATURATION"></span><dl> <dt>**WICRawChangeNotification \_ Saturação**</dt> <dt>0x00000080</dt> </dl>                                                     | Máscara usada para relatar uma alteração de saturação.<br/>                                                                  |
| <span id="WICRawChangeNotification_Tint"></span><span id="wicrawchangenotification_tint"></span><span id="WICRAWCHANGENOTIFICATION_TINT"></span><dl> <dt>**WICRawChangeNotification \_ Tint**</dt> <dt>0x00000100</dt> </dl>                                                                             | Máscara usada para relatar uma alteração de tonalidade.<br/>                                                                        |
| <span id="WICRawChangeNotification_NoiseReduction"></span><span id="wicrawchangenotification_noisereduction"></span><span id="WICRAWCHANGENOTIFICATION_NOISEREDUCTION"></span><dl> <dt>**WICRawChangeNotification \_ NoiseReduction**</dt> <dt>0x00000200</dt> </dl>                                     | Máscara usada para relatar uma alteração de redução de ruído.<br/>                                                             |
| <span id="WICRawChangeNotification_DestinationColorContext"></span><span id="wicrawchangenotification_destinationcolorcontext"></span><span id="WICRAWCHANGENOTIFICATION_DESTINATIONCOLORCONTEXT"></span><dl> <dt>**WICRawChangeNotification \_ DestinationColorContext**</dt> <dt>0x00000400</dt> </dl> | Máscara usada para relatar uma alteração de contexto de cor de destino.<br/>                                                   |
| <span id="WICRawChangeNotification_ToneCurve"></span><span id="wicrawchangenotification_tonecurve"></span><span id="WICRAWCHANGENOTIFICATION_TONECURVE"></span><dl> <dt>**WICRawChangeNotification \_ ToneCurve**</dt> <dt>0x00000800</dt> </dl>                                                         | Máscara usada para relatar uma alteração de curva de tom.<br/>                                                                  |
| <span id="WICRawChangeNotification_Rotation"></span><span id="wicrawchangenotification_rotation"></span><span id="WICRAWCHANGENOTIFICATION_ROTATION"></span><dl> <dt>**WICRawChangeNotification \_ Rotação**</dt> <dt>0x00001000</dt> </dl>                                                             | Máscara usada para relatar uma [**alteração WICRawRotationCapabilities.**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities)<br/> |
| <span id="WICRawChangeNotification_RenderMode"></span><span id="wicrawchangenotification_rendermode"></span><span id="WICRAWCHANGENOTIFICATION_RENDERMODE"></span><dl> <dt>**WICRawChangeNotification \_ RenderMode**</dt> <dt>0x00002000</dt> </dl>                                                     | Máscara usada para relatar uma [**alteração WICRawRenderMode.**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode)<br/>                     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, Windows aplicativos da área de trabalho do Vista \[\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Wincodec.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)
</dt> </dl>

 

 




