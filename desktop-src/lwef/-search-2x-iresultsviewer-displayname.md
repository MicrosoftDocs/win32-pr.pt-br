---
title: Propriedade DisplayName IResultsViewer (WdsView. h)
description: Nome de exibição localizado do tipo.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- Propriedade DisplayName recursos de ambiente do Windows herdados
- Propriedade DisplayName recursos de ambiente do Windows herdados, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, Propriedade DisplayName
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5ba65729fb238dbed57b71d893a9814c8ac8f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761061"
---
# <a name="iresultsviewerdisplayname-property"></a>IResultsViewer::D Propriedade isplayname

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Nome de exibição localizado do tipo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor da propriedade

Ponteiro para um valor que recebe o nome de exibição localizado para o tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                        |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





