---
title: Elemento EnableQuarantineChecks (EapType)
description: Saiba mais sobre o elemento EnableQuarantineChecks (EapType). Esse elemento indica se as verificações de NAP (proteção de acesso à rede) devem ser executadas.
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Elemento EnableQuarantineChecks EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917696"
---
# <a name="enablequarantinechecks-eaptype-element"></a>Elemento EnableQuarantineChecks (EapType)

O elemento **EnableQuarantineChecks (EapType)** indica se as verificações de NAP (proteção de acesso à rede) devem ser executadas.

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

O elemento **EnableQuarantineChecks** é definido pelo elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Comentários

Se o elemento **EnableQuarantineChecks** for true, o PEAP executará verificações de NAP; Se for FALSE, o PEAP não executará verificações de NAP. O elemento **EnableQuarantineChecks** é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos do esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





