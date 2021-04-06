---
description: Os aplicativos que usam as funções Unicode e API de conjunto de caracteres geralmente usam a mesma classe de janela. O sistema operacional converte mensagens de forma transparente entre janelas de classes diferentes.
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: Tradução automática de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647066"
---
# <a name="automatic-message-translation"></a><span data-ttu-id="2f71d-104">Tradução automática de mensagens</span><span class="sxs-lookup"><span data-stu-id="2f71d-104">Automatic Message Translation</span></span>

<span data-ttu-id="2f71d-105">Os aplicativos que usam as funções Unicode e API de conjunto de caracteres geralmente usam a mesma classe de janela.</span><span class="sxs-lookup"><span data-stu-id="2f71d-105">Applications using the Unicode and character set API functions generally use the same window class.</span></span> <span data-ttu-id="2f71d-106">O sistema operacional converte mensagens de forma transparente entre janelas de classes diferentes.</span><span class="sxs-lookup"><span data-stu-id="2f71d-106">The operating system transparently translates messages between windows of different classes.</span></span>

<span data-ttu-id="2f71d-107">Uma função de janela é implementada para receber mensagens em formato Unicode ou de página de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="2f71d-107">A window function is implemented to receive messages in Unicode or Windows code page format.</span></span> <span data-ttu-id="2f71d-108">A função Window pode enviar mensagens ou chamar funções de qualquer um dos tipos.</span><span class="sxs-lookup"><span data-stu-id="2f71d-108">The window function can send messages or call functions of either type.</span></span>

<span data-ttu-id="2f71d-109">As mensagens a seguir têm argumentos de texto e estão sujeitas à tradução automática de texto.</span><span class="sxs-lookup"><span data-stu-id="2f71d-109">The following messages have text arguments and are subject to automatic text translation.</span></span> <span data-ttu-id="2f71d-110">Para obter informações sobre a tradução automática, consulte [subclasse e conversão automática de mensagens](subclassing-and-automatic-message-translation.md).</span><span class="sxs-lookup"><span data-stu-id="2f71d-110">For information about automatic translation, see [Subclassing and Automatic Message Translation](subclassing-and-automatic-message-translation.md).</span></span>

<dl>

