---
title: Enumeração ViewContents
description: Usado pelo conteúdo do IResultsViewer para indicar ou definir como o conjunto de retorno da consulta atual é exibido.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- recursos de ambiente Windows de enumeração herdados do ViewContents
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2070b68ec62a8dd6ca86758b98a6399ee41180eaad24613d17d0825a927b1871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829106"
---
# <a name="viewcontents-enumeration"></a>Enumeração ViewContents

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

Usado por [**IResultsViewer:: Contents**](-search-2x-iresultsviewer-contents.md) para indicar ou definir como o conjunto de retorno da consulta atual é exibido.

## <a name="syntax"></a>Syntax


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**
</dt> <dd>

Indica o tipo de conteúdo que está sendo exibido no modo de exibição de resultados.

</dd> <dt>

<span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**
</dt> <dd>

Indica que o tipo de conteúdo que está sendo exibido na exibição de resultados está definido atualmente como a exibição do Shell.

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**
</dt> <dd>

Indica que o tipo de conteúdo que está sendo exibido na exibição de resultados está definido atualmente como a exibição do navegador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| INSERI<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





