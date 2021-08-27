---
description: MF_MT_FSSourceTypeDecoded atributo – especifica se um decodificador pode usar DTS (carimbos de data/hora de decodificar) ao definir carimbos de data/hora.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae25fce343d0c24f7b0a79e2623e7c3e2d0f9272b2f95a825860860ff6f88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113756"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>Atributo \_ MF MT \_ FSSourceTypeDecoded

Especifica que um tipo de mídia é decodificado automaticamente.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**


## <a name="remarks"></a>Comentários
Um tipo de mídia é marcado como um atributo para indicar que isso não existe na fonte física e é sintetizado pelo pipeline. Um valor de 1 (TRUE) indica que o tipo de mídia é sintetizado. Um valor de 0 (FALSE) ou o valor que não está presente indica que não está.

Na versão atual, esse atributo deve ser especificado usando o seguinte valor guid em vez da MD_MT_FSSourceTypeDecoded constante:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




