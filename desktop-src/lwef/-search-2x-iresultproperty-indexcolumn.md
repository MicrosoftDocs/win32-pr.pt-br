---
title: Propriedade IResultProperty IndexColumn (WdsSharedIDL. h)
description: Nome da coluna de propriedades no índice.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- recursos de ambiente herdado Windows da propriedade IndexColumn
- propriedade IndexColumn recursos de ambiente herdados Windows, interface IResultProperty
- recursos de ambiente Windows da interface IResultProperty herdada, propriedade IndexColumn
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a78d91b9e823dbf8d3c7a2273247706f9ae2bb04c6f64d08f5555eb875023c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754769"
---
# <a name="iresultpropertyindexcolumn-property"></a>Propriedade IResultProperty:: IndexColumn

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

Nome da coluna de propriedades no índice.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valor da propriedade

Retorna um ponteiro para o nome da coluna no índice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com \[ aplicativos de área de trabalho do SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisador de desktops (WDS) 2.6.5<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