[<span data-ttu-id="2f71d-111">AddString CB \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-111">CB\_ADDSTRING</span></span>](../controls/cb-addstring.md)  
[<span data-ttu-id="2f71d-112">\_pasta CB</span><span class="sxs-lookup"><span data-stu-id="2f71d-112">CB\_DIR</span></span>](../controls/cb-dir.md)  
[<span data-ttu-id="2f71d-113">localização da CB \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-113">CB\_FINDSTRING</span></span>](../controls/cb-findstring.md)  
[<span data-ttu-id="2f71d-114">\_GETLBTEXT CB</span><span class="sxs-lookup"><span data-stu-id="2f71d-114">CB\_GETLBTEXT</span></span>](../controls/cb-getlbtext.md)  
[<span data-ttu-id="2f71d-115">inserção de CB \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-115">CB\_INSERTSTRING</span></span>](../controls/cb-insertstring.md)  
[<span data-ttu-id="2f71d-116">seleção do CB \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-116">CB\_SELECTSTRING</span></span>](../controls/cb-selectstring.md)  
[<span data-ttu-id="2f71d-117">em \_ GETline</span><span class="sxs-lookup"><span data-stu-id="2f71d-117">EM\_GETLINE</span></span>](../controls/em-getline.md)  
[<span data-ttu-id="2f71d-118">em \_ REPLACESEL</span><span class="sxs-lookup"><span data-stu-id="2f71d-118">EM\_REPLACESEL</span></span>](../controls/em-replacesel.md)  
[<span data-ttu-id="2f71d-119">em \_ SETpasswordchar</span><span class="sxs-lookup"><span data-stu-id="2f71d-119">EM\_SETPASSWORDCHAR</span></span>](../controls/em-setpasswordchar.md)  
[<span data-ttu-id="2f71d-120">o \_ ADDfile do lb</span><span class="sxs-lookup"><span data-stu-id="2f71d-120">LB\_ADDFILE</span></span>](../controls/lb-addfile.md)  
[<span data-ttu-id="2f71d-121">seqüência de caracteres de LB \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-121">LB\_ADDSTRING</span></span>](../controls/lb-addstring.md)  
[<span data-ttu-id="2f71d-122">Dir. de LB \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-122">LB\_DIR</span></span>](../controls/lb-dir.md)  
[<span data-ttu-id="2f71d-123">Localizar LBstring \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-123">LB\_FINDSTRING</span></span>](../controls/lb-findstring.md)  
[<span data-ttu-id="2f71d-124">LB \_ GETtext</span><span class="sxs-lookup"><span data-stu-id="2f71d-124">LB\_GETTEXT</span></span>](../controls/lb-gettext.md)  
[<span data-ttu-id="2f71d-125">KG \_ InsertString</span><span class="sxs-lookup"><span data-stu-id="2f71d-125">LB\_INSERTSTRING</span></span>](../controls/lb-insertstring.md)  
[<span data-ttu-id="2f71d-126">seleção de LBstring \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-126">LB\_SELECTSTRING</span></span>](../controls/lb-selectstring.md)  
[<span data-ttu-id="2f71d-127">ASKCBFORMATNAME do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-127">WM\_ASKCBFORMATNAME</span></span>](../dataxchg/wm-askcbformatname.md)  
[<span data-ttu-id="2f71d-128">caractere do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-128">WM\_CHAR</span></span>](../inputdev/wm-char.md)  
[<span data-ttu-id="2f71d-129">CHARTOITEM do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-129">WM\_CHARTOITEM</span></span>](../controls/wm-chartoitem.md)  
[<span data-ttu-id="2f71d-130">criação do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-130">WM\_CREATE</span></span>](../winmsg/wm-create.md)  
[<span data-ttu-id="2f71d-131">DEADCHAR do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-131">WM\_DEADCHAR</span></span>](../inputdev/wm-deadchar.md)  
[<span data-ttu-id="2f71d-132">DEVMODECHANGE do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-132">WM\_DEVMODECHANGE</span></span>](../gdi/wm-devmodechange.md)  
[<span data-ttu-id="2f71d-133">WM \_ GETtext</span><span class="sxs-lookup"><span data-stu-id="2f71d-133">WM\_GETTEXT</span></span>](../winmsg/wm-gettext.md)  
[<span data-ttu-id="2f71d-134">MDICREATE do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-134">WM\_MDICREATE</span></span>](../winmsg/wm-mdicreate.md)  
[<span data-ttu-id="2f71d-135">MENUCHAR do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-135">WM\_MENUCHAR</span></span>](../menurc/wm-menuchar.md)  
[<span data-ttu-id="2f71d-136">NCCREATE do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-136">WM\_NCCREATE</span></span>](../winmsg/wm-nccreate.md)  
[<span data-ttu-id="2f71d-137">SetText do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-137">WM\_SETTEXT</span></span>](../winmsg/wm-settext.md)  
[<span data-ttu-id="2f71d-138">SYSCHAR do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-138">WM\_SYSCHAR</span></span>](../menurc/wm-syschar.md)  
[<span data-ttu-id="2f71d-139">SYSDEADCHAR do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-139">WM\_SYSDEADCHAR</span></span>](../inputdev/wm-sysdeadchar.md)  
[<span data-ttu-id="2f71d-140">WININICHANGE do WM \_</span><span class="sxs-lookup"><span data-stu-id="2f71d-140">WM\_WININICHANGE</span></span>](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="2f71d-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f71d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f71d-142">Unicode na API do Windows</span><span class="sxs-lookup"><span data-stu-id="2f71d-142">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
