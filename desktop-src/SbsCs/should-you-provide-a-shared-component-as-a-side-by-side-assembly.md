---
description: Os provedores de componentes compartilhados devem considerar tornar seu componente disponível como um assembly lado a lado se um ou mais dos casos a seguir forem verdadeiros.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: Você deve fornecer um componente compartilhado como um assembly lado a lado?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829771"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a><span data-ttu-id="e72a1-103">Você deve fornecer um componente compartilhado como um assembly lado a lado?</span><span class="sxs-lookup"><span data-stu-id="e72a1-103">Should you provide a shared component as a side-by-side assembly?</span></span>

<span data-ttu-id="e72a1-104">Os provedores de componentes compartilhados devem considerar tornar seu componente disponível como um assembly lado a lado se um ou mais dos seguintes itens forem verdadeiros:</span><span class="sxs-lookup"><span data-stu-id="e72a1-104">Providers of shared components should consider making their component available as a side-by-side assembly if one or more of the following are true:</span></span>

-   <span data-ttu-id="e72a1-105">O componente expõe uma interface de programação de aplicativo avançada que é usada por muitos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e72a1-105">The component exposes a rich application programming interface that is used by many applications.</span></span> <span data-ttu-id="e72a1-106">Por exemplo, um componente como o MSHTML, que permite que aplicativos C e C++ acessem o modelo de objeto HTML dinâmico (DHTML).</span><span class="sxs-lookup"><span data-stu-id="e72a1-106">For example, a component such as MSHTML, which enables C and C++ applications to access the Dynamic HTML (DHTML) Object Model.</span></span>
-   <span data-ttu-id="e72a1-107">O componente já está sendo compartilhado por vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e72a1-107">The component is already being shared by multiple applications.</span></span> <span data-ttu-id="e72a1-108">Por exemplo, um componente como o COMCTL32, que fornece aos aplicativos acesso aos controles comuns.</span><span class="sxs-lookup"><span data-stu-id="e72a1-108">For example, a component such as COMCTL32, which provides applications access to the common controls.</span></span>
-   <span data-ttu-id="e72a1-109">O componente é um novo componente.</span><span class="sxs-lookup"><span data-stu-id="e72a1-109">The component is a new component.</span></span>
-   <span data-ttu-id="e72a1-110">O componente é um componente de modo de usuário e não um driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e72a1-110">The component is a user-mode component and not a device driver.</span></span>

<span data-ttu-id="e72a1-111">Nem todo componente é um candidato adequado para um assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="e72a1-111">Not every component is a suitable candidate for a side-by-side assembly.</span></span> <span data-ttu-id="e72a1-112">Um componente não é um candidato adequado para um assembly lado a lado se qualquer uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="e72a1-112">A component is not a suitable candidate for a side-by-side assembly if any of the following are true:</span></span>

-   <span data-ttu-id="e72a1-113">O componente manipula a comunicação entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e72a1-113">The component handles communication between applications.</span></span> <span data-ttu-id="e72a1-114">Por exemplo, partes de OLE32 não fariam um bom assembly lado a lado porque você não desejaria ter duas versões diferentes das partes que coordenam a comunicação entre os aplicativos executados no seu sistema.</span><span class="sxs-lookup"><span data-stu-id="e72a1-114">For example, parts of OLE32 would not make a good side-by-side assembly because you would not want to have two different versions of the parts that coordinate communication between applications run on your system.</span></span>
-   <span data-ttu-id="e72a1-115">O componente gerencia um dispositivo físico ou virtual para o sistema.</span><span class="sxs-lookup"><span data-stu-id="e72a1-115">The component manages a physical or virtual device for the system.</span></span> <span data-ttu-id="e72a1-116">Por exemplo, um driver de dispositivo para um spooler de impressão.</span><span class="sxs-lookup"><span data-stu-id="e72a1-116">For example a device driver for a print spooler.</span></span>

<span data-ttu-id="e72a1-117">Em alguns casos, pode ser possível para o desenvolvedor do componente recriar um componente existente a fim de torná-lo adequado para publicação como um assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="e72a1-117">In some cases it may be possible for the developer of the component to redesign an existing component in order to make it suitable for publication as a side-by-side assembly.</span></span> <span data-ttu-id="e72a1-118">Para obter mais informações, consulte [diretrizes para criar assemblies lado a lado](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="e72a1-118">For more information see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

 

 



