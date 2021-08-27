---
title: Propriedade DisplayName IResultsViewer (WdsView. h)
description: Nome de exibição localizado do tipo.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- recursos de ambiente herdado de Windows da propriedade DisplayName
- propriedade DisplayName herdada Windows recursos de ambiente, interface IResultsViewer
- IResultsViewer interface herdada Windows recursos de ambiente, propriedade DisplayName
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
ms.openlocfilehash: 98d3f0c5f7887861d2d757c71a4327ce57af7f39ae3f4811167789c6b4e662ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754391"
---
# <a name="iresultsviewerdisplayname-property"></a>IResultsViewer::D Propriedade isplayname

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

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
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com \[ aplicativos de área de trabalho do SP1\]<br/>                        |
| Redistribuível<br/>          | Windows Pesquisador de desktops (WDS) 2.6.5<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





