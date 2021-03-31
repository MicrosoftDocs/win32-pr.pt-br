---
title: Classes auxiliares vinculadas dinamicamente
description: Uma classe auxiliar vinculada dinamicamente é uma classe que é anexada a um objeto individual, em vez de uma classe de objeto.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- AD de classes auxiliares vinculadas dinamicamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159329"
---
# <a name="dynamically-linked-auxiliary-classes"></a><span data-ttu-id="9f7a7-104">Classes auxiliares vinculadas dinamicamente</span><span class="sxs-lookup"><span data-stu-id="9f7a7-104">Dynamically Linked Auxiliary Classes</span></span>

<span data-ttu-id="9f7a7-105">Uma classe auxiliar vinculada dinamicamente é uma classe que é anexada a um objeto individual, em vez de uma classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="9f7a7-105">A dynamically linked auxiliary class is a class that is attached to an individual object, rather than to an object class.</span></span> <span data-ttu-id="9f7a7-106">A vinculação dinâmica permite que você armazene atributos adicionais com um objeto individual sem o impacto em toda a floresta de estender a definição de esquema para uma classe inteira.</span><span class="sxs-lookup"><span data-stu-id="9f7a7-106">Dynamic linking enables you to store additional attributes with an individual object without the forest-wide impact of extending the schema definition for an entire class.</span></span> <span data-ttu-id="9f7a7-107">Por exemplo, uma empresa poderia usar a vinculação dinâmica para anexar uma classe auxiliar específica de vendas aos objetos de usuário de suas pessoas de vendas e outras classes auxiliares específicas de departamento aos objetos de usuário de funcionários de outros departamentos.</span><span class="sxs-lookup"><span data-stu-id="9f7a7-107">For example, an enterprise could use dynamic linking to attach a sales-specific auxiliary class to the user objects of its sales people, and other department-specific auxiliary classes to the user objects of employees in other departments.</span></span>

<span data-ttu-id="9f7a7-108">A vinculação dinâmica não é complexa: Adicione o nome da classe auxiliar aos valores do atributo **objectClass** de um objeto.</span><span class="sxs-lookup"><span data-stu-id="9f7a7-108">Dynamic linking is not complex: add the name of the auxiliary class to the values of an object's **objectClass** attribute.</span></span> <span data-ttu-id="9f7a7-109">Se a classe auxiliar tiver atributos obrigatórios (**mustHave** ou **systemMustHave**), você deverá defini-los ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9f7a7-109">If the auxiliary class has any mandatory attributes (**mustHave** or **systemMustHave**), you must set them at the same time.</span></span> <span data-ttu-id="9f7a7-110">Para obter mais informações e um exemplo de código, consulte [adicionando uma classe auxiliar a uma instância de objeto](adding-an-auxiliary-class-to-an-object-instance.md).</span><span class="sxs-lookup"><span data-stu-id="9f7a7-110">For more information and a code example, see [Adding an Auxiliary Class to an Object Instance](adding-an-auxiliary-class-to-an-object-instance.md).</span></span>

<span data-ttu-id="9f7a7-111">Para remover uma classe auxiliar dinamicamente vinculada, limpe os valores de todos os atributos da classe auxiliar e, em seguida, remova o nome da classe auxiliar do atributo **objectClass** do objeto.</span><span class="sxs-lookup"><span data-stu-id="9f7a7-111">To remove a dynamically linked auxiliary class, clear the values of all attributes from the auxiliary class, and then remove the name of the auxiliary class from the **objectClass** attribute of the object.</span></span>

<span data-ttu-id="9f7a7-112">Se você adicionar dinamicamente uma classe auxiliar que é uma subclasse de outra classe auxiliar, ambas as classes auxiliares serão adicionadas ao objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="9f7a7-112">If you dynamically add an auxiliary class that is a subclass of another auxiliary class, both auxiliary classes are added to the target object.</span></span> <span data-ttu-id="9f7a7-113">No entanto, remover a classe auxiliar filho não remove seu pai; cada classe deve ser explicitamente removida.</span><span class="sxs-lookup"><span data-stu-id="9f7a7-113">However, removing the child auxiliary class does not remove its parent; each class must be explicitly removed.</span></span>

 

 




