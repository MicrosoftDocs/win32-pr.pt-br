---
title: Substitutos de DLL
description: Substitutos de DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814420"
---
# <a name="dll-surrogates"></a><span data-ttu-id="5ebd0-103">Substitutos de DLL</span><span class="sxs-lookup"><span data-stu-id="5ebd0-103">DLL Surrogates</span></span>

<span data-ttu-id="5ebd0-104">COM torna possível criar servidores DLL que podem ser carregados em um processo EXE substituto.</span><span class="sxs-lookup"><span data-stu-id="5ebd0-104">COM makes it possible to create DLL servers that can be loaded into a surrogate EXE process.</span></span> <span data-ttu-id="5ebd0-105">Isso combina a facilidade de escrever servidores DLL com os benefícios da implementação executável.</span><span class="sxs-lookup"><span data-stu-id="5ebd0-105">This combines the ease of writing DLL servers with the benefits of executable implementation.</span></span> <span data-ttu-id="5ebd0-106">Ferramentas de desenvolvimento como Microsoft Visual Studio facilitam a gravação de servidores DLL, mas um servidor DLL em si tem limites.</span><span class="sxs-lookup"><span data-stu-id="5ebd0-106">Development tools like Microsoft Visual Studio facilitate the writing of DLL servers, but a DLL server in itself has limits.</span></span> <span data-ttu-id="5ebd0-107">A execução do servidor DLL em um processo substituto oferece vários benefícios possíveis:</span><span class="sxs-lookup"><span data-stu-id="5ebd0-107">Running the DLL server in a surrogate process offers several possible benefits:</span></span>

-   <span data-ttu-id="5ebd0-108">Isolamento de falhas e a capacidade de atender vários clientes simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="5ebd0-108">Fault isolation and the ability to service multiple clients simultaneously.</span></span>
-   <span data-ttu-id="5ebd0-109">Em um ambiente distribuído, uma implementação de servidor DLL pode ser usada para atender a clientes remotos.</span><span class="sxs-lookup"><span data-stu-id="5ebd0-109">In a distributed environment, a DLL server implementation could be used to service remote clients.</span></span>
-   <span data-ttu-id="5ebd0-110">Ele pode permitir que os clientes se protejam contra código de servidor não confiável, permitindo que eles acessem os serviços que o servidor DLL fornece.</span><span class="sxs-lookup"><span data-stu-id="5ebd0-110">It could permit clients to help protect themselves from untrusted server code while allowing them access to the services the DLL server provides.</span></span>
-   <span data-ttu-id="5ebd0-111">A execução de um servidor DLL em um substituto fornece a DLL com a segurança do substituto.</span><span class="sxs-lookup"><span data-stu-id="5ebd0-111">Running a DLL server in a surrogate provides the DLL with the surrogate's security.</span></span>

<span data-ttu-id="5ebd0-112">O COM fornece um processo substituto padrão, ou você pode gravar um substituto personalizado se tiver necessidades especiais.</span><span class="sxs-lookup"><span data-stu-id="5ebd0-112">COM provides a default surrogate process, or you can write a custom surrogate if you have special needs.</span></span>

<span data-ttu-id="5ebd0-113">Os tópicos a seguir fornecem mais informações sobre os substitutos de DLL:</span><span class="sxs-lookup"><span data-stu-id="5ebd0-113">The following topics provide more information on DLL surrogates:</span></span>

-   [<span data-ttu-id="5ebd0-114">Requisitos do servidor DLL</span><span class="sxs-lookup"><span data-stu-id="5ebd0-114">DLL Server Requirements</span></span>](dll-server-requirements.md)
-   [<span data-ttu-id="5ebd0-115">Usando o System-Supplied substituto</span><span class="sxs-lookup"><span data-stu-id="5ebd0-115">Using the System-Supplied Surrogate</span></span>](using-the-system-supplied-surrogate.md)
-   [<span data-ttu-id="5ebd0-116">Gravando um substituto personalizado</span><span class="sxs-lookup"><span data-stu-id="5ebd0-116">Writing a Custom Surrogate</span></span>](writing-a-custom-surrogate.md)

 

 




