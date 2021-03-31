---
title: CENUMOBJ. CPP
description: No componente de provedor de exemplo, a enumeração de um objeto de contêiner usa as rotinas, de cenumobj. cpp, listadas na tabela a seguir.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641823"
---
# <a name="cenumobjcpp"></a><span data-ttu-id="a4c13-103">CENUMOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="a4c13-103">CENUMOBJ.CPP</span></span>

<span data-ttu-id="a4c13-104">No componente de provedor de exemplo, a enumeração de um objeto de contêiner usa as rotinas, de cenumobj. cpp, listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4c13-104">In the example provider component, the enumeration of a container object uses the routines, from cenumobj.cpp, listed in the following table.</span></span>



| <span data-ttu-id="a4c13-105">Método</span><span class="sxs-lookup"><span data-stu-id="a4c13-105">Method</span></span>                                                 | <span data-ttu-id="a4c13-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4c13-106">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c13-107">**CSampleDSGenObjectEnum:: criar**</span><span class="sxs-lookup"><span data-stu-id="a4c13-107">**CSampleDSGenObjectEnum::Create**</span></span>                     | <span data-ttu-id="a4c13-108">Crie um objeto para habilitar a enumeração de objetos Active Directory genéricos.</span><span class="sxs-lookup"><span data-stu-id="a4c13-108">Create an object to enable enumeration of generic Active Directory objects.</span></span>                                                                                           |
| <span data-ttu-id="a4c13-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span><span class="sxs-lookup"><span data-stu-id="a4c13-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span></span>     | <span data-ttu-id="a4c13-110">Inicialização.</span><span class="sxs-lookup"><span data-stu-id="a4c13-110">Initialization.</span></span>                                                                                                                                                       |
| <span data-ttu-id="a4c13-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="a4c13-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="a4c13-112">Gerenciar a recuperação de objetos.</span><span class="sxs-lookup"><span data-stu-id="a4c13-112">Manage retrieval of objects.</span></span>                                                                                                                                          |
| <span data-ttu-id="a4c13-113">**CSampleDSGenObjectEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="a4c13-113">**CSampleDSGenObjectEnum::FetchObjects**</span></span>               | <span data-ttu-id="a4c13-114">Recupere o conjunto de ponteiros [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que correspondem ao filtro.</span><span class="sxs-lookup"><span data-stu-id="a4c13-114">Retrieve the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers that match the filter.</span></span>                                                             |
| <span data-ttu-id="a4c13-115">**CSampleDSGenObjectEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="a4c13-115">**CSampleDSGenObjectEnum::FetchNextObject**</span></span>            | <span data-ttu-id="a4c13-116">Recuperar um objeto e fazer a correspondência com o filtro.</span><span class="sxs-lookup"><span data-stu-id="a4c13-116">Retrieve an object and match against the filter.</span></span> <span data-ttu-id="a4c13-117">Se corresponder, empacote-o em objeto genérico e retorne um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a4c13-117">If it matches, wrap it in generic object and return a [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |
| <span data-ttu-id="a4c13-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="a4c13-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="a4c13-119">Gerenciar a recuperação de objetos.</span><span class="sxs-lookup"><span data-stu-id="a4c13-119">Manage retrieving the objects.</span></span>                                                                                                                                        |
| <span data-ttu-id="a4c13-120">**CSampleDSGenObjectEnum:: Next**</span><span class="sxs-lookup"><span data-stu-id="a4c13-120">**CSampleDSGenObjectEnum::Next**</span></span>                       | <span data-ttu-id="a4c13-121">Recupera o número especificado de elementos do objeto de enumeração indicado.</span><span class="sxs-lookup"><span data-stu-id="a4c13-121">Retrieve the specified number of elements from the enumeration object indicated.</span></span>                                                                                      |
| <span data-ttu-id="a4c13-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span><span class="sxs-lookup"><span data-stu-id="a4c13-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span></span>            | <span data-ttu-id="a4c13-123">Verifique se a classe de objeto corresponde a uma na lista de filtros.</span><span class="sxs-lookup"><span data-stu-id="a4c13-123">Verify that object class matches one in the filter list.</span></span>                                                                                                              |
| <span data-ttu-id="a4c13-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span><span class="sxs-lookup"><span data-stu-id="a4c13-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span></span>         | <span data-ttu-id="a4c13-125">Gerenciar a matriz de filtros.</span><span class="sxs-lookup"><span data-stu-id="a4c13-125">Manage the filter array.</span></span>                                                                                                                                              |
| <span data-ttu-id="a4c13-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span><span class="sxs-lookup"><span data-stu-id="a4c13-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span></span> | <span data-ttu-id="a4c13-127">Adicione uma nova classe de objeto ao filtro e defina o filtro como contíguo.</span><span class="sxs-lookup"><span data-stu-id="a4c13-127">Add a new object class to the filter and set the filter as contiguous.</span></span>                                                                                                |
| <span data-ttu-id="a4c13-128">**FreeFilterList**</span><span class="sxs-lookup"><span data-stu-id="a4c13-128">**FreeFilterList**</span></span>                                     | <span data-ttu-id="a4c13-129">Libere o filtro.</span><span class="sxs-lookup"><span data-stu-id="a4c13-129">Free the filter.</span></span>                                                                                                                                                      |



 

 

 