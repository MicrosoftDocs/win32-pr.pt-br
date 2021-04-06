---
description: O pool de aplicativos COM+ permite que processos de thread único sejam dimensionados, de forma semelhante ao modo como o pool de threads permite que os objetos single-thread sejam dimensionados.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Conceitos do pool de aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826267"
---
# <a name="com-application-pooling-concepts"></a><span data-ttu-id="0714b-103">Conceitos do pool de aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="0714b-103">COM+ Application Pooling Concepts</span></span>

<span data-ttu-id="0714b-104">O pool de aplicativos COM+ permite que processos de thread único sejam dimensionados, de forma semelhante ao modo como o pool de threads permite que os objetos single-thread sejam dimensionados.</span><span class="sxs-lookup"><span data-stu-id="0714b-104">COM+ application pooling allows single-threaded processes to scale, similar to the way that thread pooling allows single-threaded objects to scale.</span></span> <span data-ttu-id="0714b-105">O pool de aplicativos também pode ajudar a recuperar-se de falhas em processos únicos, fornecendo outros processos em execução capazes de lidar com as ativações.</span><span class="sxs-lookup"><span data-stu-id="0714b-105">Application pooling can also help recover from failures in single processes by providing other running processes able to handle activations.</span></span>

> [!Note]  
> <span data-ttu-id="0714b-106">Os aplicativos de biblioteca têm as propriedades de reciclagem e pooling de seu processo de host.</span><span class="sxs-lookup"><span data-stu-id="0714b-106">Library applications have the recycling and pooling properties of their host process.</span></span>

 

<span data-ttu-id="0714b-107">Todos os métodos da interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) dão suporte ao pooling de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0714b-107">All methods of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface support application pooling.</span></span>

<span data-ttu-id="0714b-108">O pool de aplicativos COM+ é configurável por aplicativo usando a propriedade ConcurrentApps do objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) na coleção de [**aplicativos**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="0714b-108">COM+ application pooling is configurable per application by using the ConcurrentApps property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="0714b-109">ConcurrentApps é um valor inteiro que especifica o número máximo de processos Dllhost simultâneos que devem ser iniciados para o serviço de ativações de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0714b-109">ConcurrentApps is an integer value that specifies the maximum number of simultaneous Dllhost processes that should be started to service activations for an application.</span></span> <span data-ttu-id="0714b-110">Essa propriedade pode ser definida usando a ferramenta de administração de serviços de componentes ou programaticamente.</span><span class="sxs-lookup"><span data-stu-id="0714b-110">This property can be set by using the Component Services administration tool or programmatically.</span></span>

<span data-ttu-id="0714b-111">Se a propriedade ConcurrentApps for definida como 1, que é o valor padrão, o serviço de pooling de aplicativos COM+ será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0714b-111">If the ConcurrentApps property is set to 1, which is the default value, the COM+ Application Pooling service is disabled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0714b-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0714b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0714b-113">Tarefas do pool de aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="0714b-113">COM+ Application Pooling Tasks</span></span>](com--application-pooling-tasks.md)
</dt> <dt>

[<span data-ttu-id="0714b-114">Conceitos de reciclagem de aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="0714b-114">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



