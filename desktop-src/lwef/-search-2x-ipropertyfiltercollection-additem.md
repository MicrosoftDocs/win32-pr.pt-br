---
title: Propriedade AddItem IPropertyFilterCollection (WdsSharedIDL. h)
description: Adiciona um novo filtro à coleção.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- recursos de ambiente herdado de Windows de propriedade additem
- propriedade additem herdada Windows recursos de ambiente, interface IPropertyFilterCollection
- recursos de ambiente Windows da interface IPropertyFilterCollection herdados, propriedade additem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeafec95549fefa244dff6ff44ad9110150ae1b410e38b423a0a31f09cf54194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755443"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>Propriedade IPropertyFilterCollection:: AddItem

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

Adiciona um novo filtro à coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Valor da propriedade

Retorna um ponteiro para o endereço do novo filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com \[ aplicativos de área de trabalho do SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisador de desktops (WDS) 2.6.5<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





