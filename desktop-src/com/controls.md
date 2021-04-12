---
title: Controls (COM)
description: Controles
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294683"
---
# <a name="controls-com"></a><span data-ttu-id="3f7c5-103">Controls (COM)</span><span class="sxs-lookup"><span data-stu-id="3f7c5-103">Controls (COM)</span></span>

<span data-ttu-id="3f7c5-104">Um controle ActiveX é, na verdade, apenas outro termo para objeto OLE ou, mais especificamente, objeto COM.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-104">An ActiveX control is really just another term for OLE object or more specifically, COM object.</span></span> <span data-ttu-id="3f7c5-105">Em outras palavras, um controle, na pior das hipóteses, é um objeto COM que dá suporte à interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e também o registro em si.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-105">In other words, a control, at the very least, is some COM object that supports the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface and is also self-registering.</span></span> <span data-ttu-id="3f7c5-106">Por meio de [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , um contêiner pode gerenciar o tempo de vida do controle, bem como descobrir dinamicamente a extensão completa da funcionalidade de um controle com base nas interfaces disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-106">Through [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) a container can manage the lifetime of the control as well as dynamically discover the full extent of a control's functionality based on the available interfaces.</span></span> <span data-ttu-id="3f7c5-107">Isso permite que um controle implemente o mínimo de funcionalidade que ele precisa para, em vez de dar suporte a um grande número de interfaces que, na verdade, não fazem nada.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-107">This allows a control to implement as little functionality as it needs to, instead of supporting a large number of interfaces that actually don't do anything.</span></span> <span data-ttu-id="3f7c5-108">Em suma, esse requisito mínimo para nada mais que **IUnknown** permite que qualquer controle seja tão leve quanto possível.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-108">In short, this minimal requirement for nothing more than **IUnknown** allows any control to be as lightweight as it can.</span></span>

<span data-ttu-id="3f7c5-109">Em suma, além de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e Autoregistro, não há nenhum outro requisito para um controle.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-109">In short, other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and self-registration, there are no other requirements for a control.</span></span> <span data-ttu-id="3f7c5-110">No entanto, há convenções que devem ser seguidas sobre o que o suporte de uma interface significa em termos de funcionalidade fornecida ao contêiner pelo controle.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-110">There are, however, conventions that should be followed about what the support of an interface means in terms of functionality provided to the container by the control.</span></span> <span data-ttu-id="3f7c5-111">Em seguida, esta seção descreve o que significa para um controle para realmente dar suporte a uma interface, bem como métodos, propriedades e eventos que um controle deve fornecer como uma linha de base, se houver ocasiões para dar suporte a métodos, propriedades e eventos.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-111">This section then describes what it means for a control to actually support an interface, as well as methods, properties, and events that a control should provide as a baseline if it has occasion to support methods, properties, and events.</span></span>

<span data-ttu-id="3f7c5-112">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="3f7c5-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3f7c5-113">Registro automático para controles</span><span class="sxs-lookup"><span data-stu-id="3f7c5-113">Self Registration for Controls</span></span>](self-registration-for-controls.md)
-   [<span data-ttu-id="3f7c5-114">O que é o suporte para uma interface significa</span><span class="sxs-lookup"><span data-stu-id="3f7c5-114">What Support for an Interface Means</span></span>](what-support-for-an-interface-means.md)
-   [<span data-ttu-id="3f7c5-115">Interfaces de persistência</span><span class="sxs-lookup"><span data-stu-id="3f7c5-115">Persistence Interfaces</span></span>](persistence-interfaces.md)
-   [<span data-ttu-id="3f7c5-116">Métodos opcionais em interfaces de controle</span><span class="sxs-lookup"><span data-stu-id="3f7c5-116">Optional Methods in Control Interfaces</span></span>](optional-methods-in-control-interfaces.md)
-   [<span data-ttu-id="3f7c5-117">Opções de fábrica de classes</span><span class="sxs-lookup"><span data-stu-id="3f7c5-117">Class Factory Options</span></span>](class-factory-options.md)
-   [<span data-ttu-id="3f7c5-118">Expondo Propriedades por meio de IDispatch</span><span class="sxs-lookup"><span data-stu-id="3f7c5-118">Exposing Properties through IDispatch</span></span>](properties.md)
-   [<span data-ttu-id="3f7c5-119">Expondo métodos por meio de IDispatch</span><span class="sxs-lookup"><span data-stu-id="3f7c5-119">Exposing Methods through IDispatch</span></span>](exposing-methods-through-idispatch.md)
-   [<span data-ttu-id="3f7c5-120">Eventos em controles</span><span class="sxs-lookup"><span data-stu-id="3f7c5-120">Events in Controls</span></span>](events-in-controls.md)
-   [<span data-ttu-id="3f7c5-121">Páginas de propriedade</span><span class="sxs-lookup"><span data-stu-id="3f7c5-121">Property Pages</span></span>](property-pages.md)
-   [<span data-ttu-id="3f7c5-122">Propriedades de ambiente para controles</span><span class="sxs-lookup"><span data-stu-id="3f7c5-122">Ambient Properties for Controls</span></span>](ambient-properties-for-controls.md)
-   [<span data-ttu-id="3f7c5-123">Usando a funcionalidade do contêiner</span><span class="sxs-lookup"><span data-stu-id="3f7c5-123">Using the Container's Functionality</span></span>](using-the-container-s-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="3f7c5-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f7c5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f7c5-125">Diretrizes de contêiner de controle e controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="3f7c5-125">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




