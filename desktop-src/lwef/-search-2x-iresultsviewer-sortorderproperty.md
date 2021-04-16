---
title: Propriedade IResultsViewer SortOrderProperty (WdsView.h)
description: Essa propriedade definirá ou retornará a ordem das colunas para classificar os resultados por.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Recursos do ambiente Windows herdado da propriedade SortOrderproperty
- Propriedade SortOrderproperty recursos de ambiente herdados do Windows, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, Propriedade SortOrderproperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa36dba99afbee58b480e17f241cb32f75cd5dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779570"
---
# <a name="iresultsviewersortorderproperty-property"></a><span data-ttu-id="4352a-106">Propriedade IResultsViewer:: SortOrderproperty</span><span class="sxs-lookup"><span data-stu-id="4352a-106">IResultsViewer::SortOrderProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="4352a-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4352a-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4352a-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4352a-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="4352a-109">Essa propriedade definirá ou retornará a ordem das colunas para classificar os resultados por.</span><span class="sxs-lookup"><span data-stu-id="4352a-109">This property will set or return the order of columns to sort results by.</span></span>

<span data-ttu-id="4352a-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4352a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4352a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4352a-111">Syntax</span></span>


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a><span data-ttu-id="4352a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4352a-112">Property value</span></span>

<span data-ttu-id="4352a-113">Define a propriedade [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) .</span><span class="sxs-lookup"><span data-stu-id="4352a-113">Sets the [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4352a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4352a-114">Requirements</span></span>



| <span data-ttu-id="4352a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4352a-115">Requirement</span></span> | <span data-ttu-id="4352a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4352a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4352a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4352a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4352a-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="4352a-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4352a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4352a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4352a-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="4352a-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="4352a-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4352a-121">Redistributable</span></span><br/>          | <span data-ttu-id="4352a-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="4352a-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="4352a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4352a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4352a-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="4352a-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





