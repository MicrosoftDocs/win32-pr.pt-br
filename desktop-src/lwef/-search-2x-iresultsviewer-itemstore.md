---
title: Propriedade IResultsViewer do repositório de chaves (WdsView. h)
description: Essa propriedade definirá ou retornará o nome do repositório para filtrar os resultados por.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- Recursos de ambiente herdado do Windows da propriedade ItemProperty Store
- Recursos do ambiente Windows herdado da propriedade ItemProperty Store, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, Propriedade ItemProperty
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
ms.openlocfilehash: 99abd4ef7ee36a0c76efa391d98a9fdb1d75f34e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455076"
---
# <a name="iresultsvieweritemstore-property"></a><span data-ttu-id="03038-106">Propriedade IResultsViewer:: ItemProperty</span><span class="sxs-lookup"><span data-stu-id="03038-106">IResultsViewer::ItemStore property</span></span>

> [!NOTE]
> <span data-ttu-id="03038-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="03038-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="03038-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="03038-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="03038-109">Essa propriedade definirá ou retornará o nome do repositório para filtrar os resultados por.</span><span class="sxs-lookup"><span data-stu-id="03038-109">This property will set or return the name of the store to filter results by.</span></span>

<span data-ttu-id="03038-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="03038-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="03038-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="03038-111">Syntax</span></span>


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="03038-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="03038-112">Property value</span></span>

<span data-ttu-id="03038-113">Define os nomes do repositório.</span><span class="sxs-lookup"><span data-stu-id="03038-113">Sets the names of the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="03038-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03038-114">Requirements</span></span>



| <span data-ttu-id="03038-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="03038-115">Requirement</span></span> | <span data-ttu-id="03038-116">Valor</span><span class="sxs-lookup"><span data-stu-id="03038-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="03038-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03038-117">Minimum supported client</span></span><br/> | <span data-ttu-id="03038-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="03038-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="03038-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03038-119">Minimum supported server</span></span><br/> | <span data-ttu-id="03038-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="03038-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="03038-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="03038-121">Redistributable</span></span><br/>          | <span data-ttu-id="03038-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="03038-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="03038-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03038-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="03038-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="03038-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





