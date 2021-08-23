---
title: Propriedade SortProperty de IResultsViewer (WdsView.h)
description: Essa propriedade definirá ou retornará o IndexColumn da propriedade por onde classificar os resultados.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Propriedade SortProperty Herdou Windows Recursos de Ambiente
- Propriedade SortProperty Recursos Windows ambiente herdado, interface IResultsViewer
- Interface IResultsViewer Recursos Windows ambiente herdado, propriedade SortProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ab912dde6bdc87b2e9d05496f25de497b6fdc9c8fde4e65e3d2cb89549b1e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610926"
---
# <a name="iresultsviewersortproperty-property"></a>Propriedade IResultsViewer::SortProperty

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Essa propriedade definirá ou retornará o IndexColumn da propriedade por onde classificar os resultados.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valor da propriedade

Define a propriedade IndexColumn.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                        |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 2.6.5<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





