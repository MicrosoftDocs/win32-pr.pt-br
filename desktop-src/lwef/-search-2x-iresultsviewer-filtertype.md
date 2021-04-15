---
title: Propriedade FilterType IResultsViewer (WdsView. h)
description: Essa propriedade definirá ou retornará o nome do tipo preceived para filtrar os resultados por.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- Propriedade FilterType recursos de ambiente herdados do Windows
- Propriedade FilterType recursos de ambiente herdados do Windows, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, Propriedade FilterType
topic_type:
- apiref
api_name:
- IResultsViewer.FilterType
- IResultsViewer.get_FilterType
- IResultsViewer.put_FilterType
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890d0ceadddb9f3b46ee8b45f109a389472be218
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761253"
---
# <a name="iresultsviewerfiltertype-property"></a>Propriedade IResultsViewer:: FilterType

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Essa propriedade definirá ou retornará o nome do tipo preceived para filtrar os resultados por.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_FilterType(
  [in]          BSTR name
);

HRESULT get_FilterType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor da propriedade

Define o tipo percebido usado para filtrar os resultados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                        |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





