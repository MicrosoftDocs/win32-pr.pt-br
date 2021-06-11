---
description: Saiba mais sobre a interface IAMFilterData, que converte informações de filtro em dados binários empacotados. Essa interface foi substituída.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interface IAMFilterData (Fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1e43e0f16ddfdee596f0dc6bd736ed86fc6fa37d
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989431"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="2236c-104">Interface IAMFilterData</span><span class="sxs-lookup"><span data-stu-id="2236c-104">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="2236c-105">Essa interface foi substituída.</span><span class="sxs-lookup"><span data-stu-id="2236c-105">This interface has been deprecated.</span></span> <span data-ttu-id="2236c-106">Os novos aplicativos devem usar a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2236c-106">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="2236c-107">A `IAMFilterData` interface converte informações de filtro em dados binários empacotados, que podem ser armazenados no registro.</span><span class="sxs-lookup"><span data-stu-id="2236c-107">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="2236c-108">O objeto mapeador de filtro expõe essa interface.</span><span class="sxs-lookup"><span data-stu-id="2236c-108">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="2236c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="2236c-109">Members</span></span>

<span data-ttu-id="2236c-110">A interface **IAMFilterData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2236c-110">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2236c-111">**IAMFilterData** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2236c-111">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="2236c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2236c-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2236c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2236c-113">Methods</span></span>

<span data-ttu-id="2236c-114">A interface **IAMFilterData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2236c-114">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="2236c-115">Método</span><span class="sxs-lookup"><span data-stu-id="2236c-115">Method</span></span>                                                     | <span data-ttu-id="2236c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2236c-116">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="2236c-117">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="2236c-117">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="2236c-118">Cria dados de registro binários para um filtro.</span><span class="sxs-lookup"><span data-stu-id="2236c-118">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="2236c-119">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="2236c-119">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="2236c-120">Desempacota os dados de registro binários de um filtro.</span><span class="sxs-lookup"><span data-stu-id="2236c-120">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2236c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2236c-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2236c-122">O cabeçalho Fil \_ Data. h está localizado no diretório de [exemplo do mapeador](mapper-sample.md) no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2236c-122">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2236c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2236c-123">Requirements</span></span>



| <span data-ttu-id="2236c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2236c-124">Requirement</span></span> | <span data-ttu-id="2236c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2236c-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2236c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2236c-126">Header</span></span><br/> | <dl> <span data-ttu-id="2236c-127"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="2236c-127"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2236c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2236c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2236c-129">Interfaces preteridas</span><span class="sxs-lookup"><span data-stu-id="2236c-129">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
