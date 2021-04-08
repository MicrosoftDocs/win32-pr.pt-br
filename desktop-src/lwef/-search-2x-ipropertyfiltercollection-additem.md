---
title: Propriedade AddItem IPropertyFilterCollection (WdsSharedIDL. h)
description: Adiciona um novo filtro à coleção.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- Recursos do ambiente Windows herdado da propriedade AddItem
- Propriedade AddItem recursos de ambiente do Windows herdados, interface IPropertyFilterCollection
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection, Propriedade AddItem
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
ms.openlocfilehash: b199f0e696f75fb5549b274ac888989f7a723b48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009224"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>Propriedade IPropertyFilterCollection:: AddItem

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





