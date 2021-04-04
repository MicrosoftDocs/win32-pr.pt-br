---
description: Hospedando diretamente um DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hospedando diretamente um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646189"
---
# <a name="directly-hosting-a-dmo"></a><span data-ttu-id="352dd-103">Hospedando diretamente um DMO</span><span class="sxs-lookup"><span data-stu-id="352dd-103">Directly Hosting a DMO</span></span>

<span data-ttu-id="352dd-104">Esta seção descreve como um aplicativo pode atuar como o cliente direto de um DMO.</span><span class="sxs-lookup"><span data-stu-id="352dd-104">This section describes how an application can act as the direct client of a DMO.</span></span> <span data-ttu-id="352dd-105">O aplicativo fornece a entrada para o DMO, o DMO cria a saída, e o aplicativo usa a saída para renderização, processamento adicional ou qualquer outra coisa.</span><span class="sxs-lookup"><span data-stu-id="352dd-105">The application delivers input to the DMO, the DMO creates output, and the application uses the output for rendering, further processing, or anything else.</span></span> <span data-ttu-id="352dd-106">O aplicativo é responsável por problemas como alocação de memória, tempo e sincronização e Threading.</span><span class="sxs-lookup"><span data-stu-id="352dd-106">The application is responsible for issues such as memory allocation, timing and synchronization, and threading.</span></span> <span data-ttu-id="352dd-107">Esses requisitos dependerão da natureza do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="352dd-107">These requirements will depend on the nature of the application.</span></span>

<span data-ttu-id="352dd-108">As informações nesta seção também se aplicam se você estiver escrevendo um componente que atue como uma camada entre um aplicativo e um DMO (por exemplo, um controle ActiveX que hospeda um DMO).</span><span class="sxs-lookup"><span data-stu-id="352dd-108">The information in this section also applies if you are writing a component that acts as a layer between an application and a DMO (for example, an ActiveX Control that hosts a DMO).</span></span> <span data-ttu-id="352dd-109">Além disso, você deve ler esta seção se estiver escrevendo um DMO, pois ela descreve a funcionalidade que o seu DMO deve implementar.</span><span class="sxs-lookup"><span data-stu-id="352dd-109">In addition, you should read this section if you are writing a DMO, because it describes the functionality that your DMO must implement.</span></span>

<span data-ttu-id="352dd-110">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="352dd-110">This section contains the following topics:</span></span>

-   [<span data-ttu-id="352dd-111">Definindo tipos de mídia em um DMO</span><span class="sxs-lookup"><span data-stu-id="352dd-111">Setting Media Types on a DMO</span></span>](setting-media-types-on-a-dmo.md)
-   [<span data-ttu-id="352dd-112">Processando dados em um DMO</span><span class="sxs-lookup"><span data-stu-id="352dd-112">Processing Data in a DMO</span></span>](processing-data-in-a-dmo.md)
-   [<span data-ttu-id="352dd-113">Processamento in-loco</span><span class="sxs-lookup"><span data-stu-id="352dd-113">In-Place Processing</span></span>](in-place-processing.md)
-   [<span data-ttu-id="352dd-114">Fluxos opcionais</span><span class="sxs-lookup"><span data-stu-id="352dd-114">Optional Streams</span></span>](optional-streams.md)
-   [<span data-ttu-id="352dd-115">Implementando IMediaBuffer</span><span class="sxs-lookup"><span data-stu-id="352dd-115">Implementing IMediaBuffer</span></span>](implementing-imediabuffer.md)

## <a name="related-topics"></a><span data-ttu-id="352dd-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="352dd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="352dd-117">Usando DMOs</span><span class="sxs-lookup"><span data-stu-id="352dd-117">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



