---
title: Enumeração ViewContents
description: Usado pelo conteúdo do IResultsViewer para indicar ou definir como o conjunto de retorno da consulta atual é exibido.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Recursos do ambiente Windows herdado de enumeração ViewContents
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
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781416"
---
# <a name="viewcontents-enumeration"></a><span data-ttu-id="1f4d3-104">Enumeração ViewContents</span><span class="sxs-lookup"><span data-stu-id="1f4d3-104">ViewContents enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="1f4d3-105">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1f4d3-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="1f4d3-106">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1f4d3-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="1f4d3-107">Usado por [**IResultsViewer:: Contents**](-search-2x-iresultsviewer-contents.md) para indicar ou definir como o conjunto de retorno da consulta atual é exibido.</span><span class="sxs-lookup"><span data-stu-id="1f4d3-107">Used by [**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) to indicate or set how the current query return set is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f4d3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f4d3-108">Syntax</span></span>


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a><span data-ttu-id="1f4d3-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="1f4d3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1f4d3-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span><span class="sxs-lookup"><span data-stu-id="1f4d3-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="1f4d3-111">Indica o tipo de conteúdo que está sendo exibido no modo de exibição de resultados.</span><span class="sxs-lookup"><span data-stu-id="1f4d3-111">Indicates the type of contents being displayed in the results view.</span></span>

</dd> <dt>

<span data-ttu-id="1f4d3-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span><span class="sxs-lookup"><span data-stu-id="1f4d3-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="1f4d3-113">Indica que o tipo de conteúdo que está sendo exibido na exibição de resultados está definido atualmente como a exibição do Shell.</span><span class="sxs-lookup"><span data-stu-id="1f4d3-113">Indicates the type of contents being displayed in the results view is currently set to the Shell view.</span></span>

</dd> <dt>

<span data-ttu-id="1f4d3-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span><span class="sxs-lookup"><span data-stu-id="1f4d3-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="1f4d3-115">Indica que o tipo de conteúdo que está sendo exibido na exibição de resultados está definido atualmente como a exibição do navegador.</span><span class="sxs-lookup"><span data-stu-id="1f4d3-115">Indicates the type of contents being displayed in the results view is currently set to the browser view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f4d3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f4d3-116">Requirements</span></span>



| <span data-ttu-id="1f4d3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f4d3-117">Requirement</span></span> | <span data-ttu-id="1f4d3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1f4d3-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f4d3-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="1f4d3-119">IDL</span></span><br/> | <dl> <span data-ttu-id="1f4d3-120"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f4d3-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





