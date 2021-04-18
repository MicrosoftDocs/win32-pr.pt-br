---
description: Observe que essa interface foi preterida.
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
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759125"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="6328f-103">Interface IAMFilterData</span><span class="sxs-lookup"><span data-stu-id="6328f-103">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="6328f-104">Essa interface foi substituída.</span><span class="sxs-lookup"><span data-stu-id="6328f-104">This interface has been deprecated.</span></span> <span data-ttu-id="6328f-105">Os novos aplicativos devem usar a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6328f-105">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="6328f-106">A `IAMFilterData` interface converte informações de filtro em dados binários empacotados, que podem ser armazenados no registro.</span><span class="sxs-lookup"><span data-stu-id="6328f-106">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="6328f-107">O objeto mapeador de filtro expõe essa interface.</span><span class="sxs-lookup"><span data-stu-id="6328f-107">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="6328f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6328f-108">Members</span></span>

<span data-ttu-id="6328f-109">A interface **IAMFilterData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6328f-109">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6328f-110">**IAMFilterData** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6328f-110">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="6328f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6328f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6328f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6328f-112">Methods</span></span>

<span data-ttu-id="6328f-113">A interface **IAMFilterData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6328f-113">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="6328f-114">Método</span><span class="sxs-lookup"><span data-stu-id="6328f-114">Method</span></span>                                                     | <span data-ttu-id="6328f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6328f-115">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="6328f-116">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="6328f-116">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="6328f-117">Cria dados de registro binários para um filtro.</span><span class="sxs-lookup"><span data-stu-id="6328f-117">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="6328f-118">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="6328f-118">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="6328f-119">Desempacota os dados de registro binários de um filtro.</span><span class="sxs-lookup"><span data-stu-id="6328f-119">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6328f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6328f-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6328f-121">O cabeçalho Fil \_ Data. h está localizado no diretório de [exemplo do mapeador](mapper-sample.md) no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="6328f-121">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6328f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6328f-122">Requirements</span></span>



| <span data-ttu-id="6328f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6328f-123">Requirement</span></span> | <span data-ttu-id="6328f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6328f-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6328f-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6328f-125">Header</span></span><br/> | <dl> <span data-ttu-id="6328f-126"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="6328f-126"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6328f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6328f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6328f-128">Interfaces preteridas</span><span class="sxs-lookup"><span data-stu-id="6328f-128">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
