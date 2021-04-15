---
title: Classes auxiliares dinâmicas
description: Semelhante às classes de objeto estrutural e abstrato, as classes auxiliares são definidas por um objeto classSchema no esquema de Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- AD de classes auxiliares dinâmicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453930"
---
# <a name="dynamic-auxiliary-classes"></a><span data-ttu-id="5cca7-104">Classes auxiliares dinâmicas</span><span class="sxs-lookup"><span data-stu-id="5cca7-104">Dynamic Auxiliary Classes</span></span>

<span data-ttu-id="5cca7-105">Semelhante às classes de objeto estrutural e abstrato, as classes auxiliares são definidas por um objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) no esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5cca7-105">Similar to structural and abstract object classes, auxiliary classes are defined by a [**classSchema**](/windows/desktop/ADSchema/c-classschema) object in the Active Directory schema.</span></span> <span data-ttu-id="5cca7-106">Para obter mais informações, consulte [classes estruturais, abstratas e auxiliares](structural-abstract-and-auxiliary-classes.md).</span><span class="sxs-lookup"><span data-stu-id="5cca7-106">For more information, see [Structural, Abstract, and Auxiliary Classes](structural-abstract-and-auxiliary-classes.md).</span></span> <span data-ttu-id="5cca7-107">Essa definição de esquema especifica várias características da classe, incluindo os atributos associados à classe.</span><span class="sxs-lookup"><span data-stu-id="5cca7-107">This schema definition specifies various characteristics of the class, including the attributes associated with the class.</span></span>

<span data-ttu-id="5cca7-108">Ao contrário das classes estruturais, não é possível criar uma instância de uma classe auxiliar como você pode com uma classe estrutural.</span><span class="sxs-lookup"><span data-stu-id="5cca7-108">Unlike with structural classes, You cannot create an instance of an auxiliary class as you can with a structural class.</span></span> <span data-ttu-id="5cca7-109">Em vez disso, você usa uma classe auxiliar para estender a lista de atributos que está associada a outra classe de objeto estrutural, abstrata ou auxiliar.</span><span class="sxs-lookup"><span data-stu-id="5cca7-109">Instead, you use an auxiliary class to extend the list of attributes that is associated with another structural, abstract, or auxiliary object class.</span></span>

<span data-ttu-id="5cca7-110">Na versão inicial do Windows 2000, Active Directory Domain Services forneceu suporte para vinculação estática de classes auxiliares à definição [**classSchema**](/windows/desktop/ADSchema/c-classschema) de outra classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="5cca7-110">In the initial release of Windows 2000, Active Directory Domain Services provided support for statically linking auxiliary classes to the [**classSchema**](/windows/desktop/ADSchema/c-classschema) definition of another object class.</span></span> <span data-ttu-id="5cca7-111">Quando uma classe auxiliar é usada dessa forma, cada instância da classe de objeto dá suporte aos atributos da classe auxiliar.</span><span class="sxs-lookup"><span data-stu-id="5cca7-111">When an auxiliary class is used in this way, every instance of the object class supports the attributes of the auxiliary class.</span></span>

<span data-ttu-id="5cca7-112">**Windows 2000 Server e versões anteriores:** O Active Directory Domain Services não oferece suporte para a vinculação dinâmica de classes auxiliares a objetos individuais, e não apenas a classes inteiras de objetos.</span><span class="sxs-lookup"><span data-stu-id="5cca7-112">**Windows 2000 Server and earlier:** Active Directory Domain Services does not provide support for dynamically linking auxiliary classes to individual objects, and not just to entire classes of objects.</span></span> <span data-ttu-id="5cca7-113">Além disso, as classes auxiliares que foram anexadas a uma instância de objeto não podem ser removidas subsequentemente da instância.</span><span class="sxs-lookup"><span data-stu-id="5cca7-113">In addition, auxiliary classes that have been attached to an object instance cannot subsequently be removed from the instance.</span></span>

<span data-ttu-id="5cca7-114">**Windows Server 2003:** As classes auxiliares dinâmicas têm suporte quando todos os controladores de domínio na floresta estão executando o Windows Server 2003 e o modo funcional da floresta é o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5cca7-114">**Windows Server 2003:** Dynamic Auxiliary Classes are supported when all domain controllers in the forest are running Windows Server 2003 and the forest functional mode is Windows Server 2003.</span></span>

<span data-ttu-id="5cca7-115">Para obter mais informações sobre as classes auxiliares, consulte:</span><span class="sxs-lookup"><span data-stu-id="5cca7-115">For more information about auxiliary classes, see:</span></span>

-   [<span data-ttu-id="5cca7-116">Classes auxiliares vinculadas dinamicamente</span><span class="sxs-lookup"><span data-stu-id="5cca7-116">Dynamically Linked Auxiliary Classes</span></span>](dynamically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="5cca7-117">Classes auxiliares vinculadas estaticamente</span><span class="sxs-lookup"><span data-stu-id="5cca7-117">Statically Linked Auxiliary Classes</span></span>](statically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="5cca7-118">Determinando as classes associadas a uma instância de objeto</span><span class="sxs-lookup"><span data-stu-id="5cca7-118">Determining the Classes Associated With an Object Instance</span></span>](determining-the-classes-associated-with-an-object-instance.md)
-   [<span data-ttu-id="5cca7-119">Adicionando uma classe auxiliar a uma instância de objeto</span><span class="sxs-lookup"><span data-stu-id="5cca7-119">Adding an Auxiliary Class to an Object Instance</span></span>](adding-an-auxiliary-class-to-an-object-instance.md)

<span data-ttu-id="5cca7-120">Para obter mais informações sobre os níveis funcionais de floresta, consulte "como aumentar Active Directory níveis funcionais de domínio e floresta" na base de dados de conhecimento de ajuda e suporte em [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .</span><span class="sxs-lookup"><span data-stu-id="5cca7-120">For more information about forest functional levels, see "How to raise Active Directory domain and forest functional levels" in the Help and Support Knowledge Base at [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692).</span></span>

 

 