---
title: Glossário do COM
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105772974"
---
# <a name="com-glossary"></a><span data-ttu-id="0d9b4-103">Glossário do COM</span><span class="sxs-lookup"><span data-stu-id="0d9b4-103">COM Glossary</span></span>

<dl> <dt>

<span data-ttu-id="0d9b4-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**ativá**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-105">O processo de carregar um objeto na memória, que o coloca no estado de execução.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-105">The process of loading an object in memory, which puts it into the running state.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**estado ativo**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**active state**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-107">Um objeto COM que está no estado de execução e tem uma interface do usuário visível.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-107">A COM object that is in the running state and has a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker absoluto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**absolute moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-109">Um moniker que especifica o local absoluto de um objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-109">A moniker that specifies the absolute location of an object.</span></span> <span data-ttu-id="0d9b4-110">Um moniker absoluto é análogo a um caminho completo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-110">An absolute moniker is analogous to a full path.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**titular do comunicado**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**advisory holder**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-112">Um objeto COM que armazena em cache, gerencia e envia notificações de alterações nos coletores de consultoria de aplicativos de contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-112">A COM object that caches, manages, and sends notifications of changes to container applications' advisory sinks.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**coletor de consultoria**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**advisory sink**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-114">Um objeto COM que pode receber notificações de alterações em um objeto incorporado ou vinculado, pois ele implementa a interface [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) ou [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-114">A COM object that can receive notifications of changes in an embedded object or linked object because it implements the [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) or [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) interface.</span></span> <span data-ttu-id="0d9b4-115">Contêineres que precisam ser notificados sobre alterações em objetos implementam um coletor de consultoria.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-115">Containers that need to be notified of changes in objects implement an advisory sink.</span></span> <span data-ttu-id="0d9b4-116">As notificações são originadas no servidor, que usa um objeto de suporte de consultoria para armazenar em cache e gerenciar notificações para contêineres.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-116">Notifications originate in the server, which uses an advisory holder object to cache and manage notifications to containers.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**objeto de agregação**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**aggregate object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-118">Um objeto COM que é composto de um ou mais objetos COM.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-118">A COM object that is made up of one or more other COM objects.</span></span> <span data-ttu-id="0d9b4-119">Um objeto na agregação é designado como o objeto de controle, que controla quais interfaces na agregação são expostas e que são particulares.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-119">One object in the aggregate is designated the controlling object, which controls which interfaces in the aggregate are exposed and which are private.</span></span> <span data-ttu-id="0d9b4-120">Esse objeto de controle tem uma implementação especial de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) chamada de controle **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-120">This controlling object has a special implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) called the controlling **IUnknown**.</span></span> <span data-ttu-id="0d9b4-121">Todos os objetos na agregação devem passar chamadas para métodos **IUnknown** por meio do **IUnknown** de controle.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-121">All objects in the aggregate must pass calls to **IUnknown** methods through the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**Aggregation**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-123">Uma técnica de composição para implementar objetos COM.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-123">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="0d9b4-124">Ele permite que você crie um novo objeto reutilizando uma ou mais implementações de interface de objetos existentes.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-124">It allows you to build a new object by reusing one or more existing objects' interface implementations.</span></span> <span data-ttu-id="0d9b4-125">O objeto Aggregate escolhe quais interfaces devem ser expostas aos clientes e as interfaces são expostas como se fossem implementadas pelo objeto Aggregate.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-125">The aggregate object chooses which interfaces to expose to clients, and the interfaces are exposed as if they were implemented by the aggregate object.</span></span> <span data-ttu-id="0d9b4-126">Os clientes do objeto de agregação se comunicam somente com o objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-126">Clients of the aggregate object communicate only with the aggregate object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**Propriedade de ambiente**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**ambient property**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-128">Uma propriedade de tempo de execução que é gerenciada e exposta pelo contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-128">A run-time property that is managed and exposed by the container.</span></span> <span data-ttu-id="0d9b4-129">Normalmente, uma propriedade de ambiente representa uma característica de um formulário, como a cor do plano de fundo, que precisa ser comunicada a um controle para que o controle possa assumir a aparência de seu ambiente adjacente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-129">Typically, an ambient property represents a characteristic of a form, such as background color, that needs to be communicated to a control so that the control can assume the look and feel of its surrounding environment.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-131">O inverso de um arquivo, item ou moniker de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-131">The inverse of a file, item, or pointer moniker.</span></span> <span data-ttu-id="0d9b4-132">Um anti-moniker é adicionado ao final de um arquivo, item ou moniker de ponteiro para anular.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-132">An anti-moniker is added to the end of a file, item, or pointer moniker to nullify it.</span></span> <span data-ttu-id="0d9b4-133">Os antimonikers são usados na construção de monikers relativos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-133">Anti-monikers are used in the construction of relative monikers.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**contagem de referência artificial**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**artificial reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-135">Uma técnica usada para ajudar a proteger um objeto antes de chamar uma função ou um método que poderia destruí-lo prematuramente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-135">A technique used to help protect an object before calling a function or method that could prematurely destroy it.</span></span> <span data-ttu-id="0d9b4-136">Um programa chama **IUnknown:: AddRef** para incrementar a contagem de referência do objeto antes de fazer a chamada que poderia liberar o objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-136">A program calls **IUnknown::AddRef** to increment the object's reference count before making the call that could free the object.</span></span> <span data-ttu-id="0d9b4-137">Depois que a função retorna, o programa chama **IUnknown:: Release** para diminuir a contagem.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-137">After the function returns, the program calls **IUnknown::Release** to decrement the count.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**Associação assíncrona**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**asynchronous binding**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-139">Um tipo de associação em que é necessário que o processo ocorra de forma assíncrona para evitar a degradação do desempenho do usuário final.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-139">A type of binding in which it is necessary for the process to occur asynchronously to avoid performance degradation for the end user.</span></span> <span data-ttu-id="0d9b4-140">Normalmente, a vinculação assíncrona é usada em ambientes distribuídos, como o World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-140">Typically, asynchronous binding is used in distributed environments such as the World Wide Web.</span></span> <span data-ttu-id="0d9b4-141">O OLE dá suporte a classes de moniker assíncronas e mecanismos de retorno de chamada que permitem que o processo de localização e inicialização de um objeto em um ambiente distribuído ocorra enquanto outras operações são executadas.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-141">OLE supports asynchronous moniker classes and callback mechanisms that allow the process of locating and initializing an object in a distributed environment to occur while other operations are being carried out.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**chamada assíncrona**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**asynchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-143">Uma chamada para uma função que é executada separadamente para que o chamador possa continuar processando as instruções sem esperar que a função retorne.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-143">A call to a function that is executed separately so that the caller can continue processing instructions without waiting for the function to return.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker assíncrono**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**asynchronous moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-145">Um moniker que dá suporte à associação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-145">A moniker that supports asynchronous binding.</span></span> <span data-ttu-id="0d9b4-146">Por exemplo, as instâncias da classe de moniker da URL fornecida pelo sistema são monikers assíncronos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-146">For example, instances of the system-supplied URL moniker class are asynchronous monikers.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**inicia**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automation**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-148">Uma maneira de manipular objetos de um aplicativo de fora do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-148">A way to manipulate an application's objects from outside the application.</span></span> <span data-ttu-id="0d9b4-149">Normalmente, a automação é usada para criar aplicativos que expõem objetos a ferramentas de programação e linguagens de macro, criar e manipular objetos de um aplicativo a partir de outros aplicativos ou criar ferramentas para acessar e manipular objetos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-149">Automation is typically used to create applications that expose objects to programming tools and macro languages, create and manipulate one application's objects from another applications, or to create tools for accessing and manipulating objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contexto de associação**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**bind context**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-151">Um objeto COM que implementa a interface [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-151">A COM object that implements the [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="0d9b4-152">Os contextos de ligação são usados em operações de moniker para manter referências aos objetos ativados quando um moniker é associado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-152">Bind contexts are used in moniker operations to hold references to the objects activated when a moniker is bound.</span></span> <span data-ttu-id="0d9b4-153">O contexto de associação contém parâmetros que se aplicam a todas as operações durante a associação de um moniker composto genérico e fornece a implementação do moniker com acesso a informações sobre seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-153">The bind context contains parameters that apply to all operations during the binding of a generic composite moniker and provides the moniker implementation with access to information about its environment.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**vinculação**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-155">Associando um nome a seu Referent.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-155">Associating a name with its referent.</span></span> <span data-ttu-id="0d9b4-156">Especificamente, localizando o objeto nomeado por um moniker, colocando-o em seu estado de execução, se ainda não estiver, e retornando um ponteiro de interface para ele.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-156">Specifically, locating the object named by a moniker, putting it into its running state if it isn't already, and returning an interface pointer to it.</span></span> <span data-ttu-id="0d9b4-157">Os objetos podem ser associados em tempo de execução (também chamado de associação tardia ou vinculação dinâmica) ou em tempo de compilação (também chamado de associação estática).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-157">Objects can be bound at run time (also called late binding or dynamic binding) or at compile time (also called static binding).</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**armazenar**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**cache**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-159">Um (geralmente temporário) armazenamento local de informações.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-159">A (usually temporary) local store of information.</span></span> <span data-ttu-id="0d9b4-160">No OLE, um cache contém informações que definem a apresentação de um objeto vinculado ou inserido quando o contêiner é aberto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-160">In OLE, a cache contains information that defines the presentation of a linked or embedded object when the container is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**inicialização do cache**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**cache initialization**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-162">Preenchendo o cache de um objeto vinculado ou inserido com dados de apresentação.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-162">Filling a linked or embedded object's cache with presentation data.</span></span> <span data-ttu-id="0d9b4-163">A interface [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) fornece métodos que um contêiner pode chamar para controlar os dados que são armazenados em cache para objetos vinculados ou incorporados.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-163">The [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) interface provides methods that a container can call to control the data that gets cached for linked or embedded objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**classes**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**class**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-165">A definição de um objeto no código.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-165">The definition of an object in code.</span></span> <span data-ttu-id="0d9b4-166">Em C++, a classe de um objeto é definida como um tipo de dados, mas esse não é o caso em outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-166">In C++, the class of an object is defined as a data type, but this is not the case in other languages.</span></span> <span data-ttu-id="0d9b4-167">Como o OLE pode ser codificado em qualquer linguagem, a classe é usada para fazer referência à definição geral do objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-167">Because OLE can be coded in any language, class is used to refer to the general object definition.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**fábrica de classes**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-169">Um objeto COM que implementa a interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e que cria uma ou mais instâncias de um objeto identificado por um determinado identificador de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-169">A COM object that implements the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface and that creates one or more instances of an object identified by a given class identifier(CLSID).</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**identificador de classe (CLSID)**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**class identifier (CLSID)**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-171">Um GUID (identificador global exclusivo) associado a um objeto de classe OLE.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-171">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="0d9b4-172">Se um objeto de classe for usado para criar mais de uma instância de um objeto, o aplicativo de servidor associado deverá registrar seu CLSID no registro do sistema para que os clientes possam localizar e carregar o código executável associado aos objetos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-172">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="0d9b4-173">Todo servidor OLE ou contêiner que permite vincular a seus objetos inseridos deve registrar um CLSID para cada definição de objeto com suporte.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-173">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**objeto de classe**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**class object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-175">Na programação orientada a objeto, um objeto cujo estado é compartilhado por todos os objetos em uma classe e cujo comportamento atua nos dados de estado classwide.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-175">In object-oriented programming, an object whose state is shared by all the objects in a class and whose behavior acts on that classwide state data.</span></span> <span data-ttu-id="0d9b4-176">No COM, os objetos de classe são chamados de fábricas de classes e normalmente não têm nenhum comportamento, exceto para criar novas instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-176">In COM, class objects are called class factories, and typically have no behavior except to create new instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**cliente**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-178">Um objeto COM que solicita serviços de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-178">A COM object that requests services from another object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**site do cliente**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**client site**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-180">O site de exibição de um objeto incorporado ou vinculado em um documento composto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-180">The display site for an embedded or linked object within a compound document.</span></span> <span data-ttu-id="0d9b4-181">O site do cliente é o principal meio pelo qual um objeto solicita serviços de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-181">The client site is the principal means by which an object requests services from its container.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-183">Um GUID (identificador global exclusivo) associado a um objeto de classe OLE.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-183">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="0d9b4-184">Se um objeto de classe for usado para criar mais de uma instância de um objeto, o aplicativo de servidor associado deverá registrar seu CLSID no registro do sistema para que os clientes possam localizar e carregar o código executável associado aos objetos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-184">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="0d9b4-185">Todo servidor OLE ou contêiner que permite vincular a seus objetos inseridos deve registrar um CLSID para cada definição de objeto com suporte.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-185">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**compromisso**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-187">Para salvar de forma persistente todas as alterações feitas em um objeto de armazenamento ou de fluxo desde que ele foi aberto ou alterações foram salvas pela última vez.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-187">To persistently save any changes made to a storage or stream object since it was opened or changes were last saved.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**componente**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-189">Um objeto que encapsula dados e código e fornece um conjunto bem especificado de serviços publicamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-189">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-191">O modelo de programação orientado a objeto OLE que define como os objetos interagem em um único processo ou entre processos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-191">The OLE object-oriented programming model that defines how objects interact within a single process or between processes.</span></span> <span data-ttu-id="0d9b4-192">Em COM, os clientes têm acesso a um objeto por meio de interfaces implementadas no objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-192">In COM, clients have access to an object through interfaces implemented on the object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barra de menus compostas**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**composite menu bar**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-194">Uma barra de menus compartilhada composta por grupos de menus de um aplicativo de contêiner e de um aplicativo de servidor ativado no local.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-194">A shared menu bar composed of menu groups from both a container application and an in-place-activated server application.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker composto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-196">Um moniker que consiste em dois ou mais monikers que são tratados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-196">A moniker that consists of two or more monikers that are treated as a unit.</span></span> <span data-ttu-id="0d9b4-197">Um moniker composto pode ser não genérico, o que significa que seus monikers do componente têm conhecimento especial um do outro, ou genéricos, o que significa que seus monikers do componente não sabem nada sobre um do outro, exceto que eles são monikers</span><span class="sxs-lookup"><span data-stu-id="0d9b4-197">A composite moniker can be non-generic, meaning that its component monikers have special knowledge of each other, or generic, meaning that its component monikers know nothing about each other except that they are monikers</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**documento composto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**compound document**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-199">Um documento que inclui objetos vinculados ou incorporados, bem como seus próprios dados nativos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-199">A document that includes linked or embedded objects, as well as its own native data.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**arquivo composto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**compound file**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-201">Uma implementação de armazenamento estruturado fornecida por OLE.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-201">An OLE-provided Structured Storage implementation.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Objeto COM**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-203">Um objeto que está de acordo com o Component Object Model OLE (COM).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-203">An object that conforms to the OLE Component Object Model (COM).</span></span> <span data-ttu-id="0d9b4-204">Um objeto COM é uma instância de uma definição de objeto, que especifica os dados do objeto e uma ou mais implementações de interfaces no objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-204">A COM object is an instance of an object definition, which specifies the object's data and one or more implementations of interfaces on the object.</span></span> <span data-ttu-id="0d9b4-205">Os clientes interagem com um objeto COM somente por meio de suas interfaces.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-205">Clients interact with a COM object only through its interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**objeto conectável**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**connectable object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-207">Um objeto COM que implementa, no mínimo, a interface [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) , para o gerenciamento de objetos de ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-207">A COM object that implements, at a minimum, the [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) interface, for the management of connection point objects.</span></span> <span data-ttu-id="0d9b4-208">Os objetos conectáveis dão suporte à comunicação do servidor para o cliente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-208">Connectable objects support communication from the server to the client.</span></span> <span data-ttu-id="0d9b4-209">Um objeto que pôde ser conectado cria e gerencia um ou mais subobjetos de ponto de conexão, que recebem eventos de interfaces implementadas em outros objetos e os enviam para o cliente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-209">A connectable object creates and manages one or more connection point subobjects, which receive events from interfaces implemented on other objects and send them on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**objeto de ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**connection point object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-211">Um objeto COM que é gerenciado por um objeto que pôde ser conectado e que implementa a interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-211">A COM object that is managed by a connectable object and that implements the [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) interface.</span></span> <span data-ttu-id="0d9b4-212">Um ou mais objetos de ponto de conexão podem ser criados e gerenciados por um objeto que pode ser conectado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-212">One or more connection point objects can be created and managed by a connectable object.</span></span> <span data-ttu-id="0d9b4-213">Cada objeto de ponto de conexão gerencia eventos de entrada de uma interface específica em outro objeto e envia esses eventos para o cliente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-213">Each connection point object manages incoming events from a specific interface on another object and sends those events on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**aplicativo de contêiner**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**container application**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-215">Um aplicativo que dá suporte a documentos compostos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-215">An application that supports compound documents.</span></span> <span data-ttu-id="0d9b4-216">O aplicativo de contêiner fornece armazenamento para um objeto incorporado ou vinculado, um site para sua exibição, acesso ao site de exibição e um coletor de consultoria para receber notificações de alterações no objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-216">The container application provides storage for an embedded or linked object, a site for its display, access to the display site, and an advisory sink for receiving notifications of changes in the object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**contenção**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**containment**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-218">Uma técnica de composição para implementar objetos COM.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-218">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="0d9b4-219">Ele permite que um objeto reutilize algumas ou todas as implementações de interface de um ou mais objetos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-219">It allows one object to reuse some or all of the interface implementations of one or more other objects.</span></span> <span data-ttu-id="0d9b4-220">O objeto externo atua como um cliente para os outros objetos, delegando a implementação quando quiser usar os serviços de um dos objetos contidos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-220">The outer object acts as a client to the other objects, delegating implementation when it wishes to use the services of one of the contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**noticioso**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-222">No COM+, um conjunto de propriedades de tempo de execução associadas a um ou mais objetos COM que são usados para fornecer serviços para esses objetos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-222">In COM+, a set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**controlo**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**control**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-224">Um objeto COM que pode ser inserido e reutilizável que dá suporte ao, no mínimo, à interface [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-224">An embeddable, reusable COM object that supports, at a minimum, the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) interface.</span></span> <span data-ttu-id="0d9b4-225">Normalmente, os controles são associados à interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-225">Controls are typically associated with the user interface.</span></span> <span data-ttu-id="0d9b4-226">Eles também dão suporte à comunicação com um contêiner e podem ser reutilizados por vários clientes, dependendo dos critérios de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-226">They also support communication with a container and can be reused by multiple clients, depending upon licensing criteria.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**contêiner de controle**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**control container**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-228">Um aplicativo que dá suporte à inserção de controles implementando a interface [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-228">An application that supports embedding of controls by implementing the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**Propriedade de controle**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**control property**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-230">Uma propriedade de tempo de execução que é exposta e gerenciada pelo próprio controle.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-230">A run-time property that is exposed and managed by the control itself.</span></span> <span data-ttu-id="0d9b4-231">Por exemplo, a fonte e o tamanho do texto usados pelo controle são propriedades de controle.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-231">For example, the font and text size used by the control are control properties.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlando objeto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlling object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-233">O objeto dentro de um objeto de agregação que controla quais interfaces dentro do objeto de agregação são expostos e que são privados.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-233">The object within an aggregate object that controls which interfaces within the aggregate object are exposed and which are private.</span></span> <span data-ttu-id="0d9b4-234">A interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do objeto de controle é chamada de controle **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-234">The [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the controlling object is called the controlling **IUnknown**.</span></span> <span data-ttu-id="0d9b4-235">As chamadas para métodos **IUnknown** de outros objetos na agregação devem ser passadas para o **IUnknown** de controle.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-235">Calls to **IUnknown** methods of other objects in the aggregate must be passed to the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**site de controle**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**control site**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-237">Uma estrutura implementada por um contêiner de controle para gerenciar a exibição e o armazenamento de um controle.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-237">A structure implemented by a control container for managing the display and storage of a control.</span></span> <span data-ttu-id="0d9b4-238">Dentro de um determinado contêiner, cada controle tem um site de controle correspondente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-238">Within a given container, each control has a corresponding control site.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**objeto de transferência de dados**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**data transfer object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-240">Um objeto que implementa a interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e contém dados a serem transferidos de um objeto para outro por meio das operações de arrastar e soltar da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-240">An object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface and contains data to be transferred from one object to another through either the Clipboard or drag-and-drop operations.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**manipulador de objeto padrão**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**default object handler**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-242">Uma DLL fornecida com OLE que atua como um substituto no espaço de processamento do aplicativo de contêiner para o objeto real.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-242">A DLL provided with OLE that acts as a surrogate in the processing space of the container application for the real object.</span></span>

<span data-ttu-id="0d9b4-243">Com o manipulador de objeto padrão, é possível examinar os dados armazenados de um objeto sem realmente ativar o objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-243">With the default object handler, it is possible to look at an object's stored data without actually activating the object.</span></span> <span data-ttu-id="0d9b4-244">O manipulador de objetos padrão executa outras tarefas, como a renderização de um objeto de seu estado armazenado em cache quando o objeto é carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-244">The default object handler performs other tasks, such as rendering an object from its cached state when the object is loaded into memory.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**objeto dependente**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**dependent object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-246">Um objeto COM que é normalmente inicializado por outro objeto (o objeto de host).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-246">A COM object that is typically initialized by another object (the host object).</span></span> <span data-ttu-id="0d9b4-247">Embora o tempo de vida do objeto dependente possa fazer sentido apenas durante o tempo de vida do objeto de host, o objeto de host não funciona como o [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de controle para o objeto dependente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-247">Although the dependent object's lifetime may only make sense during the lifetime of the host object, the host object does not function as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent object.</span></span> <span data-ttu-id="0d9b4-248">Por outro lado, um objeto é um objeto agregado quando seu tempo de vida (por meio de sua contagem de referência) é totalmente controlado pelo objeto de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-248">In contrast, an object is an aggregated object when its lifetime (by means of its reference count) is completely controlled by the managing object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**modo de acesso direto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**direct access mode**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-250">Um dos dois modos de acesso nos quais um objeto de armazenamento pode ser aberto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-250">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="0d9b4-251">No modo direto, todas as alterações são imediatamente confirmadas no objeto de armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-251">In direct mode, all changes are immediately committed to the root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**objeto Document**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**document object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-253">Um documento OLE que pode exibir uma ou mais exibições ativadas no local de seus dados em um quadro nativo ou estrangeiro, como um navegador, mantendo o controle total sobre a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-253">An OLE document that can display one or more in-place activated views of its data within a native or foreign frame, such as a browser, while retaining full control over its user interface.</span></span> <span data-ttu-id="0d9b4-254">Além de implementar o documento OLE comum e as interfaces de ativação in-loco, um objeto de documento deve implementar [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)e cada uma de suas exibições (na forma de um objeto de exibição de documento) deve implementar [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-254">In addition to implementing the usual OLE document and in-place activation interfaces, a document object must implement [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument), and each of its views (in the form of a document view object) must implement [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**contêiner de objeto de documento**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**document object container**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-256">Um aplicativo de contêiner capaz de exibir uma ou mais exibições de um ou mais objetos de documento e gerenciar todos os objetos de documento contidos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-256">A container application capable of displaying one or more views of one or more document objects and of managing all contained document objects within a file.</span></span> <span data-ttu-id="0d9b4-257">Cada objeto de documento é associado a um site de documento, e cada site de documento contém um ou mais sites de exibição de documento correspondentes às exibições com suporte pelo objeto Document.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-257">Each document object is associated with a document site, and each document site contains one or more document view sites corresponding to the views supported by the document object.</span></span> <span data-ttu-id="0d9b4-258">Um contêiner de objeto de documento também inclui um quadro de contêiner, que manipula a negociação de menus e barras de ferramentas e a enumeração de objetos contidos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-258">A document object container also includes a container frame, which handles menu and toolbar negotiation and the enumeration of contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**servidor de objeto de documento**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**document object server**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-260">Um aplicativo de servidor capaz de fornecer objetos de documento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-260">A server application capable of providing document objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**site do documento**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**document site**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-262">Um site do cliente implementado por um contêiner de objeto de documento para gerenciar a exibição e o armazenamento de um objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-262">A client site implemented by a document object container for managing the display and storage of a document object.</span></span> <span data-ttu-id="0d9b4-263">Cada objeto de documento em um contêiner tem um site de documento correspondente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-263">Each document object in a container has a corresponding document site.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**objeto do site do documento**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**document site object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-265">Um objeto COM que implementa a interface [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) , além das interfaces de cliente-site usuais (como [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-265">A COM object that implements the [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) interface, in addition to the usual client-site interfaces (such as [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**exibição de documento**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**document view**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-267">Uma apresentação específica dos dados de um documento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-267">A particular presentation of a document's data.</span></span> <span data-ttu-id="0d9b4-268">Um único objeto de documento pode ter uma ou mais exibições, mas uma única exibição de documento pode pertencer a um único objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-268">A single document object can have one or more views, but a single document view can belong to one and only one document object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**objeto de exibição de documento**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**document view object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-270">Um objeto COM que implementa a interface [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) e corresponde a uma determinada exibição de documento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-270">A COM object that implements the [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) interface and corresponds to a particular document view.</span></span> <span data-ttu-id="0d9b4-271">Um objeto com várias exibições de documento agrega um objeto de exibição de documento separado para cada exibição.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-271">An object with multiple document views aggregates a separate document view object for each view.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**site de exibição de documentos**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**document view site**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-273">Um objeto agregado por um objeto de site de documento para gerenciar o espaço de exibição para uma exibição específica de um objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-273">An object aggregated by a document site object for managing the display space for a particular view of a document object.</span></span> <span data-ttu-id="0d9b4-274">Em um determinado site de documento, cada exibição de documento tem um site de exibição de documento correspondente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-274">Within a given document site, each document view has a corresponding document view site.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**objeto de site de exibição de documento**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**document view site object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-276">Um objeto COM que é agregado em um objeto de site de documento e implementa a interface [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) e, opcionalmente, a interface [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-276">A COM object that is aggregated in a document site object and implements the [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) interface and, optionally, the [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**arrastar e soltar**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**drag and drop**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-278">Uma operação na qual o usuário final usa o mouse ou outro dispositivo apontador para mover dados para outro local na mesma janela ou em outra janela.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-278">An operation in which the end user uses the mouse or other pointing device to move data to another location in the same window or another window.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Incorporar**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**embed**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-280">Para inserir um objeto em um documento composto de forma a preservar os formatos de dados nativos a esse objeto e habilitá-lo a ser editado de dentro de seu contêiner usando as ferramentas expostas por seu servidor.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-280">To insert an object into a compound document in such a way as to preserve the data formats native to that object, and to enable it to be edited from within its container using tools exposed by its server.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**objeto inserido**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**embedded object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-282">Um objeto cujos dados são armazenados em um documento composto, mas o objeto é executado no espaço de processo de seu servidor.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-282">An object whose data is stored in a compound document, but the object runs in the process space of its server.</span></span> <span data-ttu-id="0d9b4-283">O manipulador de objetos padrão fornece um substituto no espaço de processamento do aplicativo de contêiner para o objeto real.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-283">The default object handler provides a surrogate in the processing space of the container application for the real object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**Propriedade estendida**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**extended property**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-285">Uma propriedade de tempo de execução, como a posição e o tamanho de um controle, que um usuário presumiria ser exposto pelo controle, mas é exposto e gerenciado pelo contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-285">A run-time property, such as a control's position and size, that a user would assume to be exposed by the control but is exposed and managed by the container.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker do arquivo**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**file moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-287">Um moniker com base em um caminho no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-287">A moniker based on a path in the file system.</span></span> <span data-ttu-id="0d9b4-288">Os identificadores de arquivo podem ser usados para identificar objetos que são salvos em seus próprios arquivos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-288">File monikers can be used to identify objects that are saved in their own files.</span></span> <span data-ttu-id="0d9b4-289">Um moniker de arquivo é um objeto COM que dá suporte à implementação fornecida pelo sistema da interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) para a classe File moniker.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-289">A file moniker is a COM object that supports the system-provided implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface for the file moniker class.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**objeto de fonte**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**font object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-291">Um objeto COM que fornece acesso a fontes Graphics Device Interface (GDI) implementando a interface [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-291">A COM object that provides access to Graphics Device Interface (GDI) fonts by implementing the [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificador de formato**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**format identifier**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-293">Um GUID que identifica uma propriedade persistente definida.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-293">A GUID that identifies a persistent property set.</span></span> <span data-ttu-id="0d9b4-294">Também conhecido como FMTID.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-294">Also referred to as FMTID.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**quadro**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-296">A parte de um aplicativo de contêiner responsável por negociar menus, teclas de aceleração, barras de ferramentas e outros elementos de interface do usuário compartilhados com um objeto COM inserido ou um objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-296">The part of a container application responsible for negotiating menus, accelerator keys, toolbars, and other shared user-interface elements with an embedded COM object or a document object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**objeto de quadro**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**frame object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-298">Um objeto COM que implementa a interface [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) e, opcionalmente, a interface [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-298">A COM object that implements the [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) interface and, optionally, the [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker composto genérico**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**generic composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-300">Uma coleção sequenciada de monikers, começando com um moniker de arquivo para fornecer o caminho de nível de documento e continuando com um ou mais monikers de item que, como um todo, identifica exclusivamente um objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-300">A sequenced collection of monikers, starting with a file moniker to provide the document-level path and continuing with one or more item monikers that, taken as a whole, uniquely identifies an object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**função auxiliar**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**helper function**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-302">Uma função que encapsula chamadas para outras funções e métodos de interface publicamente disponíveis no SDK do OLE.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-302">A function that encapsulates calls to other functions and interface methods publicly available in the OLE SDK.</span></span> <span data-ttu-id="0d9b4-303">As funções auxiliares são uma maneira conveniente de chamar sequências usadas com frequência de chamadas de função e de método que realizam tarefas comuns.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-303">Helper functions are a convenient way to call frequently used sequences of function and method calls that accomplish common tasks.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**objeto de host**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**host object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-305">Um objeto COM que forma uma relação hierárquica com um ou mais objetos COM, conhecidos como objetos dependentes.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-305">A COM object that forms a hierarchical relationship with one or more other COM objects, known as the dependent objects.</span></span> <span data-ttu-id="0d9b4-306">Normalmente, o objeto de host instancia os objetos dependentes e sua existência faz sentido dentro do tempo de vida do objeto de host.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-306">Typically, the host object instantiates the dependent objects, and their existence only makes sense within the lifetime of the host object.</span></span> <span data-ttu-id="0d9b4-307">No entanto, o objeto de host não funciona como o [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de controle para os objetos dependentes, nem é delegado diretamente às implementações de interface desses objetos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-307">However, the host object does not act as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent objects, nor does it directly delegate to the interface implementations of those objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**RESULTADO**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-309">Um identificador de resultado opaco definido como zero para um retorno bem-sucedido de uma função e diferente de zero se as informações de erro ou de status forem retornadas.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-309">An opaque result handle defined to be zero for a successful return from a function and nonzero if error or status information is returned.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**objeto de hiperlink**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**hyperlink object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-311">Um objeto COM que implementa, no mínimo, a interface [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) e atua como um link para um objeto em outro local (o destino).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-311">A COM object that implements, at a minimum, the [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) interface and acts as a link to an object at another location (the target).</span></span> <span data-ttu-id="0d9b4-312">Um hiperlink é composto de quatro partes: um moniker que identifica o local do destino; uma cadeia de caracteres para o local dentro do destino; um nome amigável, ou exibível, para o destino; e uma cadeia de caracteres que pode conter parâmetros adicionais.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-312">A hyperlink is made up of four parts: a moniker that identifies the target's location; a string for the location within the target; a friendly, or displayable, name for the target; and a string that can contain additional parameters.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contexto de procura de hiperlink**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**hyperlink browse context**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-314">Um objeto COM que implementa a interface [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) e mantém a pilha de navegação de hiperlink.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-314">A COM object that implements the [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) interface and maintains the hyperlink navigation stack.</span></span> <span data-ttu-id="0d9b4-315">O objeto de contexto de procura gerencia a janela do quadro do hiperlink e a janela do objeto de destino do hiperlink.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-315">The browse context object manages the hyperlink frame window and hyperlink target object's window.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**contêiner de hiperlink**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**hyperlink container**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-317">Um aplicativo de contêiner que dá suporte a hiperlinks implementando a interface [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e, se os objetos do contêiner podem ser destinos de outros hiperlinks, a interface [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-317">A container application that supports hyperlinks by implementing the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and, if the container's objects can be targets of other hyperlinks, the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**objeto de moldura de hiperlink**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**hyperlink frame object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-319">Um objeto COM que implementa a interface [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) e controla a navegação de nível superior e a exibição de hiperlinks para o contêiner do quadro e o servidor do destino do hiperlink.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-319">A COM object that implements the [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) interface and controls the top-level navigation and display of hyperlinks for the frame's container and the hyperlink target's server.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**objeto do site de hiperlink**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**hyperlink site object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-321">Um objeto COM que implementa a interface [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e fornece o moniker ou o identificador de interface do seu contêiner de hiperlink.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-321">A COM object that implements the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and supplies either the moniker or interface identifier of its hyperlink container.</span></span> <span data-ttu-id="0d9b4-322">Um site de hiperlink pode atender a vários hiperlinks.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-322">One hyperlink site can serve multiple hyperlinks.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**objeto de destino do hiperlink**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**hyperlink target object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-324">Um objeto COM que implementa a interface [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) e fornece seu moniker, nome amigável e outras informações que outros objetos de hiperlink usarão para navegar até ele.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-324">A COM object that implements the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface and supplies its moniker, friendly name, and other information that other hyperlink objects will use to navigate to it.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**parâmetro in**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-326">Um parâmetro que é alocado, definido e liberado pelo chamador de um método de função ou de interface.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-326">A parameter that is allocated, set, and freed by the caller of a function or interface method.</span></span> <span data-ttu-id="0d9b4-327">Um parâmetro in não é modificado pela função chamada.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-327">An in parameter is not modified by the called function.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**parâmetro in/out**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**in/out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-329">Um parâmetro que é inicialmente alocado pelo chamador de um método de função ou de interface e definido, liberado e realocado, se necessário, pelo processo que é chamado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-329">A parameter that is initially allocated by the caller of a function or interface method, and set, freed, and reallocated, if necessary, by the process that is called.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**ativação in-loco**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**in-place activation**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-331">Editar um objeto inserido dentro da janela de seu contêiner, usando as ferramentas fornecidas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-331">Editing an embedded object within the window of its container, using tools provided by the server.</span></span> <span data-ttu-id="0d9b4-332">Objetos vinculados não dão suporte à ativação in-loco; Eles são sempre editados na janela do servidor.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-332">Linked objects do not support in-place activation; they are always edited in the window of the server.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**servidor em processo**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**in-process server**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-334">Um servidor implementado como uma DLL que é executada no espaço de processo do cliente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-334">A server implemented as a DLL that runs in the process space of the client.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**cópia**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**instance**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-336">Um objeto para o qual a memória é alocada ou que é persistente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-336">An object for which memory is allocated or which is persistent.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-338">Um grupo de funções relacionadas semanticamente que fornecem acesso a um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-338">A group of semantically related functions that provide access to a COM object.</span></span> <span data-ttu-id="0d9b4-339">Cada interface OLE define um contrato que permite que os objetos interajam de acordo com o Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-339">Each OLE interface defines a contract that allows objects to interact according to the Component Object Model (COM).</span></span> <span data-ttu-id="0d9b4-340">Embora o OLE forneça muitas implementações de interface, a maioria das interfaces também pode ser implementada por desenvolvedores que projetam aplicativos OLE.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-340">While OLE provides many interface implementations, most interfaces can also be implemented by developers designing OLE applications.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificador de interface (IID)**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**interface identifier (IID)**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-342">Um GUID (identificador global exclusivo) associado a uma interface.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-342">A globally unique identifier (GUID) associated with an interface.</span></span> <span data-ttu-id="0d9b4-343">Algumas funções usam IIDs como parâmetros para permitir que o chamador especifique qual ponteiro de interface deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-343">Some functions take IIDs as parameters to allow the caller to specify which interface pointer should be returned.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker do item**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**item moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-345">Um moniker com base em uma cadeia de caracteres que identifica um objeto em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-345">A moniker based on a string that identifies an object in a container.</span></span> <span data-ttu-id="0d9b4-346">Os monikers de item podem identificar objetos menores do que um arquivo, incluindo objetos incorporados em um documento composto ou um pseudo objeto (como um intervalo de células em uma planilha).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-346">Item monikers can identify objects smaller than a file, including embedded objects in a compound document, or a pseudo-object (like a range of cells in a spreadsheet).</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licença**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licensing**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-348">Um recurso do COM que fornece controle sobre a criação de objetos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-348">A feature of COM that provides control over object creation.</span></span> <span data-ttu-id="0d9b4-349">Os objetos licenciados podem ser criados somente por clientes que estão autorizados a usá-los.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-349">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="0d9b4-350">O licenciamento é implementado em COM por meio da interface [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) e por suporte para uma chave de licença que pode ser passada em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-350">Licensing is implemented in COM through the [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**vincular objeto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**link object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-352">Um objeto COM que é criado quando um objeto COM vinculado é criado ou carregado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-352">A COM object that is created when a linked COM object is created or loaded.</span></span> <span data-ttu-id="0d9b4-353">O objeto link é fornecido pelo OLE e implementa a interface [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-353">The link object is provided by OLE and implements the [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**objeto vinculado**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**linked object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-355">Um objeto COM cujos dados de origem residem fisicamente onde ele foi inicialmente criado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-355">A COM object whose source data physically resides where it was initially created.</span></span> <span data-ttu-id="0d9b4-356">Somente um moniker que representa os dados de origem e os dados de apresentação apropriados são mantidos com o documento composto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-356">Only a moniker that represents the source data and the appropriate presentation data are kept with the compound document.</span></span> <span data-ttu-id="0d9b4-357">As alterações feitas na origem do link são refletidas automaticamente no objeto vinculado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-357">Changes made to the link source are automatically reflected in the linked object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**origem do link**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**link source**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-359">Os dados que são a origem de um objeto vinculado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-359">The data that is the source of a linked object.</span></span> <span data-ttu-id="0d9b4-360">Uma fonte de link pode ser um arquivo ou uma parte de um arquivo, como um intervalo selecionado de células dentro de um arquivo (também chamado de pseudo objeto).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-360">A link source may be a file or a portion of a file, such as a selected range of cells within a file (also called a pseudo object).</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**estado carregado**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**loaded state**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-362">O estado de um objeto depois que suas estruturas de dados são carregadas na memória e estão acessíveis para o processo do cliente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-362">The state of an object after its data structures have been loaded into memory and are accessible to the client process.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**servidor local**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**local server**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-364">Um servidor fora do processo implementado como um. Aplicativo EXE em execução no mesmo computador que o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-364">An out-of-process server implemented as an .EXE application running on the same computer as its client application.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**proprietário**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**lock**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-366">Um ponteiro mantido para-e, possivelmente, uma contagem de referência incrementada em um objeto em execução.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-366">A pointer held to-and possibly, a reference count incremented on-a running object.</span></span> <span data-ttu-id="0d9b4-367">O OLE define dois tipos de bloqueios que podem ser mantidos em um objeto: forte e fraca.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-367">OLE defines two types of locks that can be held on an object: strong and weak.</span></span> <span data-ttu-id="0d9b4-368">Para implementar um bloqueio forte, um servidor deve manter um ponteiro e uma contagem de referência, para que o objeto permaneça "bloqueado" na memória pelo menos até que o servidor chame [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-368">To implement a strong lock, a server must maintain both a pointer and a reference count, so that the object will remain "locked" in memory at least until the server calls [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="0d9b4-369">Para implementar um bloqueio fraco, o servidor mantém apenas um ponteiro para o objeto, para que o objeto possa ser destruído por outro processo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-369">To implement a weak lock, the server maintains only a pointer to the object, so that the object can be destroyed by another process.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-371">Empacotamento e envio de chamadas de método de interface entre limites de thread ou processo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-371">Packaging and sending interface method calls across thread or process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**tipo de mídia**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**media type**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-373">Uma extensão de MIME que permite a negociação de formato de dados entre um cliente e um objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-373">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Tipo de conteúdo MIME**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME content type**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-375">Uma extensão de MIME que permite a negociação de formato de dados entre um cliente e um objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-375">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**MIME (Multipurpose Internet Mail Extension)**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME)**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-377">Um protocolo de Internet originalmente desenvolvido para permitir o intercâmbio de mensagens de email com conteúdo rico em ambientes de rede, computador e email heterogêneos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-377">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, computer, and email environments.</span></span> <span data-ttu-id="0d9b4-378">Na prática, o MIME também foi adotado e estendido por aplicativos que não são de email.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-378">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-380">Um objeto que implementa a interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-380">An object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="0d9b4-381">Um moniker atua como um nome que identifica exclusivamente um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-381">A moniker acts as a name that uniquely identifies a COM object.</span></span> <span data-ttu-id="0d9b4-382">Da mesma forma que um caminho identifica um arquivo no sistema de arquivos, um moniker identifica um objeto COM no namespace do diretório.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-382">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**classe de moniker**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker class**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-384">Uma implementação da interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-384">An implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="0d9b4-385">As classes de moniker fornecidas pelo sistema incluem moniker de arquivo, monikers de item, monikers compostos genéricos, antimonikers, monikers de ponteiro e identificadores de URL.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-385">System-supplied moniker classes include file monikers, item monikers, generic composite monikers, anti-monikers, pointer monikers, and URL monikers.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**cliente de moniker**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**moniker client**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-387">Um aplicativo que usa monikers para adquirir ponteiros de interface para objetos gerenciados por outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-387">An application that uses monikers to acquire interface pointers to objects managed by another application.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**provedor de moniker**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**moniker provider**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-389">Um aplicativo que torna os monikers disponíveis que identificam os objetos que ele gerencia, para que os objetos estejam acessíveis a outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-389">An application that makes available monikers that identify the objects it manages, so that the objects are accessible to other applications.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**extensão do namespace**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-391">Um objeto COM em processo que implementa [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)e [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), que às vezes são chamados de interfaces de extensão de namespace.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-391">An in-process COM object that implements [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), and [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), which are sometimes referred to as the namespace extension interfaces.</span></span> <span data-ttu-id="0d9b4-392">Uma extensão de namespace é usada para estender o namespace do Shell ou para criar um namespace separado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-392">A namespace extension is used either to extend the shell's namespace or to create a separate namespace.</span></span> <span data-ttu-id="0d9b4-393">Os usuários primários são as caixas de diálogo do Windows Explorer e arquivo comum.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-393">Primary users are the Windows Explorer and common file dialog boxes.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**dados nativos**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**native data**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-395">Os dados usados por um aplicativo de servidor OLE ao editar um objeto inserido.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-395">The data used by an OLE server application when editing an embedded object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**objeto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-397">No OLE, uma estrutura de programação que encapsula os dados e a funcionalidade que são definidos e alocados como uma única unidade e para o qual o único acesso público é por meio das interfaces da estrutura de programação.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-397">In OLE, a programming structure encapsulating both data and functionality that are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="0d9b4-398">Um objeto COM deve dar suporte a, no mínimo, a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , que mantém a existência do objeto enquanto ele está sendo usado e fornece acesso às outras interfaces do objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-398">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**Estado do objeto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**object state**</span></span> 
</dt> <dd>

<span data-ttu-id="0d9b4-400">A relação entre um objeto de documento composto em seu contêiner e o aplicativo responsável pela criação do objeto: ativo, passivo, carregado ou em execução.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-400">The relationship between a compound document object in its container and the application responsible for the object's creation: active, passive, loaded, or running.</span></span> <span data-ttu-id="0d9b4-401">Os objetos passivos são armazenados em disco ou em um banco de dados, e o objeto não é selecionado ou ativo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-401">Passive objects are stored on disk or in a database, and the object is not selected or active.</span></span> <span data-ttu-id="0d9b4-402">No estado Loaded, as estruturas de dados do objeto foram carregadas na memória, mas não estão disponíveis para operações como edição.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-402">In the loaded state, the object's data structures have been loaded into memory, but they are not available for operations such as editing.</span></span> <span data-ttu-id="0d9b4-403">Os objetos em execução são carregados e estão disponíveis para todas as operações.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-403">Running objects are both loaded and available for all operations.</span></span> <span data-ttu-id="0d9b4-404">Os objetos ativos estão executando objetos que têm uma interface do usuário visível.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-404">Active objects are running objects that have a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nome do tipo de objeto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**object type name**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-406">Uma cadeia de caracteres de identificação exclusiva que é armazenada como parte das informações disponíveis para um objeto no banco de dados de registro.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-406">A unique identification string that is stored as part of the information available for an object in the registration database.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OleDb**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-408">A tecnologia baseada em objeto da Microsoft para compartilhar informações e serviços entre os limites do processo e do computador.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-408">Microsoft's object-based technology for sharing information and services across process and computer boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**servidor fora do processo**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**out-of-process server**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-410">Um servidor, implementado como um. EXE, que é executado fora do processo de seu cliente, seja no mesmo computador ou em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-410">A server, implemented as an .EXE application, which runs outside the process of its client, either on the same computer or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**parâmetro out**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-412">Um parâmetro out é alocado pela função que está sendo chamada e liberada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-412">An out parameter is allocated by the function being called, and freed by caller.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**estado passivo**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**passive state**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-414">O estado de um objeto COM quando ele é armazenado (em disco ou em um banco de dados).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-414">The state of a COM object when it is stored (on disk or in a database).</span></span> <span data-ttu-id="0d9b4-415">O objeto não está selecionado ou ativo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-415">The object is not selected or active.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**Propriedade persistente**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**persistent property**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-417">Informações que podem ser armazenadas de forma persistente como parte de um objeto de armazenamento, como um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-417">Information that can be stored persistently as part of a storage object such as a file or directory.</span></span> <span data-ttu-id="0d9b4-418">As propriedades persistentes são agrupadas em conjuntos de propriedades, que podem ser exibidas e editadas.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-418">Persistent properties are grouped into property sets, which can be displayed and edited.</span></span>

<span data-ttu-id="0d9b4-419">Uma propriedade persistente é diferente das propriedades de tempo de execução de objetos criados com controles OLE e tecnologias de automação, que podem ser usadas para afetar o comportamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-419">A persistent property is different from the run-time properties of objects created with OLE Controls and Automation technologies, which can be used to affect system behavior.</span></span> <span data-ttu-id="0d9b4-420">A estrutura [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) define todos os tipos válidos de propriedades persistentes, enquanto a estrutura **variante** define todos os tipos válidos de propriedades de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-420">The [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) structure defines all valid types of persistent properties, whereas the **VARIANT** structure defines all valid types of run-time properties.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**armazenamento persistente**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-422">Armazenamento de um arquivo ou objeto em uma mídia, como um sistema de arquivos ou um banco de dados, de forma que o objeto e os seus próprios arquivos persistam quando o arquivo é fechado e, em seguida, reaberto posteriormente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-422">Storage of a file or object in a medium such as a file system or database so that the object and its data persist when the file is closed and then re-opened at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**objeto de imagem**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**picture object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-424">Um objeto COM que fornece acesso a imagens GDI implementando a interface [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-424">A COM object that provides access to GDI images by implementing the [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker do ponteiro**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**pointer moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-426">Um moniker que mapeia um ponteiro de interface para um objeto na memória.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-426">A moniker that maps an interface pointer to an object in memory.</span></span> <span data-ttu-id="0d9b4-427">Enquanto a maioria dos monikers identifica objetos que podem ser armazenados de forma persistente, os moniker do ponteiro identificam objetos que não podem.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-427">Whereas most monikers identify objects that can be persistently stored, pointer monikers identify objects that cannot.</span></span> <span data-ttu-id="0d9b4-428">Eles permitem que esses objetos participem de uma operação de associação de moniker.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-428">They allow such objects to participate in a moniker binding operation.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**dados da apresentação**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**presentation data**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-430">Os dados usados por um contêiner para exibir objetos inseridos ou vinculados.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-430">The data used by a container to display embedded or linked objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbo primário**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**primary verb**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-432">A ação associada aos usuários de operação mais comuns ou preferenciais que o executa em um objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-432">The action associated with the most common or preferred operation users perform on an object.</span></span> <span data-ttu-id="0d9b4-433">O verbo primário é sempre definido como verbo zero no banco de dados de registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-433">The primary verb is always defined as verb zero in the system registration database.</span></span> <span data-ttu-id="0d9b4-434">Um verbo primário do objeto é executado clicando duas vezes no objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-434">An object's primary verb is executed by double-clicking on the object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-436">Informações associadas a um objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-436">Information that is associated with an object.</span></span> <span data-ttu-id="0d9b4-437">No OLE, as propriedades se enquadram em duas categorias: Propriedades de tempo de execução e propriedades persistentes.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-437">In OLE, properties fall into two categories: run-time properties and persistent properties.</span></span> <span data-ttu-id="0d9b4-438">As propriedades de tempo de execução geralmente são associadas a objetos de controle ou seus contêineres.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-438">Run-time properties are typically associated with control objects or their containers.</span></span> <span data-ttu-id="0d9b4-439">Por exemplo, cor do plano de fundo é uma propriedade de tempo de execução definida pelo contêiner de um controle.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-439">For example, background color is a run-time property set by a control's container.</span></span> <span data-ttu-id="0d9b4-440">As propriedades persistentes são associadas a objetos armazenados.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-440">Persistent properties are associated with stored objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**quadro de propriedade**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**property frame**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-442">O mecanismo de interface do usuário que exibe uma ou mais páginas de propriedades para um controle.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-442">The user interface mechanism that displays one or more property pages for a control.</span></span> <span data-ttu-id="0d9b4-443">O sistema de tempo de execução dos controles OLE fornece uma implementação padrão de um quadro de propriedade que pode ser acessado usando a função auxiliar [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-443">The OLE Controls run-time system provides a standard implementation of a property frame that can be accessed by using the [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) helper function.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificador de propriedade**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**property identifier**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-445">Um inteiro assinado de quatro bytes que identifica uma propriedade persistente dentro de um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-445">A four-byte signed integer that identifies a persistent property within a property set.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**página de propriedades**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**property page**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-447">Um objeto com com seu próprio CLSID que faz parte de uma interface do usuário, implementado por um controle e permite que as propriedades do controle sejam exibidas e definidas.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-447">A COM object with its own CLSID that is part of a user interface, implemented by a control, and allows the control's properties to be viewed and set.</span></span> <span data-ttu-id="0d9b4-448">Os objetos da página de propriedades implementam a interface [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-448">Property page objects implement the [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**site da página de propriedades**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**property page site**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-450">O local dentro de um quadro de propriedades onde uma página de propriedades é exibida.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-450">The location within a property frame where a property page is displayed.</span></span> <span data-ttu-id="0d9b4-451">O quadro de propriedades implementa a interface [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , que contém métodos para gerenciar os sites de cada uma das páginas de propriedades fornecidas por um controle.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-451">The property frame implements the [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) interface, which contains methods to manage the sites of each of the property pages supplied by a control.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**conjunto de propriedades**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**property set**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-453">Um grupo de propriedades relacionado logicamente que está associado a um objeto armazenado persistente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-453">A logically related group of properties that is associated with a persistently stored object.</span></span> <span data-ttu-id="0d9b4-454">Para criar, abrir, excluir ou enumerar um ou mais conjuntos de propriedades, implemente a interface [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-454">To create, open, delete, or enumerate one or more property sets, implement the [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="0d9b4-455">Se você estiver usando arquivos compostos, poderá usar a implementação do OLE dessa interface em vez de implementar seu próprio.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-455">If you are using compound files, you can use OLE's implementation of this interface rather than implementing your own.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**armazenamento de conjunto de propriedades**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**property set storage**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-457">Um objeto de armazenamento COM que mantém um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-457">A COM storage object that holds a property set.</span></span> <span data-ttu-id="0d9b4-458">Um armazenamento de conjunto de propriedades é um objeto dependente associado e gerenciado por um objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-458">A property set storage is a dependent object associated with and managed by a storage object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**folha de propriedades**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**property sheet**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-460">Um conjunto de páginas de propriedades para um ou mais objetos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-460">A set of property pages for one or more objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**acionista**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxy**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-462">Um objeto específico de interface que empacota parâmetros para essa interface em preparação para uma chamada de método remoto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-462">An interface-specific object that packages parameters for that interface in preparation for a remote method call.</span></span> <span data-ttu-id="0d9b4-463">Um proxy é executado no espaço de endereço do remetente e se comunica com um stub correspondente no espaço de endereço do destinatário.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-463">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**Gerenciador de proxy**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-465">No empacotamento padrão, um proxy que gerencia todos os proxies de interface para um único objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-465">In standard marshaling, a proxy that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo objeto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-467">Uma parte de um documento ou objeto inserido, como um intervalo de células em uma planilha, que pode ser a origem de um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-467">A portion of a document or embedded object, such as a range of cells in a spreadsheet, that can be the source for a COM object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**contagem de referência**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-469">Manter uma contagem de cada ponteiro de interface mantido em um objeto para garantir que o objeto não seja destruído antes que todas as referências a ele sejam liberadas.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-469">Keeping a count of each interface pointer held on an object to ensure that the object is not destroyed before all references to it are released.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relativo**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**relative moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-471">Um moniker que especifica o local de um objeto relativo ao local de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-471">A moniker that specifies the location of an object relative to the location of another object.</span></span> <span data-ttu-id="0d9b4-472">Um moniker relativo é análogo a um caminho relativo, como.. \\ relatório de backup \\ . old.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-472">A relative moniker is analogous to a relative path, such as ..\\backup\\report.old.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**servidor remoto**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**remote server**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-474">Um aplicativo de servidor, implementado como um EXE, em execução em um computador diferente do aplicativo cliente que o está usando.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-474">A server application, implemented as an EXE, running on a different computer from the client application using it.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**voltar**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**revert**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-476">Para descartar as alterações feitas em um objeto desde a última vez em que as alterações foram confirmadas ou o armazenamento do objeto foi aberto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-476">To discard any changes made to an object since the last time the changes were committed or the object's storage was opened.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**objeto de armazenamento raiz**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**root storage object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-478">O objeto de armazenamento mais externo em um documento.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-478">The outermost storage object in a document.</span></span> <span data-ttu-id="0d9b4-479">Um objeto de armazenamento raiz pode conter outros objetos de armazenamento e fluxo aninhados.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-479">A root storage object can contain other nested storage and stream objects.</span></span> <span data-ttu-id="0d9b4-480">Por exemplo, um documento composto é salvo em disco como uma série de objetos de armazenamento e fluxo dentro de um objeto de armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-480">For example, a compound document is saved on disk as a series of storage and stream objects within a root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**Estado de execução**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**running state**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-482">O estado de um objeto COM quando seu aplicativo de servidor está em execução e é possível acessar suas interfaces e receber notificações de alterações.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-482">The state of a COM object when its server application is running and it is possible to access its interfaces and receive notification of changes.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**executando a tabela de objetos (corrompidos)**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**running object table (ROT)**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-484">Uma tabela acessível globalmente em cada computador que controla todos os objetos COM no estado em execução que podem ser identificados por um moniker.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-484">A globally accessible table on each computer that keeps track of all COM objects in the running state that can be identified by a moniker.</span></span> <span data-ttu-id="0d9b4-485">Os provedores de moniker registram um objeto na tabela, que incrementa a contagem de referência do objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-485">Moniker providers register an object in the table, which increments the object's reference count.</span></span> <span data-ttu-id="0d9b4-486">Antes que o objeto possa ser destruído, seu moniker deve ser liberado da tabela.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-486">Before the object can be destroyed, its moniker must be released from the table.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**Propriedade de tempo de execução**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**run-time property**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-488">Informações de estado discreta associadas a um objeto de controle ou a seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-488">Discrete state information associated with a control object or its container.</span></span> <span data-ttu-id="0d9b4-489">Há três tipos de propriedades de tempo de execução: Propriedades de ambiente, propriedades de controle e propriedades estendidas.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-489">There are three types of run-time properties: ambient properties, control properties, and extended properties.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**registro automático**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**self-registration**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-491">O processo pelo qual um servidor pode executar suas próprias operações de registro.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-491">The process by which a server can perform its own registry operations.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**aplicativo de servidor**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**server application**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-493">Um aplicativo que pode criar objetos COM.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-493">An application that can create COM objects.</span></span> <span data-ttu-id="0d9b4-494">Os aplicativos de contêiner podem então ser inseridos ou vinculados a esses objetos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-494">Container applications can then embed or link to these objects.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**objeto estático**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**static object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-496">Um objeto que contém apenas uma apresentação, sem dados nativos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-496">An object that contains only a presentation, with no native data.</span></span> <span data-ttu-id="0d9b4-497">Um contêiner pode tratar um objeto estático como se fosse um objeto vinculado ou incorporado, exceto que não é possível editar um objeto estático.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-497">A container can treat a static object as though it were a linked or embedded object, except that it is not possible to edit a static object.</span></span>

<span data-ttu-id="0d9b4-498">Um objeto estático pode resultar, por exemplo, da interrupção de um link em um objeto vinculado, ou seja, o aplicativo do servidor não está disponível ou o usuário não quer que o objeto vinculado seja mais atualizado.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-498">A static object can result, for example, from the breaking of a link on a linked object-that is, the server application is unavailable, or the user doesn't want the linked object to be updated anymore.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**objeto de armazenamento**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**storage object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-500">Um objeto COM que implementa a interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-500">A COM object that implements the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="0d9b4-501">Um objeto de armazenamento contém objetos de armazenamento aninhados ou objetos de fluxo, resultando no equivalente de uma estrutura de diretório/arquivo em um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-501">A storage object contains nested storage objects or stream objects, resulting in the equivalent of a directory/file structure within a single file.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**objeto Stream**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**stream object**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-503">Um objeto COM que implementa a interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-503">A COM object that implements the [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="0d9b4-504">Um objeto Stream é análogo a um arquivo em um diretório/sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-504">A stream object is analogous to a file in a directory/file system.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Armazenamento estruturado**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Structured Storage**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-506">Tecnologia do OLE para armazenar arquivos compostos em sistemas de arquivos nativos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-506">OLE's technology for storing compound files in native file systems.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**Gerenciador**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**stub**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-508">Quando os parâmetros de um método de interface ou de uma função são empacotados em um limite de processo, o stub é um objeto específico de interface que desempacota os parâmetros de marshaling e chama o método necessário.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-508">When a function's or interface method's parameters are marshaled across a process boundary, the stub is an interface-specific object that unpackages the marshaled parameters and calls the required method.</span></span> <span data-ttu-id="0d9b4-509">O stub é executado no espaço de endereço do destinatário e se comunica com um proxy correspondente no espaço de endereço do remetente.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-509">The stub runs in the receiver's address space and communicates with a corresponding proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Gerenciador de stub**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**stub manager**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-511">Gerencia todos os stubs de interface para um único objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-511">Manages all of the interface stubs for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**chamada síncrona**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**synchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-513">Uma chamada de função que não permite que mais instruções no processo de chamada sejam executadas até que a função retorne.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-513">A function call that does not allow further instructions in the calling process to be executed until the function returns.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**registro do sistema**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**system registry**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-515">Um repositório de informações em todo o sistema com suporte no Windows, que contém informações sobre o sistema e seus aplicativos, incluindo clientes e servidores OLE.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-515">A system-wide repository of information supported by Windows, which contains information about the system and its applications, including OLE clients and servers.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**modo de acesso transacionado**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**transacted access mode**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-517">Um dos dois modos de acesso nos quais um objeto de armazenamento pode ser aberto.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-517">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="0d9b4-518">Quando aberto no modo transacionado, as alterações são armazenadas em buffers até que o objeto de armazenamento raiz confirme suas alterações.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-518">When opened in transacted mode, changes are stored in buffers until the root storage object commits its changes.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**informações de tipo**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**type information**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-520">Informações sobre a classe de um objeto fornecida por uma biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-520">Information about an object's class provided by a type library.</span></span> <span data-ttu-id="0d9b4-521">Para fornecer informações de tipo, um objeto COM implementa a interface [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-521">To provide type information, a COM object implements the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**transferência de dados uniforme**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**uniform data transfer**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-523">Um modelo para transferir dados por meio da área de transferência, arrastar e soltar ou automação.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-523">A model for transferring data through the clipboard, drag and drop, or Automation.</span></span> <span data-ttu-id="0d9b4-524">Os objetos que estão em conformidade com esse modelo implementam a interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="0d9b4-524">Objects conforming to this model implement the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="0d9b4-525">Esse modelo substitui o DDE (Dynamic Data Exchange).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-525">This model replaces DDE (dynamic data exchange).</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**desempacotamento**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-527">Desempacotamento de parâmetros que foram enviados a um proxy entre limites de processo.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-527">Unpacking parameters that have been sent to a proxy across process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**localizador de recursos universal (URL)**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**universal resource locator (URL)**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-529">O identificador usado pelo World Wide Web para os nomes e locais de objetos na Internet.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-529">The identifier used by the World Wide Web for the names and locations of objects on the Internet.</span></span> <span data-ttu-id="0d9b4-530">O OLE fornece uma classe de moniker, moniker de URL, cuja implementação pode ser usada para associar um cliente a objetos identificados por uma URL.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-530">OLE provides a moniker class, URL moniker, whose implementation can be used to bind a client to objects identified by a URL.</span></span>

</dd> <dt>

<span data-ttu-id="0d9b4-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker da URL**</span><span class="sxs-lookup"><span data-stu-id="0d9b4-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0d9b4-532">Um moniker com base em um localizador de recursos universal (URL).</span><span class="sxs-lookup"><span data-stu-id="0d9b4-532">A moniker based on a universal resource locator (URL).</span></span> <span data-ttu-id="0d9b4-533">Um cliente pode usar identificadores de URL para associar a objetos que residem na Internet.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-533">A client can use URL monikers to bind to objects that reside on the Internet.</span></span> <span data-ttu-id="0d9b4-534">A classe de moniker da URL fornecida pelo sistema dá suporte à associação síncrona e assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0d9b4-534">The system-supplied URL moniker class supports both synchronous and asynchronous binding.</span></span>

</dd> </dl>

 

 