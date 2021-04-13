---
description: Stride de superfície padrão, para um tipo de mídia de vídeo descompactado. Stride é o número de bytes necessários para ir de uma linha de pixels para a próxima.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: Atributo MF_MT_DEFAULT_STRIDE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165019"
---
# <a name="mf_mt_default_stride-attribute"></a>\_ \_ Atributo Stride padrão MF MT \_

Stride de superfície padrão, para um tipo de mídia de vídeo descompactado. Stride é o número de bytes necessários para ir de uma linha de pixels para a próxima.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor **INT32** .

## <a name="remarks"></a>Comentários

O valor do atributo é armazenado como um **UINT32**, mas deve ser convertido em um valor inteiro assinado de 32 bits. O stride pode ser negativo.

Stride é positivo para imagens de cima para baixo e negativo para imagens de baixo para cima.

Esse atributo fornece o stride para uma representação *contígua* da imagem na memória; ou seja, uma representação sem nenhum byte de preenchimento adicional após cada linha. Se um buffer de mídia der suporte à interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , use o método [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para obter o stride real da superfície, que pode incluir bytes de preenchimento extras.

Para obter mais informações sobre o stride de superfície, consulte [Stride de imagem](image-stride.md).

Para obter um exemplo de como calcular o stride padrão, consulte [buffers de vídeo não compactados](uncompressed-video-buffers.md).

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Stride da imagem](image-stride.md)
</dt> </dl>

 

 




