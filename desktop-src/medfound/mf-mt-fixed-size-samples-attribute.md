---
description: Especifica para um tipo de mídia se os exemplos têm um tamanho fixo.
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: Atributo MF_MT_FIXED_SIZE_SAMPLES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3662532d1e10857945a828ec3f46beef991fb438dfea0f33dc7d73832aeca7e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605626"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a>\_Atributo de \_ \_ exemplos de tamanho fixo MF MT \_

Especifica para um tipo de mídia se os exemplos têm um tamanho fixo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, todas as amostras no fluxo serão do mesmo tamanho (em bytes). Caso contrário, os exemplos podem variar em tamanho.

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

 

 




