---
description: O catálogo COM+ armazena atributos de aplicativo COM+, atributos de classe e atributos de nível de computador. Ele garante a consistência entre esses atributos e fornece operações comuns sobre esses atributos.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: O catálogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756665"
---
# <a name="the-com-catalog"></a><span data-ttu-id="2406f-104">O catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="2406f-104">The COM+ Catalog</span></span>

<span data-ttu-id="2406f-105">O catálogo COM+ armazena atributos de aplicativo COM+, atributos de classe e atributos de nível de computador.</span><span class="sxs-lookup"><span data-stu-id="2406f-105">The COM+ catalog stores COM+ application attributes, class attributes, and computer-level attributes.</span></span> <span data-ttu-id="2406f-106">Ele garante a consistência entre esses atributos e fornece operações comuns sobre esses atributos.</span><span class="sxs-lookup"><span data-stu-id="2406f-106">It guarantees consistency among these attributes and provides common operations on top of these attributes.</span></span>

<span data-ttu-id="2406f-107">O catálogo COM+ usa dois repositórios diferentes, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2406f-107">The COM+ catalog uses two different stores, as follows:</span></span>

-   <span data-ttu-id="2406f-108">O banco de dados de registro do COM+</span><span class="sxs-lookup"><span data-stu-id="2406f-108">The COM+ registration database</span></span>
-   <span data-ttu-id="2406f-109">O registro do Windows (**HKEY \_ classes \_ root**)</span><span class="sxs-lookup"><span data-stu-id="2406f-109">The Windows registry (**HKEY\_CLASSES\_ROOT**)</span></span>

<span data-ttu-id="2406f-110">O catálogo apresenta uma exibição lógica e unificada dessas duas lojas e as expõe por meio da biblioteca de administração do COM+.</span><span class="sxs-lookup"><span data-stu-id="2406f-110">The catalog presents a unified, logical view of these two stores and exposes them through the COM+ Administration Library.</span></span> <span data-ttu-id="2406f-111">Essa biblioteca fornece, por meio de uma linguagem de script, toda a funcionalidade da ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="2406f-111">This library provides, through a scripting language, all the functionality of the Component Services administrative tool.</span></span>

<span data-ttu-id="2406f-112">Para componentes COM existentes que não exigem novos serviços COM+, a pesquisa ocorre no registro do Windows existente.</span><span class="sxs-lookup"><span data-stu-id="2406f-112">For existing COM components that do not require any new COM+ services, lookup occurs in the existing Windows registry.</span></span> <span data-ttu-id="2406f-113">O catálogo COM+ também usa o registro do Windows para a biblioteca de tipos e o registro de proxy/stub de interface.</span><span class="sxs-lookup"><span data-stu-id="2406f-113">The COM+ catalog also uses the Windows registry for type library and interface proxy/stub registration.</span></span>

## <a name="split-registration"></a><span data-ttu-id="2406f-114">Dividir registro</span><span class="sxs-lookup"><span data-stu-id="2406f-114">Split Registration</span></span>

<span data-ttu-id="2406f-115">Para novos componentes que realmente já são componentes COM que são usados no ambiente de serviços (por exemplo, componentes do MTS), o aspecto básico de COM do registro é armazenado no registro do Windows e novos serviços e atributos (por exemplo, componentes na fila) são armazenados no banco de dados de registro do COM+.</span><span class="sxs-lookup"><span data-stu-id="2406f-115">For new components that are actually already existing COM components that are used in the services environment (for example, MTS components), the basic COM aspect of the registration is stored in the Windows registry and new services and attributes (for example, queued components) are stored in the COM+ registration database.</span></span> <span data-ttu-id="2406f-116">Isso é conhecido como um *registro de divisão*.</span><span class="sxs-lookup"><span data-stu-id="2406f-116">This is known as a *split registration*.</span></span>

<span data-ttu-id="2406f-117">Cada atributo é armazenado em apenas um local: ou o registro do Windows ou o banco de dados de registro do COM+.</span><span class="sxs-lookup"><span data-stu-id="2406f-117">Each attribute is stored in only one location: either the Windows registry or the COM+ registration database.</span></span> <span data-ttu-id="2406f-118">Os novos componentes COM são registrados exclusivamente no banco de dados de registro do COM+, com alguma duplicação no registro do Windows para que as ferramentas existentes possam usá-los.</span><span class="sxs-lookup"><span data-stu-id="2406f-118">New COM components are registered exclusively in the COM+ registration database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

## <a name="transactional-updates-to-the-catalog"></a><span data-ttu-id="2406f-119">Atualizações transacionais para o catálogo</span><span class="sxs-lookup"><span data-stu-id="2406f-119">Transactional Updates to the Catalog</span></span>

<span data-ttu-id="2406f-120">Algumas operações no catálogo são executadas de forma transacional.</span><span class="sxs-lookup"><span data-stu-id="2406f-120">Some operations on the catalog are performed in a transactional manner.</span></span> <span data-ttu-id="2406f-121">Quando você invoca a biblioteca de administração COM+ de um componente transacional, as atualizações para o banco de dados de registro do COM+ ocorrerão dentro do limite de transação do componente de chamada.</span><span class="sxs-lookup"><span data-stu-id="2406f-121">When you invoke the COM+ Administration Library from a transactional component, the updates to the COM+ registration database will take place within the calling component's transaction boundary.</span></span>

<span data-ttu-id="2406f-122">No entanto, as atualizações que envolvem alterações em outras lojas (como o sistema de arquivos e o registro do Windows) não têm garantia de serem totalmente transacionais.</span><span class="sxs-lookup"><span data-stu-id="2406f-122">However, updates that involve changes to other stores (such as the file system and Windows registry) are not guaranteed to be fully transactional.</span></span> <span data-ttu-id="2406f-123">Uma transação anulada pode deixar esses repositórios em um estado inconsistente com as alterações feitas entre si ou com o banco de dados de registro do COM+.</span><span class="sxs-lookup"><span data-stu-id="2406f-123">An aborted transaction can leave these stores in a state that is inconsistent with any changes made to one another or to the COM+ registration database.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2406f-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2406f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2406f-125">Criando pacotes de instalação para aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="2406f-125">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="2406f-126">Implantando proxies de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2406f-126">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="2406f-127">O utilitário de replicação COMREPL</span><span class="sxs-lookup"><span data-stu-id="2406f-127">The COMREPL Replication Utility</span></span>](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



