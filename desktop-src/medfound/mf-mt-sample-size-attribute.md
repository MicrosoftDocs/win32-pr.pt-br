---
description: Especifica o tamanho de cada amostra, em bytes, em um tipo de mídia.
ms.assetid: 4c28f73d-ff40-4eb9-a45f-57a60df719c6
title: Atributo MF_MT_SAMPLE_SIZE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f032d52c4b63329b50597bd512a5f3c50e1b74b5d2c5d5d6e84bc506feb7bd3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060086"
---
# <a name="mf_mt_sample_size-attribute"></a>\_Atributo de \_ tamanho de amostra MF MT \_

Especifica o tamanho de cada amostra, em bytes, em um tipo de mídia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo será válido somente se o atributo de [**\_ \_ \_ \_ exemplos de tamanho fixo MF MT**](mf-mt-fixed-size-samples-attribute.md) for **true**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



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
</dt> </dl>

 

 




