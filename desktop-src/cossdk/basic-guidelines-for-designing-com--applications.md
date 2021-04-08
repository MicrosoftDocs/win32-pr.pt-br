---
description: Diretrizes básicas para criar aplicativos COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Diretrizes básicas para criar aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089377"
---
# <a name="basic-guidelines-for-designing-com-applications"></a><span data-ttu-id="c04dd-103">Diretrizes básicas para criar aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="c04dd-103">Basic Guidelines for Designing COM+ Applications</span></span>

<span data-ttu-id="c04dd-104">Para aproveitar ao máximo o COM+, há algumas diretrizes básicas que você pode usar ao criar um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="c04dd-104">To take full advantage of COM+, there are a few basic guidelines you can use when creating an application:</span></span>

-   <span data-ttu-id="c04dd-105">**Modele seu estado durável como um esquema de banco de dados, usando a ferramenta de banco de dados de sua escolha.**</span><span class="sxs-lookup"><span data-stu-id="c04dd-105">**Model your durable state as a database schema, using your database tool of choice.**</span></span> <span data-ttu-id="c04dd-106">Quase todos os aplicativos precisam manter o estado durável.</span><span class="sxs-lookup"><span data-stu-id="c04dd-106">Almost every application needs to maintain durable state.</span></span> <span data-ttu-id="c04dd-107">Os bancos de dados fornecem os serviços necessários para criar um armazenamento durável e escalonável do estado.</span><span class="sxs-lookup"><span data-stu-id="c04dd-107">Databases provide the services needed to create durable and scalable storage of state.</span></span> <span data-ttu-id="c04dd-108">Portanto, a primeira etapa na criação de um aplicativo COM+ é modelar o estado durável de seu aplicativo como um tipo de esquema de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c04dd-108">Therefore, the first step in creating a COM+ application is to model the durable state of your application as some sort of database schema.</span></span> <span data-ttu-id="c04dd-109">Na verdade, não importa qual banco de dados você usa; a maioria dos bancos de dados comerciais é compatível com o COM+.</span><span class="sxs-lookup"><span data-stu-id="c04dd-109">It doesn't really matter what database you use; most commercial databases are compatible with COM+.</span></span> <span data-ttu-id="c04dd-110">Microsoft SQL Server é um bom exemplo de uma solução que você pode usar.</span><span class="sxs-lookup"><span data-stu-id="c04dd-110">Microsoft SQL Server is a good example of one solution you could use.</span></span>

-   <span data-ttu-id="c04dd-111">**Modele a lógica do seu aplicativo COM+ como um conjunto de interfaces COM.**</span><span class="sxs-lookup"><span data-stu-id="c04dd-111">**Model the logic of your COM+ application as a set of COM interfaces.**</span></span> <span data-ttu-id="c04dd-112">Depois que você tiver um esquema que representa as informações de estado do aplicativo, modele as trocas que acontecem no aplicativo como interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="c04dd-112">Once you have a schema that represents the state information of the application, model the interchanges that happen in the application as COM interfaces.</span></span> <span data-ttu-id="c04dd-113">Essas interfaces modelarão o comportamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c04dd-113">These interfaces will model the behavior of the application.</span></span> <span data-ttu-id="c04dd-114">Esse também é o estágio de desenvolvimento quando você deve determinar quais serviços COM+ funcionam melhor para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c04dd-114">This is also the development stage when you should determine which COM+ services work best for your application.</span></span>

-   <span data-ttu-id="c04dd-115">**Criar DLLs de componentes que contêm componentes que usam o esquema de dados físicos e expõem uma exibição lógica dos dados para outros componentes (o primeiro item dessa lista), bem como componentes que são implementados em termos do modelo de dados lógicos (o segundo item nessa lista).**</span><span class="sxs-lookup"><span data-stu-id="c04dd-115">**Build component DLLs that contain components that use the physical data schema and expose a logical view of the data to other components (the first item in this list), as well as components that are implemented in terms of the logical data model (the second item in this list).**</span></span> <span data-ttu-id="c04dd-116">Depois de ter a estrutura da lógica e as informações de estado, você pode começar a escrever código e agora pode gravar componentes COM baseados em DLL que implementam as interfaces em termos do esquema definido.</span><span class="sxs-lookup"><span data-stu-id="c04dd-116">Once you have the structure of the logic and the state information, you can begin to write code and can now write DLL-based COM components that implement the interfaces in terms of the defined schema.</span></span> <span data-ttu-id="c04dd-117">Seus componentes simplesmente atuam como manipuladores para trabalhar com suas informações de banco de dados, e as DLLs de componentes permitem criar um aplicativo COM+ que funcione e que seja dimensionado com êxito.</span><span class="sxs-lookup"><span data-stu-id="c04dd-117">Your components simply act as manipulators for working with your database information, and your component DLLs enable you build a COM+ application that works and that scales successfully.</span></span>

-   <span data-ttu-id="c04dd-118">**Implante os componentes no ambiente COM+ usando os serviços COM+ que você selecionou.**</span><span class="sxs-lookup"><span data-stu-id="c04dd-118">**Deploy the components in the COM+ environment using the COM+ services you've selected.**</span></span> <span data-ttu-id="c04dd-119">Depois de criar o aplicativo, você pode implantar o aplicativo em um cluster de rede ou de servidor.</span><span class="sxs-lookup"><span data-stu-id="c04dd-119">Once you have built the application, you can then deploy the application across a network or server cluster.</span></span> <span data-ttu-id="c04dd-120">Agora você pode tomar decisões com base nos recursos disponíveis e pode personalizar cada componente para obter o máximo de desempenho.</span><span class="sxs-lookup"><span data-stu-id="c04dd-120">You can now make decisions based on resources available, and you can tailor each component for maximum performance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c04dd-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c04dd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c04dd-122">Princípios e pressuposições de design de COM+</span><span class="sxs-lookup"><span data-stu-id="c04dd-122">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="c04dd-123">Criando o aplicativo COM+ usando UML</span><span class="sxs-lookup"><span data-stu-id="c04dd-123">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="c04dd-124">Dicas de design gerais para usar o COM+</span><span class="sxs-lookup"><span data-stu-id="c04dd-124">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="c04dd-125">Otimizando interações com a camada de lógica de negócios do COM+</span><span class="sxs-lookup"><span data-stu-id="c04dd-125">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="c04dd-126">Outras ferramentas da Microsoft para a criação de aplicativos distribuídos</span><span class="sxs-lookup"><span data-stu-id="c04dd-126">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



