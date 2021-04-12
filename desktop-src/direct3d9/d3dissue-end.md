---
description: Essa macro cria um valor usado pelo problema para emitir uma extremidade de consulta.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298666"
---
# <a name="d3dissue_end"></a><span data-ttu-id="5fabc-103">D3DISSUE \_ fim</span><span class="sxs-lookup"><span data-stu-id="5fabc-103">D3DISSUE\_END</span></span>

<span data-ttu-id="5fabc-104">Essa macro cria um valor usado pelo [**problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) para emitir uma extremidade de consulta.</span><span class="sxs-lookup"><span data-stu-id="5fabc-104">This macro creates a value used by [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) to issue a query end.</span></span>

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a><span data-ttu-id="5fabc-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fabc-105">Parameters</span></span>





 

## <a name="remarks"></a><span data-ttu-id="5fabc-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fabc-106">Remarks</span></span>

<span data-ttu-id="5fabc-107">Essa macro altera o estado da consulta para não sinalizado.</span><span class="sxs-lookup"><span data-stu-id="5fabc-107">This macro changes the query state to nonsignaled.</span></span>

<span data-ttu-id="5fabc-108">\_O D3DISSUE end é válido para os seguintes tipos de consulta.</span><span class="sxs-lookup"><span data-stu-id="5fabc-108">D3DISSUE\_END is valid for the following query types.</span></span>

-   <span data-ttu-id="5fabc-109">D3DQUERYTYPE \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="5fabc-109">D3DQUERYTYPE\_VCACHE</span></span>
-   <span data-ttu-id="5fabc-110">\_RESOURCEMANAGER D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="5fabc-110">D3DQUERYTYPE\_ResourceManager</span></span>
-   <span data-ttu-id="5fabc-111">D3DQUERYTYPE \_ VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="5fabc-111">D3DQUERYTYPE\_VERTEXSTATS</span></span>
-   <span data-ttu-id="5fabc-112">\_Evento D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="5fabc-112">D3DQUERYTYPE\_EVENT</span></span>
-   <span data-ttu-id="5fabc-113">D3DQUERYTYPE \_ oclusão</span><span class="sxs-lookup"><span data-stu-id="5fabc-113">D3DQUERYTYPE\_OCCLUSION</span></span>

## <a name="requirements"></a><span data-ttu-id="5fabc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fabc-114">Requirements</span></span>



| <span data-ttu-id="5fabc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fabc-115">Requirement</span></span> | <span data-ttu-id="5fabc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5fabc-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fabc-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fabc-117">Header</span></span><br/> | <dl> <span data-ttu-id="5fabc-118"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fabc-118"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fabc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fabc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fabc-120">Macros</span><span class="sxs-lookup"><span data-stu-id="5fabc-120">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="5fabc-121">**Início do D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5fabc-121">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md)
</dt> <dt>

[<span data-ttu-id="5fabc-122">**D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="5fabc-122">**D3DQUERYTYPE**</span></span>](./d3dquerytype.md)
</dt> </dl>

 

 
