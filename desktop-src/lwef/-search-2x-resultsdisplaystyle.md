---
title: Enumeração ResultsDisplayStyle
description: Usado por IResultsViewer Resultstyle para definir ou determinar como os resultados são exibidos.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- recursos de ambiente Windows de enumeração herdados do ResultsDisplayStyle
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a045765b53f29e978c286a14a1d82b86ffb21b5046dee606029a957ee0434c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726517"
---
# <a name="resultsdisplaystyle-enumeration"></a>Enumeração ResultsDisplayStyle

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

Usado por [**IResultsViewer:: resultstyle**](-search-2x-iresultsviewer-resultsstyle.md) para definir ou determinar como os resultados são exibidos.

## <a name="syntax"></a>Syntax


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**
</dt> <dd>

Indica que os resultados são exibidos como ícones pequenos.

</dd> <dt>

<span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**
</dt> <dd>

Indica que os resultados são exibidos como ícones grandes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| INSERI<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





