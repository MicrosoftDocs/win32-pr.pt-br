---
title: Propriedade IPropertyFilter IndexColumn (WdsSharedIDL. h)
description: Nome da coluna indexada da propriedade pela qual filtrar.
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- Recursos do ambiente Windows herdado da propriedade IndexColumn
- Propriedade IndexColumn recursos de ambiente do Windows herdados, interface IPropertyFilter
- Recursos do ambiente Windows herdado da interface IPropertyFilter, Propriedade IndexColumn
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009318"
---
# <a name="ipropertyfilterindexcolumn-property"></a>Propriedade IPropertyFilter:: IndexColumn

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Nome da coluna indexada da propriedade pela qual filtrar.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valor da propriedade

Define a propriedade da coluna.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





