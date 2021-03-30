---
title: Classes auxiliares vinculadas estaticamente
description: Uma classe auxiliar vinculada estaticamente é aquela que está incluída no atributo auxiliaryClass ou systemAuxiliaryClass da definição classSchema de uma classe de objeto no esquema.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- AD de classes auxiliares vinculadas estaticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634914"
---
# <a name="statically-linked-auxiliary-classes"></a><span data-ttu-id="034dd-104">Classes auxiliares vinculadas estaticamente</span><span class="sxs-lookup"><span data-stu-id="034dd-104">Statically Linked Auxiliary Classes</span></span>

<span data-ttu-id="034dd-105">Uma classe auxiliar vinculada estaticamente é aquela que está incluída no atributo **auxiliaryClass** ou **SystemAuxiliaryClass** da definição **classSchema** de uma classe de objeto no esquema.</span><span class="sxs-lookup"><span data-stu-id="034dd-105">A statically linked auxiliary class is one that is included in the **auxiliaryClass** or **systemAuxiliaryClass** attribute of an object class's **classSchema** definition in the schema.</span></span> <span data-ttu-id="034dd-106">Isso significa que a classe auxiliar é parte de cada instância da classe à qual está associada.</span><span class="sxs-lookup"><span data-stu-id="034dd-106">This means that the auxiliary class is part of every instance of the class with which it is associated.</span></span>

<span data-ttu-id="034dd-107">Uma classe auxiliar pode ser vinculada estaticamente a uma classe de objeto quando a classe é definida, ou seja, quando seu objeto **classSchema** é adicionado ao contêiner de esquema.</span><span class="sxs-lookup"><span data-stu-id="034dd-107">An auxiliary class can be statically linked to an object class when the class is defined, that is, when its **classSchema** object is added to the schema container.</span></span> <span data-ttu-id="034dd-108">Essa é a única vez que o **systemAuxiliaryClass** pode ser usado; Depois que um objeto **classSchema** é criado, seu atributo **systemAuxiliaryClass** não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="034dd-108">This is the only time that the **systemAuxiliaryClass** can be used; after a **classSchema** object is created, its **systemAuxiliaryClass** attribute cannot be modified.</span></span> <span data-ttu-id="034dd-109">Uma classe auxiliar que é vinculada estaticamente neste momento pode ter atributos obrigatórios (**mustHave**) e/ou opcionais (**mayHave**).</span><span class="sxs-lookup"><span data-stu-id="034dd-109">An auxiliary class that is statically linked at this time can have mandatory (**mustHave**) and/or optional (**mayHave**) attributes.</span></span>

<span data-ttu-id="034dd-110">Um usuário com privilégios com as permissões necessárias para estender o esquema pode adicionar ou remover classes auxiliares do atributo **systemAuxiliaryClass** de um objeto **classSchema** existente.</span><span class="sxs-lookup"><span data-stu-id="034dd-110">A privileged user with the permissions required to extend the schema can add or remove auxiliary classes from the **systemAuxiliaryClass** attribute of an existing **classSchema** object.</span></span> <span data-ttu-id="034dd-111">Isso adiciona ou remove a classe auxiliar de todas as instâncias existentes da classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="034dd-111">Doing so adds or removes the auxiliary class from every existing instance of the object class.</span></span> <span data-ttu-id="034dd-112">Uma classe auxiliar que é vinculada estaticamente neste momento pode ter atributos opcionais, mas não pode ter atributos obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="034dd-112">An auxiliary class that is statically linked at this time can have optional attributes, but cannot have mandatory attributes.</span></span> <span data-ttu-id="034dd-113">Isso ocorre porque pode haver instâncias existentes da classe Object; nesse caso, a adição de um novo atributo obrigatório criaria problemas.</span><span class="sxs-lookup"><span data-stu-id="034dd-113">This is because there may be existing instances of the object class, in which case, adding a new mandatory attribute would create problems.</span></span> <span data-ttu-id="034dd-114">Um usuário privilegiado pode subseqüentemente remover uma classe auxiliar do atributo **auxiliaryClass** de um objeto **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="034dd-114">A privileged user can subsequently remove an auxiliary class from the **auxiliaryClass** attribute of a **classSchema** object.</span></span>

 

 




