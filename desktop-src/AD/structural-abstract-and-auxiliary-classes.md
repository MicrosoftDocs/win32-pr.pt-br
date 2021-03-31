---
title: Classes estruturais, abstratas e auxiliares
description: O atributo objectClassCategory de um objeto classSchema pode ter um valor, conforme listado na tabela a seguir, que indica se a classe é estrutural, abstrata ou auxiliar.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- AD de classes estruturais, abstratas e auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004894"
---
# <a name="structural-abstract-and-auxiliary-classes"></a><span data-ttu-id="fda90-104">Classes estruturais, abstratas e auxiliares</span><span class="sxs-lookup"><span data-stu-id="fda90-104">Structural, Abstract, and Auxiliary Classes</span></span>

<span data-ttu-id="fda90-105">O atributo **objectClassCategory** de um objeto **classSchema** pode ter um valor, conforme listado na tabela a seguir, que indica se a classe é estrutural, abstrata ou auxiliar.</span><span class="sxs-lookup"><span data-stu-id="fda90-105">The **objectClassCategory** attribute of a **classSchema** object can have a value, as listed in the following table, that indicates whether the class is structural, abstract, or auxiliary.</span></span>



| <span data-ttu-id="fda90-106">Valor</span><span class="sxs-lookup"><span data-stu-id="fda90-106">Value</span></span> | <span data-ttu-id="fda90-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fda90-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fda90-108">1</span><span class="sxs-lookup"><span data-stu-id="fda90-108">1</span></span>     | <span data-ttu-id="fda90-109">Uma classe estrutural, que é o único tipo de classe que pode ter instâncias em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="fda90-109">A structural class, which is the only type of class that can have instances in Active Directory Domain Services.</span></span> <span data-ttu-id="fda90-110">Uma classe estrutural pode ser uma subclasse de uma classe abstrata ou estrutural.</span><span class="sxs-lookup"><span data-stu-id="fda90-110">A structural class can be a subclass of an abstract or structural class.</span></span> <span data-ttu-id="fda90-111">Uma classe estrutural pode incluir qualquer número de classes auxiliares em sua definição.</span><span class="sxs-lookup"><span data-stu-id="fda90-111">A structural class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="fda90-112">2</span><span class="sxs-lookup"><span data-stu-id="fda90-112">2</span></span>     | <span data-ttu-id="fda90-113">Uma classe abstrata, que é um modelo usado para derivar novas classes abstratas, auxiliares e estruturais.</span><span class="sxs-lookup"><span data-stu-id="fda90-113">An abstract class, which is a template used to derive new abstract, auxiliary, and structural classes.</span></span> <span data-ttu-id="fda90-114">Uma classe abstract só pode ser uma subclasse de uma classe abstract.</span><span class="sxs-lookup"><span data-stu-id="fda90-114">An abstract class can only be a subclass of an abstract class.</span></span> <span data-ttu-id="fda90-115">Classes abstratas não podem ser instanciadas em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="fda90-115">Abstract classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="fda90-116">Uma classe abstrata pode incluir qualquer número de classes auxiliares em sua definição.</span><span class="sxs-lookup"><span data-stu-id="fda90-116">An abstract class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="fda90-117">3</span><span class="sxs-lookup"><span data-stu-id="fda90-117">3</span></span>     | <span data-ttu-id="fda90-118">Uma classe auxiliar, que pode ser incluída na definição de uma classe estrutural, abstrata ou auxiliar. nesse caso, os valores **mustContain**, **systemMustContain**, **mayContain** e **systemMayContain** da classe auxiliar são adicionados a esses da classe...</span><span class="sxs-lookup"><span data-stu-id="fda90-118">An auxiliary class, which can be included in the definition of a structural, abstract, or auxiliary class, in which case, the **mustContain**, **systemMustContain**, **mayContain**, and **systemMayContain** values of the auxiliary class are added to those of the class.</span></span> <span data-ttu-id="fda90-119">Uma classe auxiliar pode ser uma subclasse de uma classe abstrata ou auxiliar.</span><span class="sxs-lookup"><span data-stu-id="fda90-119">An auxiliary class can be a subclass of an abstract or auxiliary class.</span></span> <span data-ttu-id="fda90-120">As classes auxiliares não podem ser instanciadas no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="fda90-120">Auxiliary classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="fda90-121">Uma classe auxiliar pode incluir qualquer número de classes auxiliares em sua definição.</span><span class="sxs-lookup"><span data-stu-id="fda90-121">An auxiliary class can include any number of auxiliary classes in its definition.</span></span> |



 

<span data-ttu-id="fda90-122">Não confunda o **objectClassCategory** com uma [categoria de objeto](object-class-and-object-category.md).</span><span class="sxs-lookup"><span data-stu-id="fda90-122">Do not confuse the **objectClassCategory** with an [object category](object-class-and-object-category.md).</span></span>

 

 




