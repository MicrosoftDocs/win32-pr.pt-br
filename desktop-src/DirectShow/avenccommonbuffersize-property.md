---
description: Especifica o tamanho do buffer usado durante a codificação. Essa propriedade se aplica somente aos modos de codificação CBR (taxa de bits constante) e VBR (taxa de bits variável).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Propriedade AVEncCommonBufferSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69eb0c4829d30f3eff0297b7e591686f671d0d67967a65dc76695878d74b454e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794726"
---
# <a name="avenccommonbuffersize-property"></a>Propriedade AVEncCommonBufferSize

Especifica o tamanho do buffer usado durante a codificação. Essa propriedade se aplica somente aos modos de codificação CBR (taxa de bits constante) e VBR (taxa de bits variável).

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonBufferSize**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade tem um intervalo linear de valores. Para obter o intervalo com suporte, chame [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange). Não há suporte para intervalos de parâmetros para codificadores de câmera UVC 1.5 H.264.

## <a name="remarks"></a>Comentários

Para alguns formatos de vídeo, o tamanho do buffer é especificado em bits e, para outros, é especificado em bytes. Consulte os comentários abaixo para obter informações específicas.

Para o vídeo MPEG, essa propriedade define o tamanho do buffer do verificador de buffer de vídeo (VBV). O tamanho do buffer está em bits.

Para vídeo H.264 e Windows Media Video, a propriedade define o tamanho do HRD (decodificador de referência hipotética). O tamanho do buffer é em bytes.

Para câmeras de codificação UVC 1.5 H264, o valor de CPB enviado ao codificador de câmera deve ser alinhado de 16 bits. O tamanho do buffer é em bytes.

Essa propriedade também é usada com codificadores de câmera [UVC 1.5 H.264](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

