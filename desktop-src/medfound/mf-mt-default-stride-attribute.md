---
description: Avanço de superfície padrão, para um tipo de mídia de vídeo descompactado. Stride é o número de bytes necessários para passar de uma linha de pixels para a próxima.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: MF_MT_DEFAULT_STRIDE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e130918f62d6ff986ced7dd6449dcc2d381a00fc0d7c0342eeb4afcc03833bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035234"
---
# <a name="mf_mt_default_stride-attribute"></a>Atributo \_ MF MT \_ DEFAULT \_ STRIDE

Avanço de superfície padrão, para um tipo de mídia de vídeo descompactado. Stride é o número de bytes necessários para passar de uma linha de pixels para a próxima.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Trate como um **valor INT32.**

## <a name="remarks"></a>Comentários

O valor do atributo é armazenado como **um UINT32,** mas deve ser lançado em um valor inteiro com sinal de 32 bits. Stride pode ser negativo.

Stride é positivo para imagens de cima para baixo e negativo para imagens de baixo para cima.

Esse atributo fornece o passo a passo para *uma representação contígua* da imagem na memória; ou seja, uma representação sem bytes de preenchimento adicionais após cada linha. Se um buffer de mídia dá suporte à interface [**IMF2DBuffer,**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) use o método [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para obter o avanço real da superfície, que pode incluir bytes de preenchimento extra.

Para obter mais informações sobre o avanço da superfície, consulte [Image Stride.](image-stride.md)

Para ver um exemplo de como calcular o passo padrão, consulte [Buffers de vídeo descompactados.](uncompressed-video-buffers.md)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Passo da imagem](image-stride.md)
</dt> </dl>

 

 




