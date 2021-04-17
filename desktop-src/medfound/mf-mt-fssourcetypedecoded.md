---
description: Especifica se um decodificador pode usar os carimbos de data/hora (DTS) ao definir carimbos de data/hora.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790437"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>\_ \_ Atributo FSSourceTypeDecoded MF MT

Especifica que um tipo de mídia é decodificado automaticamente.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**


## <a name="remarks"></a>Comentários
Um tipo de mídia é marcado como um atributo para indicar que isso não existe na origem física e é sintetizado pelo pipeline. Um valor de 1 (TRUE) indica que o tipo de mídia está sintetizado. Um valor de 0 (FALSE) ou o valor não está presente, indica que ele não é.

Na versão atual, esse atributo deve ser especificado usando o seguinte valor de GUID em vez da constante de MD_MT_FSSourceTypeDecoded:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




