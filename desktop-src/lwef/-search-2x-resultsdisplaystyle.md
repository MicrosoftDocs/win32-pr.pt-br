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
# <a name="resultsdisplaystyle-enumeration"></a><span data-ttu-id="a1cf3-104">Enumeração ResultsDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="a1cf3-104">ResultsDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="a1cf3-105">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a1cf3-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a1cf3-106">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a1cf3-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a1cf3-107">Usado por [**IResultsViewer:: resultstyle**](-search-2x-iresultsviewer-resultsstyle.md) para definir ou determinar como os resultados são exibidos.</span><span class="sxs-lookup"><span data-stu-id="a1cf3-107">Used by [**IResultsViewer::ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) to set or determine how results are displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1cf3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1cf3-108">Syntax</span></span>


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="a1cf3-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="a1cf3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a1cf3-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span><span class="sxs-lookup"><span data-stu-id="a1cf3-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="a1cf3-111">Indica que os resultados são exibidos como ícones pequenos.</span><span class="sxs-lookup"><span data-stu-id="a1cf3-111">Indicates Results are displayed as small icons.</span></span>

</dd> <dt>

<span data-ttu-id="a1cf3-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span><span class="sxs-lookup"><span data-stu-id="a1cf3-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="a1cf3-113">Indica que os resultados são exibidos como ícones grandes.</span><span class="sxs-lookup"><span data-stu-id="a1cf3-113">Indicates Results are displayed as large icons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1cf3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1cf3-114">Requirements</span></span>



| <span data-ttu-id="a1cf3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1cf3-115">Requirement</span></span> | <span data-ttu-id="a1cf3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a1cf3-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1cf3-117">INSERI</span><span class="sxs-lookup"><span data-stu-id="a1cf3-117">IDL</span></span><br/> | <dl> <span data-ttu-id="a1cf3-118"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a1cf3-118"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





