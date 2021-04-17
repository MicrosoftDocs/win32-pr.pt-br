---
description: Força o codificador a codificar o próximo quadro como um quadro-chave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Propriedade CODECAPI_AVEncVideoForceKeyFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812164"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

