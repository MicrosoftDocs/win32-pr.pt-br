---
description: Um especialista é uma DLL (biblioteca de vínculo dinâmico) do Microsoft Win32 que analisa o tráfego de rede coletado por um NPP (provedor de pacotes de rede) e colocado em um arquivo de captura.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755070"
---
# <a name="expert"></a><span data-ttu-id="4bf23-103">Especialista</span><span class="sxs-lookup"><span data-stu-id="4bf23-103">Expert</span></span>

<span data-ttu-id="4bf23-104">Um especialista é uma DLL (biblioteca de vínculo dinâmico) do Microsoft Win32 que analisa o tráfego de rede coletado por um NPP ( [*provedor de pacotes de rede*](n.md) ) e colocado em um arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="4bf23-104">An expert is a Microsoft Win32 dynamic-link library (DLL) that analyzes network traffic collected by a [*network packet provider*](n.md) (NPP), and placed in a capture file.</span></span> <span data-ttu-id="4bf23-105">Depois que os dados são capturados e armazenados em um arquivo de captura, o especialista trabalha com um analisador, também conhecido como analisador de protocolo, para analisar os dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="4bf23-105">After the data is captured and stored in a capture file, the expert works with a parser, also referred to as a protocol parser, to analyze the data in the file.</span></span> <span data-ttu-id="4bf23-106">Por exemplo, você pode examinar os quadros do arquivo de captura e usar um [*analisador*](p.md) para reconhecer protocolos como o protocolo SMB ou TCP/IP (Transmission Control Protocol/Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="4bf23-106">For example, you can examine the frames of the capture file and use a [*parser*](p.md) to recognize protocols such as server message block (SMB), or Transmission Control Protocol/Internet Protocol (TCP/IP).</span></span>

<span data-ttu-id="4bf23-107">Você pode criar um especialista para trabalhar com todos os analisadores de Monitor de Rede e quaisquer analisadores que você criar por conta própria.</span><span class="sxs-lookup"><span data-stu-id="4bf23-107">You can design an expert to work with all of the Network Monitor parsers, and any parsers that you create yourself.</span></span>

<span data-ttu-id="4bf23-108">Depois que uma correspondência solicitada de protocolos identifica um quadro específico, o especialista extrai dados do quadro.</span><span class="sxs-lookup"><span data-stu-id="4bf23-108">After a requested match of protocols identifies a specific frame, the expert extracts data from the frame.</span></span> <span data-ttu-id="4bf23-109">Você pode programar o especialista para manipular informações em dados utilizáveis que o Monitor de Rede Visualizador de Eventos exibe.</span><span class="sxs-lookup"><span data-stu-id="4bf23-109">You can program the expert to manipulate information into usable data that the Network Monitor Event Viewer displays.</span></span>

<span data-ttu-id="4bf23-110">Você pode configurar um especialista em tempo de execução e, em seguida, usar Monitor de Rede para salvar os dados de configuração do usuário para reutilização com arquivos de captura diferentes.</span><span class="sxs-lookup"><span data-stu-id="4bf23-110">You can configure an expert at run time, and then use Network Monitor to save user configuration data for reuse with different capture files.</span></span> <span data-ttu-id="4bf23-111">Você pode usar um especialista para fornecer dados de correlação e resoluções personalizadas para usuários finais.</span><span class="sxs-lookup"><span data-stu-id="4bf23-111">You can use an expert to provide correlation data and custom resolutions for end users.</span></span> <span data-ttu-id="4bf23-112">Para obter mais informações sobre a criação de informações de configuração baseadas em HTML, consulte [página de referência de evento](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="4bf23-112">For more information about the creation of HTML-based configuration information, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="4bf23-113">Durante a instalação do Monitor de Rede, as seguintes DLLs de especialistas são instaladas no subdiretório especialistas:</span><span class="sxs-lookup"><span data-stu-id="4bf23-113">During Network Monitor setup, the following expert DLLs are installed in the Experts sub-directory:</span></span>

-   <span data-ttu-id="4bf23-114">Coalesce.dll</span><span class="sxs-lookup"><span data-stu-id="4bf23-114">Coalesce.dll</span></span>
-   <span data-ttu-id="4bf23-115">Propdist.dll</span><span class="sxs-lookup"><span data-stu-id="4bf23-115">Propdist.dll</span></span>
-   <span data-ttu-id="4bf23-116">Protdist.dll</span><span class="sxs-lookup"><span data-stu-id="4bf23-116">Protdist.dll</span></span>
-   <span data-ttu-id="4bf23-117">Resptime.dll</span><span class="sxs-lookup"><span data-stu-id="4bf23-117">Resptime.dll</span></span>
-   <span data-ttu-id="4bf23-118">Tcpipe.dll</span><span class="sxs-lookup"><span data-stu-id="4bf23-118">Tcpipe.dll</span></span>
-   <span data-ttu-id="4bf23-119">Topuser.dll</span><span class="sxs-lookup"><span data-stu-id="4bf23-119">Topuser.dll</span></span>

<span data-ttu-id="4bf23-120">Quando você inicia Monitor de Rede, a função [**DllMain**](dllmain-expert.md) cria todos os especialistas no subdiretório especialistas.</span><span class="sxs-lookup"><span data-stu-id="4bf23-120">When you start Network Monitor, the [**DllMain**](dllmain-expert.md) function builds all experts in the experts subdirectory.</span></span> <span data-ttu-id="4bf23-121">Quando o usuário seleciona **especialistas** no menu **ferramentas** da interface do usuário do monitor de rede, monitor de rede carrega as DLLs de especialistas.</span><span class="sxs-lookup"><span data-stu-id="4bf23-121">When the user selects **Experts** on the **Tools** menu of the Network Monitor UI, Network Monitor loads the expert DLLs.</span></span> <span data-ttu-id="4bf23-122">O especialista é chamado por meio do ponto de entrada do [especialista de registro](register-expert.md) para fornecer detalhes básicos sobre o especialista.</span><span class="sxs-lookup"><span data-stu-id="4bf23-122">The expert is called through the [Register Expert](register-expert.md) entry point to provide basic details about the expert.</span></span>

![caixa de diálogo especialistas no monitor de rede](images/expick.png)

<span data-ttu-id="4bf23-124">Monitor de Rede chama as seguintes funções para gerenciar o especialista:</span><span class="sxs-lookup"><span data-stu-id="4bf23-124">Network Monitor calls the following functions to manage the expert:</span></span>

-   [<span data-ttu-id="4bf23-125">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="4bf23-125">**DllMain**</span></span>](dllmain-expert.md)
-   [<span data-ttu-id="4bf23-126">**Registrar especialista**</span><span class="sxs-lookup"><span data-stu-id="4bf23-126">**Register Expert**</span></span>](register-expert.md)
-   [<span data-ttu-id="4bf23-127">**Executar**</span><span class="sxs-lookup"><span data-stu-id="4bf23-127">**Run**</span></span>](run.md)
-   [<span data-ttu-id="4bf23-128">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="4bf23-128">**Configure**</span></span>](configure.md)

<span data-ttu-id="4bf23-129">O especialista deve implementar cada uma das funções anteriores.</span><span class="sxs-lookup"><span data-stu-id="4bf23-129">The expert must implement each of the preceding functions.</span></span>

 

 



