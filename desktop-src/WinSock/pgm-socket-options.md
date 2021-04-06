---
description: O PGM usa opções de soquete para definir o estado, fornecer parâmetros de multicast e, de outra forma, implementar seus recursos de multicast.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Opções de soquete PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827102"
---
# <a name="pgm-socket-options"></a><span data-ttu-id="42ba6-103">Opções de soquete PGM</span><span class="sxs-lookup"><span data-stu-id="42ba6-103">PGM Socket Options</span></span>

<span data-ttu-id="42ba6-104">O PGM usa opções de soquete para definir o estado, fornecer parâmetros de multicast e, de outra forma, implementar seus recursos de multicast.</span><span class="sxs-lookup"><span data-stu-id="42ba6-104">PGM uses socket options to set state, provide multicast parameters, and otherwise implement its multicast capabilities.</span></span> <span data-ttu-id="42ba6-105">Esta página especifica como as opções de soquete PGM devem ser definidas, enumera as opções de soquete disponíveis para PGM e, quando apropriado, fornece exemplos de uso e informações adicionais para várias opções.</span><span class="sxs-lookup"><span data-stu-id="42ba6-105">This page specifies how PGM socket options should be set, enumerates the socket options available for PGM, and where appropriate, provides usage examples and additional information for various options.</span></span> <span data-ttu-id="42ba6-106">Para obter as definições básicas de cada opção de soquete PCM, consulte [Opções de soquete](socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="42ba6-106">For basic definitions of each PCM socket option, see [Socket Options](socket-options.md).</span></span>

<span data-ttu-id="42ba6-107">**Windows XP:** Não há suporte para a programação de multicast confiável (PGM).</span><span class="sxs-lookup"><span data-stu-id="42ba6-107">**Windows XP:** Reliable Multicast Programming (PGM) is not supported.</span></span>

<span data-ttu-id="42ba6-108">As seguintes opções de soquete estão disponíveis para os remetentes do PGM:</span><span class="sxs-lookup"><span data-stu-id="42ba6-108">The following socket options are available for PGM senders:</span></span>

<dl> <span data-ttu-id="42ba6-109">\_LATEJOIN RM</span><span class="sxs-lookup"><span data-stu-id="42ba6-109">RM\_LATEJOIN</span></span>  
<span data-ttu-id="42ba6-110">\_tamanho da \_ janela de taxa do RM \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-110">RM\_RATE\_WINDOW\_SIZE</span></span>  
<span data-ttu-id="42ba6-111">\_taxa de \_ avçd da janela de envio do RM \_ \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-111">RM\_SEND\_WINDOW\_ADV\_RATE</span></span>  
<span data-ttu-id="42ba6-112">\_estatísticas do remetente do RM \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-112">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="42ba6-113">\_ \_ método Advance da janela do remetente do \_ RM \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-113">RM\_SENDER\_WINDOW\_ADVANCE\_METHOD</span></span>  
<span data-ttu-id="42ba6-114">\_ \_ mcast TTL do conjunto do RM \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-114">RM\_SET\_MCAST\_TTL</span></span>  
<span data-ttu-id="42ba6-115">\_limite de \_ mensagem do conjunto do RM \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-115">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="42ba6-116">RM \_ set \_ Send \_ If</span><span class="sxs-lookup"><span data-stu-id="42ba6-116">RM\_SET\_SEND\_IF</span></span>  
<span data-ttu-id="42ba6-117">RM \_ usar \_ FEC</span><span class="sxs-lookup"><span data-stu-id="42ba6-117">RM\_USE\_FEC</span></span>  
</dl>

<span data-ttu-id="42ba6-118">A \_ opção método Advance de janela do remetente do RM \_ \_ \_ especifica o método usado ao avançar a janela de envio de borda à direita.</span><span class="sxs-lookup"><span data-stu-id="42ba6-118">The RM\_SENDER\_WINDOW\_ADVANCE\_METHOD option specifies the method used when advancing the trailing edge send window.</span></span> <span data-ttu-id="42ba6-119">O parâmetro optval só pode ser E \_ \_ de janela antecipada \_ por \_ hora (o padrão).</span><span class="sxs-lookup"><span data-stu-id="42ba6-119">The optval parameter can only be E\_WINDOW\_ADVANCE\_BY\_TIME (the default).</span></span> <span data-ttu-id="42ba6-120">Observe que \_ \_ \_ \_ \_ não há suporte para o uso da janela e como cache de dados.</span><span class="sxs-lookup"><span data-stu-id="42ba6-120">Note that E\_WINDOW\_USE\_AS\_DATA\_CACHE is not supported.</span></span>

<span data-ttu-id="42ba6-121">As seguintes opções de soquete estão disponíveis para receptores PGM:</span><span class="sxs-lookup"><span data-stu-id="42ba6-121">The following socket options are available for PGM receivers:</span></span>

<dl> <span data-ttu-id="42ba6-122">\_Adicionar recebimento de RM \_ \_ If</span><span class="sxs-lookup"><span data-stu-id="42ba6-122">RM\_ADD\_RECEIVE\_IF</span></span>  
<span data-ttu-id="42ba6-123">recebimento do RM \_ del \_ \_ se</span><span class="sxs-lookup"><span data-stu-id="42ba6-123">RM\_DEL\_RECEIVE\_IF</span></span>  
<span data-ttu-id="42ba6-124">\_consentimento de intranet de alta velocidade do RM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-124">RM\_HIGH\_SPEED\_INTRANET\_OPT</span></span>  
<span data-ttu-id="42ba6-125">\_estatísticas do receptor do RM \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-125">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

## <a name="setting-pgm-socket-options"></a><span data-ttu-id="42ba6-126">Definindo opções de soquete PGM</span><span class="sxs-lookup"><span data-stu-id="42ba6-126">Setting PGM Socket Options</span></span>

<span data-ttu-id="42ba6-127">O trecho de código a seguir ilustra uma diretriz de programação para definir opções de soquete PGM:</span><span class="sxs-lookup"><span data-stu-id="42ba6-127">The following code snippet illustrates a programming guideline for setting PGM socket options:</span></span>


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



<span data-ttu-id="42ba6-128">No trecho acima, o tipo e o conteúdo de *OptionData* são dependentes da opção de soquete que está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="42ba6-128">In the snippet above, the type and contents of *OptionData* are dependent on the socket option being set.</span></span> <span data-ttu-id="42ba6-129">Para todas as opções de soquete PGM, o nível de soquete é IPPROTO \_ RM.</span><span class="sxs-lookup"><span data-stu-id="42ba6-129">For all PGM socket options, the socket level is IPPROTO\_RM.</span></span> <span data-ttu-id="42ba6-130">As opções de soquete PGM devem ser definidas imediatamente após a chamada para a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) , com as seguintes exceções:</span><span class="sxs-lookup"><span data-stu-id="42ba6-130">PGM socket options must be set immediately following the call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, with the following exceptions:</span></span>

<dl> <span data-ttu-id="42ba6-131">\_limite de \_ mensagem do conjunto do RM \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-131">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="42ba6-132">\_estatísticas do remetente do RM \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-132">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="42ba6-133">\_estatísticas do receptor do RM \_</span><span class="sxs-lookup"><span data-stu-id="42ba6-133">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

 

 



