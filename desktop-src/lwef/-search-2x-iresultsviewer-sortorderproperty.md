---
title: Propriedade IResultsViewer SortOrderProperty (WdsView.h)
description: Essa propriedade definirá ou retornará a ordem das colunas para classificar os resultados por.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Recursos do ambiente Windows herdado da propriedade SortOrderproperty
- Propriedade SortOrderproperty recursos de ambiente herdados do Windows, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, Propriedade SortOrderproperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa36dba99afbee58b480e17f241cb32f75cd5dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779570"
---
# <a name="iresultsviewersortorderproperty-property"></a>Propriedade IResultsViewer:: SortOrderproperty

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Essa propriedade definirá ou retornará a ordem das colunas para classificar os resultados por.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a>Valor da propriedade

Define a propriedade [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                        |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





