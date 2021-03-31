---
title: CENUMSCH. CPP
description: No componente de provedor de exemplo, a enumeração de um objeto de esquema usa os métodos, de cenumsch. cpp, listados na tabela a seguir.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822232"
---
# <a name="cenumschcpp"></a><span data-ttu-id="6b23c-103">CENUMSCH. CPP</span><span class="sxs-lookup"><span data-stu-id="6b23c-103">CENUMSCH.CPP</span></span>

<span data-ttu-id="6b23c-104">No componente de provedor de exemplo, a enumeração de um objeto de esquema usa os métodos, de cenumsch. cpp, listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6b23c-104">In the example provider component, the enumeration of a schema object uses the methods, from cenumsch.cpp, listed in the following table.</span></span>



| <span data-ttu-id="6b23c-105">Método</span><span class="sxs-lookup"><span data-stu-id="6b23c-105">Method</span></span>                                        | <span data-ttu-id="6b23c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b23c-106">Description</span></span>                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b23c-107">**CSampleDSSchemaEnum:: criar**</span><span class="sxs-lookup"><span data-stu-id="6b23c-107">**CSampleDSSchemaEnum::Create**</span></span>               | <span data-ttu-id="6b23c-108">Crie um objeto para permitir a enumeração de um objeto de classe de esquema ADSI.</span><span class="sxs-lookup"><span data-stu-id="6b23c-108">Create an object to allow enumeration of an ADSI schema class object.</span></span>                                                |
| <span data-ttu-id="6b23c-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="6b23c-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span></span>  | <span data-ttu-id="6b23c-110">Construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="6b23c-110">Standard constructor.</span></span>                                                                                                |
| <span data-ttu-id="6b23c-111">**CSampleDSSchemaEnum:: ~ CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="6b23c-111">**CSampleDSSchemaEnum::~CSampleDSSchemaEnum**</span></span> | <span data-ttu-id="6b23c-112">Destruidor padrão.</span><span class="sxs-lookup"><span data-stu-id="6b23c-112">Standard destructor.</span></span>                                                                                                 |
| <span data-ttu-id="6b23c-113">**CSampleDSSchemaEnum:: Next**</span><span class="sxs-lookup"><span data-stu-id="6b23c-113">**CSampleDSSchemaEnum::Next**</span></span>                 | <span data-ttu-id="6b23c-114">Recupera o número especificado de elementos do objeto de esquema indicado.</span><span class="sxs-lookup"><span data-stu-id="6b23c-114">Retrieve the specified number of elements from the schema object indicated.</span></span>                                          |
| <span data-ttu-id="6b23c-115">**CSampleDSSchemaEnum::EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="6b23c-115">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="6b23c-116">Gerenciar a recuperação de ponteiros de interfaces para os objetos do tipo de objeto indicado.</span><span class="sxs-lookup"><span data-stu-id="6b23c-116">Manage retrieving the interfaces pointers to the objects of the object type indicated.</span></span>                               |
| <span data-ttu-id="6b23c-117">**CSampleDSSchemaEnum::EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="6b23c-117">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="6b23c-118">Gerenciar a recuperação de ponteiros de interface para os objetos do tipo de objeto padrão.</span><span class="sxs-lookup"><span data-stu-id="6b23c-118">Manage retrieving the interface pointers to the objects of the default object type.</span></span>                                  |
| <span data-ttu-id="6b23c-119">**CSampleDSSchemaEnum::EnumClasses**</span><span class="sxs-lookup"><span data-stu-id="6b23c-119">**CSampleDSSchemaEnum::EnumClasses**</span></span>          | <span data-ttu-id="6b23c-120">Gerenciar a recuperação de ponteiros de interface somente para os objetos de classe de esquema contidos neste objeto.</span><span class="sxs-lookup"><span data-stu-id="6b23c-120">Manage retrieving the interface pointers to only the schema class objects contained in this object.</span></span>                  |
| <span data-ttu-id="6b23c-121">**CSampleDSSchemaEnum:: GetClassObject**</span><span class="sxs-lookup"><span data-stu-id="6b23c-121">**CSampleDSSchemaEnum::GetClassObject**</span></span>       | <span data-ttu-id="6b23c-122">Recuperar a próxima definição de classe de esquema; Se for encontrado, crie um objeto de classe de esquema e retorne o ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="6b23c-122">Retrieve the next schema class definition; if found, create a schema class object, and return the interface pointer.</span></span> |
| <span data-ttu-id="6b23c-123">**CSampleDSSchemaEnum:: EnumProperties**</span><span class="sxs-lookup"><span data-stu-id="6b23c-123">**CSampleDSSchemaEnum::EnumProperties**</span></span>       | <span data-ttu-id="6b23c-124">Gerenciar a recuperação de ponteiros de interface para os objetos de propriedade contidos somente neste objeto.</span><span class="sxs-lookup"><span data-stu-id="6b23c-124">Manage retrieving the interface pointers to the property objects only contained in this object.</span></span>                      |
| <span data-ttu-id="6b23c-125">**CSampleDSSchemaEnum:: GetPropertyObject**</span><span class="sxs-lookup"><span data-stu-id="6b23c-125">**CSampleDSSchemaEnum::GetPropertyObject**</span></span>    | <span data-ttu-id="6b23c-126">Recuperar a próxima definição de propriedade; Se for encontrado, crie um objeto de classe de esquema e retorne o ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="6b23c-126">Retrieve the next property definition; if found, create a schema class object, and return the interface pointer.</span></span>     |
| <span data-ttu-id="6b23c-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span><span class="sxs-lookup"><span data-stu-id="6b23c-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span></span>         | <span data-ttu-id="6b23c-128">Gerenciar a recuperação de ponteiros de interface para os objetos de sintaxe contidos somente neste objeto.</span><span class="sxs-lookup"><span data-stu-id="6b23c-128">Manage retrieving the interface pointers to the syntax objects only contained in this object.</span></span>                        |
| <span data-ttu-id="6b23c-129">**CSampleDSSchemaEnum:: getsyntaxobject**</span><span class="sxs-lookup"><span data-stu-id="6b23c-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span></span>      | <span data-ttu-id="6b23c-130">Recuperar a próxima definição de sintaxe; Se for encontrado, crie um objeto de classe de esquema e retorne o ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="6b23c-130">Retrieve the next syntax definition; if found, create a schema class object, and return the interface pointer.</span></span>       |



 

 

 




