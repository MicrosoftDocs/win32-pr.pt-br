---
description: Você pode configurar um componente a ser colocado em pool somente quando ele for gravado corretamente para dar suporte a pool. Para obter detalhes sobre esses requisitos, consulte requisitos para objetos pooling.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configurando um componente a ser agrupado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089578"
---
# <a name="configuring-a-component-to-be-pooled"></a><span data-ttu-id="05f68-104">Configurando um componente a ser agrupado</span><span class="sxs-lookup"><span data-stu-id="05f68-104">Configuring a Component to Be Pooled</span></span>

<span data-ttu-id="05f68-105">Você pode configurar um componente a ser colocado em pool somente quando ele for gravado corretamente para dar suporte a pool.</span><span class="sxs-lookup"><span data-stu-id="05f68-105">You can configure a component to be pooled only when it is correctly written to support being pooled.</span></span> <span data-ttu-id="05f68-106">Para obter detalhes sobre esses requisitos, consulte [requisitos para objetos pooling](requirements-for-poolable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="05f68-106">For details of these requirements, see [Requirements for Poolable Objects](requirements-for-poolable-objects.md).</span></span>

> [!Note]  
> <span data-ttu-id="05f68-107">Por padrão, um componente não está configurado para ser colocado em pool.</span><span class="sxs-lookup"><span data-stu-id="05f68-107">By default, a component is not configured to be pooled.</span></span>

 

<span data-ttu-id="05f68-108">Ao configurar um componente a ser agrupado, você pode especificar as seguintes propriedades para determinar como o COM+ mantém o pool:</span><span class="sxs-lookup"><span data-stu-id="05f68-108">When you configure a component to be pooled, you can specify the following properties to determine how COM+ maintains the pool:</span></span>

-   <span data-ttu-id="05f68-109">**Tamanho mínimo do pool.**</span><span class="sxs-lookup"><span data-stu-id="05f68-109">**Minimum pool size.**</span></span> <span data-ttu-id="05f68-110">Representa o número de objetos que são criados quando o aplicativo é iniciado e o número mínimo de objetos que são mantidos no pool enquanto o aplicativo está em execução.</span><span class="sxs-lookup"><span data-stu-id="05f68-110">Represents the number of objects that are created when the application starts and the minimum number of objects that are maintained in the pool while the application is running.</span></span> <span data-ttu-id="05f68-111">Se o número de objetos disponíveis no pool cair abaixo do mínimo especificado, novos objetos serão criados para atender a todas as solicitações de objeto pendentes e reabastecer o pool.</span><span class="sxs-lookup"><span data-stu-id="05f68-111">If the number of available objects in the pool drops below the specified minimum, new objects are created to meet any outstanding object requests and refill the pool.</span></span> <span data-ttu-id="05f68-112">Se o número de objetos disponíveis no pool for maior que o número mínimo, esses objetos excedentes serão destruídos durante um ciclo de limpeza.</span><span class="sxs-lookup"><span data-stu-id="05f68-112">If the number of available objects in the pool is greater than the minimum number, those surplus objects are destroyed during a clean-up cycle.</span></span>
-   <span data-ttu-id="05f68-113">**Tamanho máximo do pool.**</span><span class="sxs-lookup"><span data-stu-id="05f68-113">**Maximum pool size.**</span></span> <span data-ttu-id="05f68-114">Representa o número máximo de objetos em pool que o Gerenciador de Pooling criará, ambos usados ativamente pelos clientes e inativos no pool.</span><span class="sxs-lookup"><span data-stu-id="05f68-114">Represents the maximum number of pooled objects that the pooling manager will create, both actively used by clients and inactive in the pool.</span></span> <span data-ttu-id="05f68-115">Ao criar objetos, o Gerenciador de Pooling verifica se o tamanho máximo do pool não foi atingido e, se não tiver, o Gerenciador de pool cria uma nova instância do objeto para dispensar para o cliente.</span><span class="sxs-lookup"><span data-stu-id="05f68-115">When creating objects, the pooling manager checks to verify that the maximum pool size has not been reached and, if it hasn't, the pool manager creates a new instance of the object to dispense to the client.</span></span> <span data-ttu-id="05f68-116">Se o tamanho máximo do pool tiver sido atingido, as solicitações do cliente serão enfileiradas e receberão o primeiro objeto disponível do pool, de acordo com a primeira chegada.</span><span class="sxs-lookup"><span data-stu-id="05f68-116">If the maximum pool size has been reached, client requests will be queued and will receive the first available object from the pool on a first-come first-served basis.</span></span> <span data-ttu-id="05f68-117">As solicitações de criação de objeto atingirão o tempo limite após um período especificado.</span><span class="sxs-lookup"><span data-stu-id="05f68-117">Object creation requests will time-out after a specified period.</span></span>
-   <span data-ttu-id="05f68-118">**Tempo limite de criação (MS).**</span><span class="sxs-lookup"><span data-stu-id="05f68-118">**Creation timeout (ms).**</span></span> <span data-ttu-id="05f68-119">Especifica quanto tempo um cliente aguardará, em milissegundos, para que um objeto seja retornado do pool após uma chamada para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="05f68-119">Specifies how long a client will wait, in milliseconds, for an object to be returned from the pool after a call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="05f68-120">Se a chamada do cliente não for bem-sucedida, o erro E o \_ tempo limite serão retornados.</span><span class="sxs-lookup"><span data-stu-id="05f68-120">If the client call is unsuccessful, the error E\_TIMEOUT is returned.</span></span>

<span data-ttu-id="05f68-121">**Para definir propriedades relacionadas ao pooling**</span><span class="sxs-lookup"><span data-stu-id="05f68-121">**To set pooling-related properties**</span></span>

1.  <span data-ttu-id="05f68-122">No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="05f68-122">In the details pane of the Component Services administrative tool, right-click the component that you want to configure, and then click **Properties**.</span></span>

2.  <span data-ttu-id="05f68-123">Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .</span><span class="sxs-lookup"><span data-stu-id="05f68-123">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="05f68-124">Para habilitar o pool de objetos para o componente, marque a caixa de seleção **habilitar pool de objetos** .</span><span class="sxs-lookup"><span data-stu-id="05f68-124">To enable object pooling for the component, select the **Enable object pooling** check box.</span></span>

4.  <span data-ttu-id="05f68-125">Na caixa **tamanho mínimo do pool** , insira o número mínimo de objetos desse tipo no pool.</span><span class="sxs-lookup"><span data-stu-id="05f68-125">In the **Minimum pool size** box, enter the minimum number of objects of this type in the pool.</span></span> <span data-ttu-id="05f68-126">O pool será mantido para ter pelo menos esse número de objetos.</span><span class="sxs-lookup"><span data-stu-id="05f68-126">The pool will be maintained to have at least this many objects.</span></span>

5.  <span data-ttu-id="05f68-127">Na caixa u, insira o número máximo de objetos desse tipo no pool.</span><span class="sxs-lookup"><span data-stu-id="05f68-127">In the u box, enter the maximum number of objects of this type in the pool.</span></span> <span data-ttu-id="05f68-128">O número de objetos, ambos ativados e desativados, nunca excederá esse valor.</span><span class="sxs-lookup"><span data-stu-id="05f68-128">The number of objects, both activated and deactivated, will never exceed this value.</span></span>

6.  <span data-ttu-id="05f68-129">Na caixa **tempo limite de criação (MS)** , digite a quantidade de tempo, em milissegundos, que um cliente aguardará por um objeto em pool se um não estiver disponível imediatamente.</span><span class="sxs-lookup"><span data-stu-id="05f68-129">In the **Creation timeout (ms)** box, enter the amount of time, in milliseconds, a client will wait for a pooled object if one is not immediately available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05f68-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05f68-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05f68-131">Estatísticas de objeto de monitoramento</span><span class="sxs-lookup"><span data-stu-id="05f68-131">Monitoring Object Statistics</span></span>](monitoring-object-statistics.md)
</dt> </dl>

 

 
