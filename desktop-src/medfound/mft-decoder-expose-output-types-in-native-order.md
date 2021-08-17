---
description: Especifica se um decodificador expõe tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b91492054215aee5a63dbcf0adf300d74933a0859a2d71256e7e4352deba9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872335"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>MFT \_ DECODER \_ EXPÕE TIPOS DE SAÍDA NO atributo NATIVE \_ \_ \_ \_ \_ ORDER

Especifica se um decodificador expõe tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo é uma dica para o decodificador organizar sua lista de tipos de saída em uma ordem específica, dependendo do uso pretendido, reprodução ou transcodificar.

Para a maioria dos formatos de codificação (H.264, MPEG-2, WMV), os decodificadores de vídeo no Microsoft Media Foundation suportam várias saídas YUV comuns, incluindo NV12, YV12, YUY2, IYUV e I420. O decodificador oferece uma lista ordenada de tipos de saída por meio de [**seu método IMFTransform::GetOutputAvailableType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)

Para reprodução, NV12 é o formato mais eficiente e amplamente suportado. Portanto, por padrão, os decodificadores normalmente oferecem NV12 como o primeiro tipo de saída na lista. Isso minimiza o tempo necessário para resolver o tipo de mídia ao criar uma topologia de reprodução. No entanto, para transcodificação, IYUV ou I420 são mais eficientes para a CPU e normalmente são preferenciais por codificadores.

Se um decodificador dá suporte a esse atributo, o atributo tem o seguinte comportamento:

-   Se o atributo tiver um valor não zero, IYUV e I420 aparecerão primeiro na lista de tipos de mídia de saída. Essa configuração é mais eficiente para transcodificação.
-   Se o atributo for zero, NV12 aparecerá primeiro na lista de tipos de mídia de saída. Essa configuração é mais eficiente para reprodução e é o padrão.

Para definir esse atributo:

1.  Chame [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no decodificador para obter um [**ponteiro IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para adicionar o atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




