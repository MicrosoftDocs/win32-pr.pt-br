---
title: Arquitetura de controles ActiveX
description: A tecnologia de controles ActiveX baseia-se em uma base de muitos objetos e interfaces de nível inferior no OLE. As interfaces exatas disponíveis em um controle variam de acordo com seus recursos. Esta seção examina mais detalhadamente os recursos que um controle pode fornecer.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635586"
---
# <a name="activex-controls-architecture"></a><span data-ttu-id="7f382-105">Arquitetura de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="7f382-105">ActiveX Controls Architecture</span></span>

<span data-ttu-id="7f382-106">A tecnologia de controles ActiveX baseia-se em uma base de muitos objetos e interfaces de nível inferior no OLE.</span><span class="sxs-lookup"><span data-stu-id="7f382-106">ActiveX controls technology builds on a foundation of many lower-level objects and interfaces in OLE.</span></span> <span data-ttu-id="7f382-107">As interfaces exatas disponíveis em um controle variam de acordo com seus recursos.</span><span class="sxs-lookup"><span data-stu-id="7f382-107">The exact interfaces available on a control vary with its capabilities.</span></span> <span data-ttu-id="7f382-108">Esta seção examina mais detalhadamente os recursos que um controle pode fornecer.</span><span class="sxs-lookup"><span data-stu-id="7f382-108">This section takes a closer look at the capabilities a control might provide.</span></span>

<span data-ttu-id="7f382-109">Os controles ActiveX são usados para fornecer os blocos de construção para a criação de interfaces de usuário em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7f382-109">ActiveX controls are used to provide the building blocks for creating user interfaces in applications.</span></span> <span data-ttu-id="7f382-110">Por exemplo, um botão que inicia alguma ação no aplicativo de contêiner quando ele é clicado é um controle simples.</span><span class="sxs-lookup"><span data-stu-id="7f382-110">For example, a button that initiates some action in the container application when it is clicked is a simple control.</span></span> <span data-ttu-id="7f382-111">Os seguintes aspectos estão envolvidos no fornecimento desses blocos de construção de interface do usuário:</span><span class="sxs-lookup"><span data-stu-id="7f382-111">The following aspects are involved in providing these user interface building blocks:</span></span>

-   <span data-ttu-id="7f382-112">Um controle pode ser inserido em seu cliente de contêiner para dar suporte a alguma atividade de interface do usuário no cliente.</span><span class="sxs-lookup"><span data-stu-id="7f382-112">A control can be embedded within its container client to support some user interface activity within the client.</span></span> <span data-ttu-id="7f382-113">Assim, um controle precisa fornecer uma representação visual de si mesmo quando ele é inserido no contêiner e precisa fornecer uma maneira de salvar seu estado, por exemplo, seus valores de propriedade e sua posição dentro de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="7f382-113">Thus, a control needs to provide a visual representation of itself when it is embedded within the container and needs to provide a way to save its state, for example, its property values and its position within its container.</span></span> <span data-ttu-id="7f382-114">O cliente deve oferecer suporte a um contêiner com objetos inseridos nele.</span><span class="sxs-lookup"><span data-stu-id="7f382-114">The client must support being a container with objects embedded in it.</span></span>
-   <span data-ttu-id="7f382-115">Ao ativar o controle usando um teclado ou mouse, o usuário final inicia alguma ação no aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="7f382-115">By activating the control using a keyboard or mouse, the end user initiates some action in the client application.</span></span> <span data-ttu-id="7f382-116">Portanto, um controle deve responder à atividade de teclado e deve ser capaz de se comunicar com seu cliente para que ele possa notificar seu contêiner de suas atividades e disparar eventos no cliente.</span><span class="sxs-lookup"><span data-stu-id="7f382-116">Thus, a control must respond to keyboard activity and must be able to communicate with its client so it can notify its container of its activities and trigger events in the client.</span></span>
-   <span data-ttu-id="7f382-117">O cliente normalmente também fornece uma linguagem de programação por meio da qual o usuário final pode iniciar ações fornecidas pelas propriedades e métodos do controle.</span><span class="sxs-lookup"><span data-stu-id="7f382-117">The client also typically provides a programming language through which the end user can initiate actions provided by the control's properties and methods.</span></span> <span data-ttu-id="7f382-118">Portanto, um controle deve dar suporte à automação e a algum conjunto de recursos de tempo de design versus tempo de execução também.</span><span class="sxs-lookup"><span data-stu-id="7f382-118">Thus, a control must support automation and some set of design-time versus run-time features as well.</span></span>

<span data-ttu-id="7f382-119">Como resultado de sua função no fornecimento de blocos de construção de interface do usuário, um controle normalmente dá suporte a recursos nas seguintes áreas usando as tecnologias OLE, conforme indicado:</span><span class="sxs-lookup"><span data-stu-id="7f382-119">As a result of its role in providing user interface building blocks, a control typically supports features in the following areas using OLE technologies as indicated:</span></span>

<dl> <dt>

<span data-ttu-id="7f382-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Propriedades e métodos</span><span class="sxs-lookup"><span data-stu-id="7f382-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Properties and methods</span></span>
</dt> <dd>

