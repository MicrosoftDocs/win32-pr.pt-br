---
description: Defina como um atributo para um objeto IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: Atributo MFPROTECTIONATTRIBUTE_BEST_EFFORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165296"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a>\_Atributo de melhor esforço do MFPROTECTIONATTRIBUTE \_

Defina como um atributo para um objeto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) . Se esse atributo estiver presente, uma tentativa com falha de aplicar a proteção será ignorada. Se o valor do atributo associado for **true**, o esquema de proteção com o atributo de [ \_ failover \_ MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) deverá ser aplicado.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Se **verdadeiro**, aplique o esquema de proteção com o atributo de [ \_ \_ failover MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) se a configuração dessa proteção falhar.

Defina como um atributo para um objeto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos UWP do Windows 8\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Somente aplicativos UWP do Windows Server 2012 \[\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




