---
description: Contém o GUID de categoria para uma Media Foundation transformação (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: Propriedade MFPKEY_CATEGORY (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828618"
---
# <a name="mfpkey_category-property"></a>\_Propriedade de categoria MFPKEY

Contém o GUID de categoria para uma Media Foundation transformação (MFT).



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**GUID** (**CLSID** \* )

CLSID do VT \_

**puuid**



## <a name="remarks"></a>Comentários

O valor dessa propriedade é um GUID que identifica a categoria de MFT. Para obter uma lista de categorias, consulte a [**\_ categoria MFT**](mft-category.md).

Essa propriedade é opcional e é apenas informativa. Uma MFT pode usar essa propriedade para relatar a categoria sob a qual ela está registrada. Para obter essa propriedade, consulte o MFT para a interface **IPropertyStore** .

Para enumerar uma categoria de MFT, chame a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) . Não há nenhum vínculo direto entre a função **MFTEnum** e essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




