---
description: Especifica para um tipo de mídia se os dados de mídia estão compactados.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: Atributo MF_MT_COMPRESSED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502384"
---
# <a name="mf_mt_compressed-attribute"></a>\_ \_ Atributo compactado do MF MT

Especifica para um tipo de mídia se os dados de mídia estão compactados.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, o tipo de mídia será um formato compactado. Caso contrário, o tipo de mídia é descompactado ou o tipo de compactação não é conhecido.

Não há garantia de que esse atributo seja definido como **true** para todos os formatos compactados; portanto, os aplicativos geralmente não devem confiar nesse atributo. A maneira mais confiável de determinar se um formato é compactado é manter uma lista de formatos conhecidos. Se um aplicativo não reconhecer um formato, conforme especificado no atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) , ele não deverá assumir nada sobre a compactação do formato.

Para determinar se um formato usa a compactação temporal (o que significa que alguns exemplos são calculados como deltas de amostras anteriores), verifique o atributo [**\_ \_ independente de todos os \_ exemplos \_ do MF MT**](mf-mt-all-samples-independent-attribute.md) .

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
</dt> </dl>

 

 




