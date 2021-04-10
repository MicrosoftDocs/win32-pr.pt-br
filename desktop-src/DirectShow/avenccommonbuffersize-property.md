---
description: Especifica o tamanho do buffer usado durante a codificação. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Propriedade AVEncCommonBufferSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087849"
---
# <a name="avenccommonbuffersize-property"></a>Propriedade AVEncCommonBufferSize

Especifica o tamanho do buffer usado durante a codificação. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonBufferSize**

## <a name="property-value"></a>Valor da propriedade

Esta propriedade tem um intervalo linear de valores. Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange). Os intervalos de parâmetros não têm suporte para codificadores de câmera H. 264 UVC 1,5.

## <a name="remarks"></a>Comentários

Para alguns formatos de vídeo, o tamanho do buffer é especificado em bits e para outros, ele é especificado em bytes. Consulte os comentários abaixo para obter informações específicas.

Para o vídeo MPEG, essa propriedade define o tamanho do buffer do verificador de buffer de vídeo (VBV). O tamanho do buffer está em bits.

Para vídeos H. 264 e vídeo de mídia do Windows, a propriedade define o tamanho do decodificador de referência hipotética (HRD). O tamanho do buffer está em bytes.

Para câmeras de codificação UVC 1,5 H264, o valor de CPB enviado para o codificador de câmera deve ser alinhado em 16 bits. O tamanho do buffer está em bytes.

Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