<span data-ttu-id="7f382-121">Como qualquer objeto OLE, um controle pode fornecer grande parte de sua funcionalidade por meio de um conjunto de interfaces de entrada com propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="7f382-121">Like any OLE object, a control can provide much of its functionality through a set of incoming interfaces with properties and methods.</span></span> <span data-ttu-id="7f382-122">O contêiner pode fornecer propriedades de ambiente adicionais e pode dar suporte à extensão das propriedades do controle por meio de agregação.</span><span class="sxs-lookup"><span data-stu-id="7f382-122">The container can supply additional ambient properties, and it can support extending the control's properties through aggregation.</span></span> <span data-ttu-id="7f382-123">Esses recursos são REST na automação OLE, páginas de propriedades, objetos conectáveis e tecnologias de controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="7f382-123">These features rest on OLE automation, property pages, connectable objects, and ActiveX control technologies.</span></span>

</dd> <dt>

<span data-ttu-id="7f382-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>LostFocus</span><span class="sxs-lookup"><span data-stu-id="7f382-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Events</span></span>
</dt> <dd>

<span data-ttu-id="7f382-125">Além de fornecer propriedades e métodos, um controle ActiveX também pode fornecer interfaces de saída para notificar seu cliente de eventos.</span><span class="sxs-lookup"><span data-stu-id="7f382-125">In addition to providing properties and methods, an ActiveX control can also provide outgoing interfaces to notify its client of events.</span></span> <span data-ttu-id="7f382-126">O cliente deve dar suporte ao tratamento desses eventos.</span><span class="sxs-lookup"><span data-stu-id="7f382-126">The client must support handling of these events.</span></span> <span data-ttu-id="7f382-127">Esses recursos usam a automação OLE e objetos conectáveis.</span><span class="sxs-lookup"><span data-stu-id="7f382-127">These features use OLE automation and connectable objects.</span></span>

</dd> <dt>

<span data-ttu-id="7f382-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Representação visual</span><span class="sxs-lookup"><span data-stu-id="7f382-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Visual representation</span></span>
</dt> <dd>

<span data-ttu-id="7f382-129">Um controle pode dar suporte ao posicionamento e à exibição em seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="7f382-129">A control can support positioning and displaying itself within its container.</span></span> <span data-ttu-id="7f382-130">O contêiner posiciona o controle e determina seu tamanho.</span><span class="sxs-lookup"><span data-stu-id="7f382-130">The container positions the control and determines its size.</span></span> <span data-ttu-id="7f382-131">Esses recursos usam tecnologia de documento composto, incluindo tecnologia de arrastar e soltar OLE.</span><span class="sxs-lookup"><span data-stu-id="7f382-131">These features use compound document technology, including OLE drag and drop technology.</span></span>

</dd> <dt>

<span data-ttu-id="7f382-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Manuseio de teclado</span><span class="sxs-lookup"><span data-stu-id="7f382-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Keyboard handling</span></span>
</dt> <dd>

<span data-ttu-id="7f382-133">Um controle pode responder a aceleradores de teclado para que o usuário final possa iniciar ações executadas pelo controle.</span><span class="sxs-lookup"><span data-stu-id="7f382-133">A control can respond to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="7f382-134">O contêiner gerencia a atividade de teclado para todos os seus controles inseridos.</span><span class="sxs-lookup"><span data-stu-id="7f382-134">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="7f382-135">Esses recursos usam tecnologias de controle e documento composto.</span><span class="sxs-lookup"><span data-stu-id="7f382-135">These features use control and compound document technologies.</span></span>

</dd> <dt>

<span data-ttu-id="7f382-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistência</span><span class="sxs-lookup"><span data-stu-id="7f382-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistence</span></span>
</dt> <dd>

<span data-ttu-id="7f382-137">Um controle pode salvar seu estado.</span><span class="sxs-lookup"><span data-stu-id="7f382-137">A control can save its state.</span></span> <span data-ttu-id="7f382-138">O cliente gerencia a persistência de seus controles inseridos.</span><span class="sxs-lookup"><span data-stu-id="7f382-138">The client manages the persistence of its embedded controls.</span></span> <span data-ttu-id="7f382-139">Esses recursos usam tecnologias de armazenamento estruturado e de persistência de objeto.</span><span class="sxs-lookup"><span data-stu-id="7f382-139">These features use structured storage and object persistence technologies.</span></span>

</dd> <dt>

<span data-ttu-id="7f382-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registro e licenciamento</span><span class="sxs-lookup"><span data-stu-id="7f382-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registration and licensing</span></span>
</dt> <dd>

<span data-ttu-id="7f382-141">Um controle normalmente dá suporte a Autoregistro e cria um conjunto de entradas do registro quando ele é instanciado.</span><span class="sxs-lookup"><span data-stu-id="7f382-141">A control typically supports self-registration and creates a set of registry entries when it is instantiated.</span></span> <span data-ttu-id="7f382-142">Um controle também pode ser licenciado para ajudar a evitar o uso não autorizado.</span><span class="sxs-lookup"><span data-stu-id="7f382-142">A control can also be licensed to help prevent unauthorized use.</span></span>

</dd> </dl>

<span data-ttu-id="7f382-143">A maioria desses recursos envolve o controle e seu contêiner de cliente.</span><span class="sxs-lookup"><span data-stu-id="7f382-143">Most of these features involve both the control and its client container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f382-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f382-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f382-145">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="7f382-145">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




