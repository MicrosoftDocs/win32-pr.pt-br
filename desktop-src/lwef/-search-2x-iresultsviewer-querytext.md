---
title: Propriedade IResultsViewer QueryText (WdsView. h)
description: Obtém ou define o texto da consulta atual.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- recursos de ambiente herdado Windows da propriedade QueryText
- propriedade QueryText recursos de ambiente herdados Windows, interface IResultsViewer
- recursos de ambiente Windows da interface IResultsViewer herdada, propriedade QueryText
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5522419d14bf27a1e836c9caa16e9dabf5a122e4566fd19c868a1f72e3f61d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753581"
---
# <a name="iresultsviewerquerytext-property"></a>Propriedade IResultsViewer:: QueryText

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

Obtém ou define o texto da consulta atual.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a>Valor da propriedade

Define o texto da consulta atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com \[ aplicativos de área de trabalho do SP1\]<br/>                        |
| Redistribuível<br/>          | Windows Pesquisador de desktops (WDS) 2.6.5<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





