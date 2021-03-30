---
title: Propriedade RemoveItem IPropertyFilterCollection (WdsSharedIDL. h)
description: Remove um filtro específico para a coleção.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- Recursos de ambiente herdado do Windows da propriedade RemoveItem
- Propriedade RemoveItem recursos de ambiente do Windows herdados, interface IPropertyFilterCollection
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection, Propriedade RemoveItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2994b636a7b8483d4b3f219648f137166b75790d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644856"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a>Propriedade IPropertyFilterCollection:: RemoveItem

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Remove um filtro específico para a coleção.

Essa propriedade é somente gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a>Valor da propriedade

Aceita um ponteiro para o índice do filtro a ser removido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





