---
title: Referência de e/s de arquivo de multimídia
description: Referência de e/s de arquivo de multimídia
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Multimídia do Windows, referência de e/s de arquivo
- multimídia, referência de e/s de arquivo
- entrada de multimídia, referência de e/s de arquivo
- referência de e/s de arquivo de multimídia
- e/s de arquivo, referência
- entrada e saída (e/s), referência
- E/s (entrada e saída), referência
- referência para e/s de arquivo de multimídia, sobre
- referência de e/s de arquivo de multimídia, sobre
- referência de e/s de arquivo, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640479"
---
# <a name="multimedia-file-io-reference"></a><span data-ttu-id="c9e2d-113">Referência de e/s de arquivo de multimídia</span><span class="sxs-lookup"><span data-stu-id="c9e2d-113">Multimedia File I/O Reference</span></span>

<span data-ttu-id="c9e2d-114">Esta seção descreve as funções, macros, mensagens e estruturas associadas à saída e entrada de arquivo multimídia.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-114">This section describes the functions, macros, messages, and structures associated with multimedia file input and output.</span></span> <span data-ttu-id="c9e2d-115">Esses elementos são agrupados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-115">These elements are grouped as follows.</span></span>

## <a name="basic-io"></a><span data-ttu-id="c9e2d-116">E/s básica</span><span class="sxs-lookup"><span data-stu-id="c9e2d-116">Basic I/O</span></span>

-   [<span data-ttu-id="c9e2d-117">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-117">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="c9e2d-118">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-118">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="c9e2d-119">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-119">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="c9e2d-120">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-120">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="c9e2d-121">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-121">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="c9e2d-122">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-122">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a><span data-ttu-id="c9e2d-123">E/s em buffer</span><span class="sxs-lookup"><span data-stu-id="c9e2d-123">Buffered I/O</span></span>

-   [<span data-ttu-id="c9e2d-124">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-124">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="c9e2d-125">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-125">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="c9e2d-126">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-126">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   <span data-ttu-id="c9e2d-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9e2d-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span></span>
-   [<span data-ttu-id="c9e2d-128">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-128">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="c9e2d-129">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-129">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a><span data-ttu-id="c9e2d-130">E/S DO RIFF</span><span class="sxs-lookup"><span data-stu-id="c9e2d-130">RIFF I/O</span></span>

-   [<span data-ttu-id="c9e2d-131">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-131">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="c9e2d-132">**MMCKINFO**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-132">**MMCKINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [<span data-ttu-id="c9e2d-133">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-133">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="c9e2d-134">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-134">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="c9e2d-135">**mmioFOURCC**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-135">**mmioFOURCC**</span></span>](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [<span data-ttu-id="c9e2d-136">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-136">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a><span data-ttu-id="c9e2d-137">Procedimentos de e/s personalizados</span><span class="sxs-lookup"><span data-stu-id="c9e2d-137">Custom I/O Procedures</span></span>

-   <span data-ttu-id="c9e2d-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9e2d-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="c9e2d-139">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-139">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="c9e2d-140">**MMIOM \_ fechar**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-140">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="c9e2d-141">**MMIOM \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-141">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="c9e2d-142">**MMIOM \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-142">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="c9e2d-143">**\_renomear MMIOM**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-143">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="c9e2d-144">**MMIOM \_ Seek**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-144">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="c9e2d-145">**MMIOM \_ gravação**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-145">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="c9e2d-146">**MMIOM \_ WRITEFLUSH**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-146">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)
-   [<span data-ttu-id="c9e2d-147">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="c9e2d-147">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a><span data-ttu-id="c9e2d-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9e2d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9e2d-149">E/s de arquivo multimídia</span><span class="sxs-lookup"><span data-stu-id="c9e2d-149">Multimedia File I/O</span></span>](multimedia-file-i-o.md)
</dt> </dl>

 

 