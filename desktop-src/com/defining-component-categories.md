---
title: Definindo categorias de componentes
description: Definindo categorias de componentes
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160492"
---
# <a name="defining-component-categories"></a><span data-ttu-id="8965e-103">Definindo categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="8965e-103">Defining Component Categories</span></span>

<span data-ttu-id="8965e-104">O autor de uma definição de categoria de componente cria um GUID exclusivo (o CATID) que é publicado junto com a definição.</span><span class="sxs-lookup"><span data-stu-id="8965e-104">The author of a component category definition creates a unique GUID (the CATID) that is published along with the definition.</span></span> <span data-ttu-id="8965e-105">Outras partes conhecem a definição desse tipo e podem fazer uso de suas classes com suporte de acordo.</span><span class="sxs-lookup"><span data-stu-id="8965e-105">Other parties know the definition of this type and can make use of its supported classes accordingly.</span></span> <span data-ttu-id="8965e-106">Como a assinatura do método de uma interface, a semântica de uma categoria não deve ser modificada após ser instalada.</span><span class="sxs-lookup"><span data-stu-id="8965e-106">Like the method signature of an interface, a category's semantics should not be modified after being installed.</span></span> <span data-ttu-id="8965e-107">É melhor manter a compatibilidade com versões anteriores da categoria, introduzindo um novo identificador de categoria com semântica revisada.</span><span class="sxs-lookup"><span data-stu-id="8965e-107">It is better to maintain backward compatibility of the category by introducing a new category identifier with revised semantics.</span></span>

<span data-ttu-id="8965e-108">Como os identificadores de interface (IID) e os identificadores de categoria de componente (CATID) existem em namespaces diferentes, parece que seria possível usar o mesmo GUID para um IID e um CATID.</span><span class="sxs-lookup"><span data-stu-id="8965e-108">Because interface identifiers (IID) and component category identifiers (CATID) exist in different namespaces, it seems as if it would be possible to use the same GUID for both an IID and a CATID.</span></span> <span data-ttu-id="8965e-109">No entanto, como IIDs geralmente são usados para o CLSID do servidor proxy/stub da interface, há o potencial de conflito.</span><span class="sxs-lookup"><span data-stu-id="8965e-109">However, since IIDs are often used for the CLSID of the interface's proxy/stub server, there is the potential for conflict.</span></span> <span data-ttu-id="8965e-110">Portanto, não use o mesmo GUID para um IID e o CATID.</span><span class="sxs-lookup"><span data-stu-id="8965e-110">Therefore, do not use the same GUID for an IID and CATID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8965e-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8965e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8965e-112">Associando ícones a uma categoria</span><span class="sxs-lookup"><span data-stu-id="8965e-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="8965e-113">Categorizando por recursos de componente</span><span class="sxs-lookup"><span data-stu-id="8965e-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="8965e-114">Categorizando por recursos de contêiner</span><span class="sxs-lookup"><span data-stu-id="8965e-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="8965e-115">Classes e associações padrão</span><span class="sxs-lookup"><span data-stu-id="8965e-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="8965e-116">O Gerenciador de categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="8965e-116">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




