---
description: Força o codificador a codificar o próximo quadro como um quadro-chave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Propriedade CODECAPI_AVEncVideoForceKeyFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e28738dcd7398ce04abe7f71778e94d7d5d4f49393365e92c43bbb347d98c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880702"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>\_Propriedade CODECAPI AVEncVideoForceKeyFrame

Força o codificador a codificar o próximo quadro como um quadro-chave.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoForceKeyFrame**

## <a name="property-value"></a>Valor da propriedade

Se o valor for diferente de zero, o codificador codificará o próximo quadro como um quadro-chave. Se o valor for zero, o codificador selecionará se deseja codificar o próximo quadro como um quadro-chave.

Essa propriedade se aplica ao próximo quadro que o codificador recebe como entrada. Para uma Media Foundation transformação (MFT), esse é o próximo quadro que é passado para o método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) . A configuração é redefinida como zero após o próximo quadro.

## <a name="remarks"></a>Comentários

Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

