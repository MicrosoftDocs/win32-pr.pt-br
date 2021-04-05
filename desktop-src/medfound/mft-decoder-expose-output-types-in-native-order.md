---
description: Especifica se um decodificador expõe os tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: Atributo MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661826"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>O \_ decodificador MFT \_ expõe os \_ \_ tipos \_ de saída no \_ atributo de \_ ordem nativa

Especifica se um decodificador expõe os tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo é uma dica para que o decodificador Organize sua lista de tipos de saída em uma ordem específica, dependendo do uso pretendido, reprodução ou transcodificação.

Para a maioria dos formatos de codificação (H. 264, MPEG-2, WMV), os decodificadores de vídeo no Microsoft Media Foundation oferecem suporte a várias saídas YUV comuns, incluindo NV12, YV12, YUY2, IYUV e I420. O decodificador oferece uma lista ordenada de tipos de saída por meio de seu método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) .

Para reprodução, o NV12 é o formato mais eficiente e com suporte amplo. Portanto, por padrão, os decodificadores normalmente oferecem NV12 como o primeiro tipo de saída na lista. Isso minimiza o tempo necessário para resolver o tipo de mídia ao criar uma topologia de reprodução. Para transcodificação, no entanto, IYUV ou I420 são mais eficientes para a CPU e normalmente são preferenciais por codificadores.

Se um decodificador oferecer suporte a esse atributo, o atributo terá o seguinte comportamento:

-   Se o atributo tiver um valor diferente de zero, IYUV e I420 aparecerão primeiro na lista de tipos de mídia de saída. Essa configuração é mais eficiente para transcodificação.
-   Se o atributo for zero, NV12 aparecerá primeiro na lista de tipos de mídia de saída. Essa configuração é mais eficiente para reprodução e é o padrão.

Para definir este atributo:

1.  Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no decodificador para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para adicionar o atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




