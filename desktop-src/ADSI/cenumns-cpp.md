---
title: CENUMNS. CPP
description: No componente de provedor de exemplo, a enumeração de um objeto de namespace usa os métodos, de cenumns. cpp, listados na tabela a seguir.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105749123"
---
# <a name="cenumnscpp"></a><span data-ttu-id="ac5fb-103">CENUMNS. CPP</span><span class="sxs-lookup"><span data-stu-id="ac5fb-103">CENUMNS.CPP</span></span>

<span data-ttu-id="ac5fb-104">No componente de provedor de exemplo, a enumeração de um objeto de namespace usa os métodos, de cenumns. cpp, listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac5fb-104">In the example provider component, the enumeration of a namespace object uses the methods, from cenumns.cpp, listed in the following table.</span></span>



| <span data-ttu-id="ac5fb-105">Método</span><span class="sxs-lookup"><span data-stu-id="ac5fb-105">Method</span></span>                                              | <span data-ttu-id="ac5fb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac5fb-106">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5fb-107">**CSampleDSNamespaceEnum:: criar**</span><span class="sxs-lookup"><span data-stu-id="ac5fb-107">**CSampleDSNamespaceEnum::Create**</span></span>                  | <span data-ttu-id="ac5fb-108">Crie um objeto para permitir a enumeração de um objeto de namespace do ADS.</span><span class="sxs-lookup"><span data-stu-id="ac5fb-108">Create an object to allow enumeration of an ADS namespace object.</span></span>                                                                                         |
| <span data-ttu-id="ac5fb-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="ac5fb-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span></span>  | <span data-ttu-id="ac5fb-110">Construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="ac5fb-110">Standard constructor.</span></span>                                                                                                                                     |
| <span data-ttu-id="ac5fb-111">**CSampleDSNamespaceEnum:: ~ CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="ac5fb-111">**CSampleDSNamespaceEnum::~CSampleDSNamespaceEnum**</span></span> | <span data-ttu-id="ac5fb-112">Destruidor padrão.</span><span class="sxs-lookup"><span data-stu-id="ac5fb-112">Standard destructor.</span></span>                                                                                                                                      |
| <span data-ttu-id="ac5fb-113">**CSampleDSNamespaceEnum:: Next**</span><span class="sxs-lookup"><span data-stu-id="ac5fb-113">**CSampleDSNamespaceEnum::Next**</span></span>                    | <span data-ttu-id="ac5fb-114">Recupera o número especificado de elementos do objeto namespace indicado.</span><span class="sxs-lookup"><span data-stu-id="ac5fb-114">Retrieve the specified number of elements from the namespace object indicated.</span></span>                                                                            |
| <span data-ttu-id="ac5fb-115">**CSampleDSNamespaceEnum::EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="ac5fb-115">**CSampleDSNamespaceEnum::EnumObjects**</span></span>             | <span data-ttu-id="ac5fb-116">Gerenciar a recuperação de ponteiros de interface para os objetos.</span><span class="sxs-lookup"><span data-stu-id="ac5fb-116">Manage retrieving the interface pointers to the objects.</span></span>                                                                                                  |
| <span data-ttu-id="ac5fb-117">**CSampleDSNamespaceEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="ac5fb-117">**CSampleDSNamespaceEnum::FetchObjects**</span></span>            | <span data-ttu-id="ac5fb-118">Busque o conjunto de ponteiros [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ac5fb-118">Fetch the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers.</span></span>                                                                          |
| <span data-ttu-id="ac5fb-119">**CSampleDSNamespaceEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="ac5fb-119">**CSampleDSNamespaceEnum::FetchNextObject**</span></span>         | <span data-ttu-id="ac5fb-120">Busque o próximo objeto.</span><span class="sxs-lookup"><span data-stu-id="ac5fb-120">Fetch the next object.</span></span> <span data-ttu-id="ac5fb-121">Se for encontrado, crie um objeto Active Directory genérico e recupere seu ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ac5fb-121">If found, create a generic Active Directory object and retrieve its [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |



 

 

 