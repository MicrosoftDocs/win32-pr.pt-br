---
description: Especifica o nível médio de volume do conteúdo de áudio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: MFPKEY_WMADRC_AVGREF propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7d3575b81ca878c610aed95ca25f73fa94c292ec16f9245a72a3a9515198c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973235"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>Propriedade AVGREF MFPKEY \_ WMADRC \_

Especifica o nível médio de volume do conteúdo de áudio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCAverageReference

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="remarks"></a>Comentários

Você pode obter esse valor do codificador depois que o conteúdo for processado. Esse valor também pode ser definido no decodificador para fins de controle de intervalo dinâmico, mas terá um efeito somente se a propriedade [ \_ \_ DRCMODE MFPKEY WCODEC](mfpkey-wmadec-drcmodeproperty.md) estiver definida.

Para obter mais informações sobre o controle de intervalo dinâmico, consulte o artigo da [Web Windows De áudio de Professional recursos do Codec](/previous-versions/ms867218(v=msdn.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
