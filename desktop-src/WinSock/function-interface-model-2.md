---
description: O transporte e o namespace do Windows Sockets&\# 8211; os provedores de serviço são DLLs com um único ponto de entrada de procedimento exportado para a função de inicialização WSPStartup ou NSPStartup do provedor de serviço, respectivamente.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Modelo de interface de função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813714"
---
# <a name="function-interface-model"></a><span data-ttu-id="b5522-103">Modelo de interface de função</span><span class="sxs-lookup"><span data-stu-id="b5522-103">Function Interface Model</span></span>

<span data-ttu-id="b5522-104">O transporte e o namespace do Windows Sockets – provedores de serviço são DLLs com um único ponto de entrada de procedimento exportado para a função de inicialização [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) ou [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)do provedor de serviço, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b5522-104">Windows Sockets transport and namespace–service providers are DLLs with a single exported procedure entry point for the service provider initialization function [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) or [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectively.</span></span> <span data-ttu-id="b5522-105">Todas as outras funções de provedor de serviço tornam-se acessíveis para o \_32.dll Ws2 por meio da tabela de expedição do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="b5522-105">All other service provider functions are made accessible to the Ws2\_32.dll through the service provider's dispatch table.</span></span> <span data-ttu-id="b5522-106">As DLLs do provedor de serviços são carregadas na memória pelo Ws2 \_32.dll somente quando necessário e são descarregadas quando seus serviços não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="b5522-106">Service provider DLL's are loaded into memory by the Ws2\_32.dll only when needed, and are unloaded when their services are no longer required.</span></span>

<span data-ttu-id="b5522-107">O SPI também define várias circunstâncias nas quais um provedor de serviço de transporte chama o \_32.dll Ws2 (upchamadas) para obter os serviços de suporte de dll.</span><span class="sxs-lookup"><span data-stu-id="b5522-107">The SPI also defines several circumstances in which a transport service provider calls up into the Ws2\_32.dll (upcalls) to obtain DLL support services.</span></span> <span data-ttu-id="b5522-108">A DLL do provedor de serviço de transporte recebe a tabela de expedição de chamada de ws2 \_32.dll por meio do parâmetro *UpcallTable* para [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="b5522-108">The transport service provider DLL is given the Ws2\_32.dll's upcall dispatch table through the *UpcallTable* parameter to [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span>

<span data-ttu-id="b5522-109">Os provedores de serviços devem ter sua extensão de nome de arquivo alterada de "DLL" para ". WSP "ou". NSP ".</span><span class="sxs-lookup"><span data-stu-id="b5522-109">Service providers should have their file name extension changed from "DLL" to ".WSP" or ".NSP".</span></span> <span data-ttu-id="b5522-110">Esse requisito não é estrito.</span><span class="sxs-lookup"><span data-stu-id="b5522-110">This requirement is not strict.</span></span> <span data-ttu-id="b5522-111">Um provedor de serviço ainda funcionará com o \_32.dll Ws2 com qualquer extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5522-111">A service provider will still operate with the Ws2\_32.dll with any file name extension.</span></span>

<span data-ttu-id="b5522-112">A SPI do Winsock usa a seguinte convenção de nomenclatura de prefixo de função:</span><span class="sxs-lookup"><span data-stu-id="b5522-112">The Winsock SPI uses the following function prefix naming convention:</span></span>

| <span data-ttu-id="b5522-113">Prefixo</span><span class="sxs-lookup"><span data-stu-id="b5522-113">Prefix</span></span> | <span data-ttu-id="b5522-114">Significado</span><span class="sxs-lookup"><span data-stu-id="b5522-114">Meaning</span></span>                          | <span data-ttu-id="b5522-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5522-115">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="b5522-116">WSP</span><span class="sxs-lookup"><span data-stu-id="b5522-116">WSP</span></span>    | <span data-ttu-id="b5522-117">Provedor de serviços do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b5522-117">Windows Sockets Service Provider</span></span> | <span data-ttu-id="b5522-118">Pontos de entrada do provedor de serviço de transporte</span><span class="sxs-lookup"><span data-stu-id="b5522-118">Transport service provider entry points</span></span>           |
| <span data-ttu-id="b5522-119">WPU</span><span class="sxs-lookup"><span data-stu-id="b5522-119">WPU</span></span>    | <span data-ttu-id="b5522-120">Upchamada do provedor do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b5522-120">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="b5522-121">Ws2 \_ pontos de entrada de32.dll para provedores de serviço</span><span class="sxs-lookup"><span data-stu-id="b5522-121">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="b5522-122">WSC</span><span class="sxs-lookup"><span data-stu-id="b5522-122">WSC</span></span>    | <span data-ttu-id="b5522-123">Configuração do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b5522-123">Windows Sockets Configuration</span></span>    | <span data-ttu-id="b5522-124">WS2 \_ pontos de entrada de32.dll para miniaplicativos de instalação</span><span class="sxs-lookup"><span data-stu-id="b5522-124">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="b5522-125">NSP</span><span class="sxs-lookup"><span data-stu-id="b5522-125">NSP</span></span>    | <span data-ttu-id="b5522-126">Provedor de namespace</span><span class="sxs-lookup"><span data-stu-id="b5522-126">Namespace Provider</span></span>               | <span data-ttu-id="b5522-127">Pontos de entrada do provedor de namespace</span><span class="sxs-lookup"><span data-stu-id="b5522-127">Namespace provider entry points</span></span>                   |



 

<span data-ttu-id="b5522-128">Conforme descrito acima, esses pontos de entrada não são exportados (com exceção de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) e [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), mas são acessados por meio de uma troca de tabelas de expedição.</span><span class="sxs-lookup"><span data-stu-id="b5522-128">As described above, these entry points are not exported (with the exception of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) and [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), but are accessed through an exchange of dispatch tables.</span></span>

 

 



