---
title: Propriedade IResultsViewer HeaderStyle (WdsView. h)
description: O estilo do cabeçalho exibido na exibição.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- Recursos do ambiente Windows herdado da propriedade HeaderStyle
- Propriedade HeaderStyle recursos de ambiente do Windows herdados, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, propriedade HeaderStyle
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc4d0ad56e1303914af712e2a9b6fa0fd416785
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644673"
---
# <a name="iresultsviewerheaderstyle-property"></a>Propriedade IResultsViewer:: HeaderStyle

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

O estilo do cabeçalho exibido na exibição.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a>Valor da propriedade

Define o estilo do cabeçalho exibido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                        |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





