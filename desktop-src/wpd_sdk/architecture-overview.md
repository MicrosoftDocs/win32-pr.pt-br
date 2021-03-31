---
description: Visão geral da arquitetura
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Visão geral da arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837015"
---
# <a name="architecture-overview"></a><span data-ttu-id="16f86-103">Visão geral da arquitetura</span><span class="sxs-lookup"><span data-stu-id="16f86-103">Architecture Overview</span></span>

<span data-ttu-id="16f86-104">A arquitetura WPD pode ser dividida em três processos.</span><span class="sxs-lookup"><span data-stu-id="16f86-104">The WPD architecture can be divided into three processes.</span></span> <span data-ttu-id="16f86-105">Dentro desses processos estão os três principais componentes de WPD: a API, o serializador e o driver.</span><span class="sxs-lookup"><span data-stu-id="16f86-105">Within these processes are the three primary components of WPD: the API, the serializer, and the driver.</span></span> <span data-ttu-id="16f86-106">A ilustração a seguir descreve os processos e componentes que constituem a arquitetura WPD.</span><span class="sxs-lookup"><span data-stu-id="16f86-106">The following illustration depicts the processes and components that constitute the WPD architecture.</span></span>

![ilustração mostrando componentes de API, serializador e driver de WPD](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a><span data-ttu-id="16f86-108">A interface de programação de aplicativos WPD</span><span class="sxs-lookup"><span data-stu-id="16f86-108">The WPD Application Programming Interface</span></span>

<span data-ttu-id="16f86-109">A API WPD é implementada como um servidor COM em processamento.</span><span class="sxs-lookup"><span data-stu-id="16f86-109">The WPD API is implemented as an in-proc COM server.</span></span> <span data-ttu-id="16f86-110">A API usa APIs padrão do Microsoft Win32 para se comunicar com o driver WPD apropriado.</span><span class="sxs-lookup"><span data-stu-id="16f86-110">The API uses standard Microsoft Win32 APIs to communicate with the appropriate WPD driver.</span></span> <span data-ttu-id="16f86-111">Um componente chamado de serializador WPD é usado por ambos os objetos de API e pelo driver para empacotar ou desempacotar parâmetros para ou do Windows Driver Foundation (WDF)-buffers do UMDF (estrutura de driver de modo de usuário).</span><span class="sxs-lookup"><span data-stu-id="16f86-111">A component called the WPD serializer is used by both API objects and the driver to pack or unpack parameters to or from Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) buffers.</span></span>

## <a name="the-wpd-serializer"></a><span data-ttu-id="16f86-112">O serializador WPD</span><span class="sxs-lookup"><span data-stu-id="16f86-112">The WPD Serializer</span></span>

<span data-ttu-id="16f86-113">O serializador WPD é implementado como um servidor COM em processamento.</span><span class="sxs-lookup"><span data-stu-id="16f86-113">The WPD serializer is implemented as an in-proc COM server.</span></span> <span data-ttu-id="16f86-114">A API WPD usa o serializador para empacotar comandos e parâmetros em buffers de mensagens que são enviados para o driver.</span><span class="sxs-lookup"><span data-stu-id="16f86-114">The WPD API uses the serializer to pack commands and parameters into message buffers that are sent to the driver.</span></span> <span data-ttu-id="16f86-115">O driver usa o serializador para desempacotar esses buffers de mensagens para processamento.</span><span class="sxs-lookup"><span data-stu-id="16f86-115">The driver uses the serializer to unpack these message buffers for processing.</span></span> <span data-ttu-id="16f86-116">O driver também usa o serializador para empacotar dados e parâmetros em buffers de resposta que são retornados para a API WPD, e a API WPD usa o serializador para desempacotar esses buffers de resposta para retornar aos chamadores.</span><span class="sxs-lookup"><span data-stu-id="16f86-116">The driver also uses the serializer to pack data and parameters into response buffers that are returned to the WPD API, and the WPD API uses the serializer to unpack these response buffers to return to callers.</span></span>

## <a name="wpd-driver"></a><span data-ttu-id="16f86-117">Driver WPD</span><span class="sxs-lookup"><span data-stu-id="16f86-117">WPD Driver</span></span>

<span data-ttu-id="16f86-118">O driver WPD é implementado como um driver padrão de estrutura de driver de modo de usuário (WDF) do Windows Driver Foundation (UMDF).</span><span class="sxs-lookup"><span data-stu-id="16f86-118">The WPD driver is implemented as a standard Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) driver.</span></span> <span data-ttu-id="16f86-119">Os drivers WPD são hospedados pelo UMDF em um processo separado chamado host do driver.</span><span class="sxs-lookup"><span data-stu-id="16f86-119">WPD drivers are hosted by UMDF in a separate process called the Driver Host.</span></span>

<span data-ttu-id="16f86-120">O driver recebe mensagens do refletor UMDF (isso não é mostrado no diagrama, já que o modo como os buffers são recebidos não é importante para o driver.</span><span class="sxs-lookup"><span data-stu-id="16f86-120">The driver receives messages from the UMDF reflector (this is not shown in the diagram, since how the buffers are received is not important to the driver.</span></span> <span data-ttu-id="16f86-121">Consulte a documentação do UMDF para obter mais informações).</span><span class="sxs-lookup"><span data-stu-id="16f86-121">See UMDF documentation for more information).</span></span> <span data-ttu-id="16f86-122">O Driver implementa um manipulador IOCL (código de controle de e/s específico de WPD) para processar as mensagens WPD recebidas pela API WPD.</span><span class="sxs-lookup"><span data-stu-id="16f86-122">The driver implements a WPD-specific I/O Control code (IOCL) handler to process WPD messages received by the WPD API.</span></span> <span data-ttu-id="16f86-123">O driver usa o serializador WPD para desempacotar comandos e parâmetros desses buffers de mensagens e para empacotar a resposta no buffer de retorno.</span><span class="sxs-lookup"><span data-stu-id="16f86-123">The driver uses the WPD serializer to unpack commands and parameters from these message buffers, and to pack the response into the return buffer.</span></span>

<span data-ttu-id="16f86-124">Os drivers WPD podem se comunicar com seus dispositivos passando por um driver de modo kernel, normalmente acessado por meio de operações de arquivo Win32 (ou seja, CreateFile, ReadFile, WriteFile e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="16f86-124">WPD drivers may communicate with their devices by going through a kernel-mode driver, typically accessed via Win32 file operations (that is, CreateFile, ReadFile, WriteFile, and so on).</span></span> <span data-ttu-id="16f86-125">Para os barramentos comuns, a Microsoft fornecerá drivers de kernel padrão para os fornecedores usarem, o que permitirá que os fornecedores enviem uma solução de driver somente de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="16f86-125">For the common buses, Microsoft will provide standard kernel drivers for vendors to use, which will allow vendors to ship a user-mode-only driver solution.</span></span> <span data-ttu-id="16f86-126">Além disso, para os dispositivos MTP (protocolo de transferência de mídia) e MSC (classe de armazenamento em massa), a Microsoft fornecerá drivers de classe WPD.</span><span class="sxs-lookup"><span data-stu-id="16f86-126">In addition, for Media Transfer Protocol (MTP) and Mass Storage Class (MSC) devices, Microsoft will provide WPD class drivers.</span></span>

<span data-ttu-id="16f86-127">Para obter mais informações sobre drivers WPD, consulte a documentação do driver de dispositivos portáteis do Windows no kit de driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="16f86-127">For more information about WPD drivers, see the Windows Portable Devices Driver documentation in the Windows Driver Kit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16f86-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16f86-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16f86-129">**Visão geral do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="16f86-129">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



