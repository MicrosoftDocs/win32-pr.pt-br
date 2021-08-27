---
title: Propriedade FilterType IResultsViewer (WdsView. h)
description: Essa propriedade definirá ou retornará o nome do tipo preceived para filtrar os resultados por.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- propriedades herdadas Windows ambiente da propriedade filtertype
- propriedade filtertype herdada Windows recursos de ambiente, interface IResultsViewer
- IResultsViewer interface herdada Windows recursos de ambiente, propriedade filtertype
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
ms.openlocfilehash: b8f4e71a469ad68431721d99343b43b28ea0f0a82b7e393f5c402b0d88735db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754302"
---
# <a name="iresultsviewerfiltertype-property"></a>Propriedade IResultsViewer:: FilterType

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

Essa propriedade definirá ou retornará o nome do tipo preceived para filtrar os resultados por.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


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
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com \[ aplicativos de área de trabalho do SP1\]<br/>                        |
| Redistribuível<br/>          | Windows Pesquisador de desktops (WDS) 2.6.5<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





