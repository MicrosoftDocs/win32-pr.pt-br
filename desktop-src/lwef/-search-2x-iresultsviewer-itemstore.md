---
title: Propriedade IResultsViewer do repositório de chaves (WdsView. h)
description: Essa propriedade definirá ou retornará o nome do repositório para filtrar os resultados por.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- recursos de ambiente herdado de Windows da propriedade itemproperty store
- recursos de ambiente herdado Windows da propriedade itemproperty store, interface IResultsViewer
- IResultsViewer interface herdada Windows recursos de ambiente, propriedade itemproperty
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21db485f8bfeb52ac413a2886f5624345e9812f2a0086b143f9a10942f7aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753897"
---
# <a name="iresultsvieweritemstore-property"></a>Propriedade IResultsViewer:: ItemProperty

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

Essa propriedade definirá ou retornará o nome do repositório para filtrar os resultados por.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor da propriedade

Define os nomes do repositório.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com \[ aplicativos de área de trabalho do SP1\]<br/>                        |
| Redistribuível<br/>          | Windows Pesquisador de desktops (WDS) 2.6.5<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





