---
description: As DLLs TAPI, juntamente com o servidor TAPI (Tapisvr.exe), são abstrações cruciais que separam aplicativos de usuário final ou de servidor dos provedores de serviço. Uma DLL TAPI em conjunto com o servidor TAPI fornece uma interface consistente entre essas duas camadas.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: DLL TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553811"
---
# <a name="tapi-dll"></a><span data-ttu-id="5ab94-104">DLL TAPI</span><span class="sxs-lookup"><span data-stu-id="5ab94-104">TAPI DLL</span></span>

<span data-ttu-id="5ab94-105">As DLLs TAPI, juntamente com o servidor TAPI (Tapisvr.exe), são abstrações cruciais que separam aplicativos de usuário final ou de servidor dos provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="5ab94-105">The TAPI DLLs, along with the TAPI Server (Tapisvr.exe), are crucial abstractions separating end-user or server applications from service providers.</span></span> <span data-ttu-id="5ab94-106">Uma DLL TAPI em conjunto com o servidor TAPI fornece uma interface consistente entre essas duas camadas.</span><span class="sxs-lookup"><span data-stu-id="5ab94-106">A TAPI DLL in conjunction with the TAPI Server provides a consistent interface between these two layers.</span></span>

<span data-ttu-id="5ab94-107">Um aplicativo TAPI carrega a DLL apropriada em seu espaço de processo.</span><span class="sxs-lookup"><span data-stu-id="5ab94-107">A TAPI application loads the appropriate DLL into its process space.</span></span> <span data-ttu-id="5ab94-108">Durante a inicialização, a TAPI estabelece um link RPC com Tapisvr.exe.</span><span class="sxs-lookup"><span data-stu-id="5ab94-108">During initialization, TAPI establishes an RPC link with Tapisvr.exe.</span></span> <span data-ttu-id="5ab94-109">O servidor TAPI é executado no contexto de SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="5ab94-109">The TAPI Server runs in the context of SVCHOST.</span></span>

<span data-ttu-id="5ab94-110">Há três DLLs associadas à TAPI: Tapi.dll, Tapi32.dll e Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="5ab94-110">There are three DLLs associated with TAPI: Tapi.dll, Tapi32.dll, and Tapi3.dll.</span></span> <span data-ttu-id="5ab94-111">Essas DLLs estão localizadas em% SystemRoot% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="5ab94-111">These DLLs are located in %SystemRoot%\\system32.</span></span> <span data-ttu-id="5ab94-112">A figura a seguir ilustra as funções de suas respectivas funções na telefonia da Microsoft:</span><span class="sxs-lookup"><span data-stu-id="5ab94-112">The following figure illustrates the roles of their respective roles in Microsoft Telephony:</span></span>

![funções das três DLLs TAPI](images/dllserv.png)

<span data-ttu-id="5ab94-114">Os aplicativos de 16 bits existentes são vinculados a Tapi.dll.</span><span class="sxs-lookup"><span data-stu-id="5ab94-114">Existing 16-bit applications link to Tapi.dll.</span></span> <span data-ttu-id="5ab94-115">Tapi.dll é simplesmente uma camada de conversão que mapeia endereços de 16 bits para endereços de 32 bits e passa solicitações para Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="5ab94-115">Tapi.dll is simply a thunk layer that maps 16-bit addresses to 32-bit addresses and pass requests to Tapi32.dll.</span></span>

<span data-ttu-id="5ab94-116">Os aplicativos existentes da TAPI 2. x de 32 bits são vinculados a Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="5ab94-116">Existing 32-bit TAPI 2.x applications link to Tapi32.dll.</span></span> <span data-ttu-id="5ab94-117">Tapi32.dll é uma camada de Marshalling fina que transfere solicitações de função para o servidor TAPI (TAPISRV) e, quando necessário, carrega e invoca as DLLs do provedor de serviços de mídia no processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ab94-117">Tapi32.dll is a thin marshalling layer that transfers function requests to the TAPI Server (TAPISRV) and, when needed, loads and invokes media service provider DLLs in the application's process.</span></span>

<span data-ttu-id="5ab94-118">Os aplicativos TAPI 3. x são vinculados a Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="5ab94-118">TAPI 3.x applications link to Tapi3.dll.</span></span>

 

 



