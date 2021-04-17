---
title: Enumeração ResultsDisplayStyle
description: Usado por IResultsViewer Resultstyle para definir ou determinar como os resultados são exibidos.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- Recursos do ambiente Windows herdado de enumeração ResultsDisplayStyle
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
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811505"
---
# <a name="resultsdisplaystyle-enumeration"></a>Enumeração ResultsDisplayStyle

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

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



 

 





