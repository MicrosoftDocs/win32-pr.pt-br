---
title: Funções de e/s de arquivo multimídia
description: Funções de e/s de arquivo multimídia
ms.assetid: a5d51906-881f-4fe0-a988-c10776a3b40d
keywords:
- Multimídia do Windows, funções de e/s de arquivo
- multimídia, funções de e/s de arquivo
- entrada de multimídia, funções de e/s de arquivo
- funções de e/s de arquivo multimídia
- funções de e/s de arquivo
- funções de entrada e saída (e/s)
- E/s (entrada e saída), funções
- referência para funções de e/s de arquivo de multimídia
- referência de e/s de arquivo de multimídia, funções
- referência de e/s de arquivo, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62b8daf8e84953acebcca9106165f27b350ef2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499024"
---
# <a name="multimedia-file-io-functions"></a><span data-ttu-id="d3a05-113">Funções de e/s de arquivo multimídia</span><span class="sxs-lookup"><span data-stu-id="d3a05-113">Multimedia File I/O Functions</span></span>

<span data-ttu-id="d3a05-114">As funções a seguir são usadas com e/s de arquivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="d3a05-114">The following functions are used with multimedia file I/O.</span></span>

-   <span data-ttu-id="d3a05-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3a05-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="d3a05-116">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="d3a05-116">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="d3a05-117">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="d3a05-117">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="d3a05-118">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="d3a05-118">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="d3a05-119">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="d3a05-119">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="d3a05-120">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="d3a05-120">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="d3a05-121">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="d3a05-121">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="d3a05-122">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="d3a05-122">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [<span data-ttu-id="d3a05-123">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="d3a05-123">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="d3a05-124">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="d3a05-124">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="d3a05-125">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="d3a05-125">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="d3a05-126">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="d3a05-126">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="d3a05-127">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="d3a05-127">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="d3a05-128">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="d3a05-128">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)
-   [<span data-ttu-id="d3a05-129">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="d3a05-129">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="d3a05-130">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="d3a05-130">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)
-   [<span data-ttu-id="d3a05-131">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="d3a05-131">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)
-   [<span data-ttu-id="d3a05-132">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="d3a05-132">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="related-topics"></a><span data-ttu-id="d3a05-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3a05-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3a05-134">Referência de e/s de arquivo de multimídia</span><span class="sxs-lookup"><span data-stu-id="d3a05-134">Multimedia File I/O Reference</span></span>](multimedia-file-i-o-reference.md)
</dt> </dl>

 

 