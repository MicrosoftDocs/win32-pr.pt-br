---
description: O qualificador ViewSpaces define os nomes e o local dos namespaces onde as instâncias de origem estão localizadas. Você pode especificar qualquer combinação de namespaces em computadores locais ou remotos.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Qualificador ViewSpaces
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171778"
---
# <a name="viewspaces-qualifier"></a>Qualificador ViewSpaces

O **qualificador ViewSpaces** define os nomes e o local dos namespaces onde as instâncias de origem estão localizadas. Você pode especificar qualquer combinação de namespaces em computadores locais ou remotos.

O exemplo a seguir lista dois namespaces no computador local.


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



O [provedor de exibição](view-provider.md) corresponde às consultas de origem no [qualificador ViewSources](viewsources-qualifier.md) para os namespaces listados no qualificador **ViewSpaces** na ordem em que as consultas e os namespaces são listados. Normalmente, há uma relação um-para-um entre o número de namespaces listados no qualificador **ViewSpaces** e as consultas listadas no qualificador **ViewSources** . Em alguns casos, talvez você queira que as consultas listadas no qualificador ViewSources sejam executadas em dois ou mais namespaces. Você pode usar dois pontos duplos "::" para separar vários namespaces que serão avaliados por uma das consultas na matriz **ViewSources** .

No exemplo a seguir, a primeira consulta na matriz [**ViewSources**](viewsources-qualifier.md) será executada no namespace no primeiro par de aspas, a segunda consulta em relação aos três namespaces no segundo par de aspas e a terceira consulta em relação aos dois namespaces no terceiro par de aspas.


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificadores específicos para o provedor de exibição**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




