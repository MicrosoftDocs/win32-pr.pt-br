---
title: Referência de MCI
description: Referência de MCI
ms.assetid: e7cedfc2-ce01-481c-a431-c93c97d45baf
keywords:
- Referência de MCI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cc54f69e714960d189567e759cf4b254275807
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105779615"
---
# <a name="mci-reference"></a><span data-ttu-id="7e0f5-104">Referência de MCI</span><span class="sxs-lookup"><span data-stu-id="7e0f5-104">MCI Reference</span></span>

<span data-ttu-id="7e0f5-105">Esta seção lista as funções MCI, estruturas, mensagens, macros, comandos e cadeias de caracteres de comando, que estão documentadas em [referência de multimídia](multimedia-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7e0f5-105">This section lists the MCI functions, structures, messages, macros, commands, and command strings, which are documented under [Multimedia Reference](multimedia-reference.md).</span></span> <span data-ttu-id="7e0f5-106">Esses elementos são agrupados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="7e0f5-106">These elements are grouped as follows.</span></span>

## <a name="notifications"></a><span data-ttu-id="7e0f5-107">Notificações</span><span class="sxs-lookup"><span data-stu-id="7e0f5-107">Notifications</span></span>

-   [<span data-ttu-id="7e0f5-108">**\_MCINOTIFY mm**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-108">**MM\_MCINOTIFY**</span></span>](mm-mcinotify.md)
-   [<span data-ttu-id="7e0f5-109">**\_MCISIGNAL mm**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-109">**MM\_MCISIGNAL**</span></span>](mm-mcisignal.md)

## <a name="getting-information"></a><span data-ttu-id="7e0f5-110">Obtendo informações</span><span class="sxs-lookup"><span data-stu-id="7e0f5-110">Getting Information</span></span>

-   <span data-ttu-id="7e0f5-111">[**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-111">[**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-112">[**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-112">[**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-113">[**mciGetDeviceIDFromElementID**](/previous-versions//dd757157(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-113">[**mciGetDeviceIDFromElementID**](/previous-versions//dd757157(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-114">[**mciGetErrorString**](/previous-versions//dd757158(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-114">[**mciGetErrorString**](/previous-versions//dd757158(v=vs.85))</span></span>

## <a name="sending-commands"></a><span data-ttu-id="7e0f5-115">Enviando comandos</span><span class="sxs-lookup"><span data-stu-id="7e0f5-115">Sending Commands</span></span>

-   <span data-ttu-id="7e0f5-116">[**mciExecute**](/previous-versions//dd757154(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-116">[**mciExecute**](/previous-versions//dd757154(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-117">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-117">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-118">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-118">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>

## <a name="time-formats"></a><span data-ttu-id="7e0f5-119">Formatos de hora</span><span class="sxs-lookup"><span data-stu-id="7e0f5-119">Time Formats</span></span>

-   [<span data-ttu-id="7e0f5-120">**\_hora de HMS MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-120">**MCI\_HMS\_HOUR**</span></span>](mci-hms-hour.md)
-   [<span data-ttu-id="7e0f5-121">**\_HMS \_ minutos MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-121">**MCI\_HMS\_MINUTE**</span></span>](mci-hms-minute.md)
-   [<span data-ttu-id="7e0f5-122">**MCI \_ HMS \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-122">**MCI\_HMS\_SECOND**</span></span>](mci-hms-second.md)
-   [<span data-ttu-id="7e0f5-123">**\_HMS de make MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-123">**MCI\_MAKE\_HMS**</span></span>](mci-make-hms.md)
-   [<span data-ttu-id="7e0f5-124">**\_criar \_ MSF do MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-124">**MCI\_MAKE\_MSF**</span></span>](mci-make-msf.md)
-   [<span data-ttu-id="7e0f5-125">**\_TMSF de make MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-125">**MCI\_MAKE\_TMSF**</span></span>](mci-make-tmsf.md)
-   <span data-ttu-id="7e0f5-126">[**\_quadro do MSF do MCI \_**](/previous-versions//dd743438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-126">[**MCI\_MSF\_FRAME**](/previous-versions//dd743438(v=vs.85))</span></span>
-   [<span data-ttu-id="7e0f5-127">**\_minuto do MSF do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-127">**MCI\_MSF\_MINUTE**</span></span>](mci-msf-minute.md)
-   [<span data-ttu-id="7e0f5-128">**MSF do MCI \_ \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-128">**MCI\_MSF\_SECOND**</span></span>](mci-msf-second.md)
-   [<span data-ttu-id="7e0f5-129">**\_quadro TMSF \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-129">**MCI\_TMSF\_FRAME**</span></span>](mci-tmsf-frame.md)
-   [<span data-ttu-id="7e0f5-130">**\_TMSF \_ minutos MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-130">**MCI\_TMSF\_MINUTE**</span></span>](mci-tmsf-minute.md)
-   [<span data-ttu-id="7e0f5-131">**MCI \_ TMSF \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-131">**MCI\_TMSF\_SECOND**</span></span>](mci-tmsf-second.md)
-   [<span data-ttu-id="7e0f5-132">**\_faixa de TMSF MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-132">**MCI\_TMSF\_TRACK**</span></span>](mci-tmsf-track.md)

## <a name="yield-procedures"></a><span data-ttu-id="7e0f5-133">Gerar procedimentos</span><span class="sxs-lookup"><span data-stu-id="7e0f5-133">Yield Procedures</span></span>

-   <span data-ttu-id="7e0f5-134">[**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-134">[**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-135">[**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-135">[**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85))</span></span>

## <a name="configuring-a-device"></a><span data-ttu-id="7e0f5-136">Configurando um dispositivo</span><span class="sxs-lookup"><span data-stu-id="7e0f5-136">Configuring a Device</span></span>

-   [<span data-ttu-id="7e0f5-137">**interrupção**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-137">**break**</span></span>](break.md)
-   [<span data-ttu-id="7e0f5-138">**configurar**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-138">**configure**</span></span>](configure.md)
-   [<span data-ttu-id="7e0f5-139">fuga</span><span class="sxs-lookup"><span data-stu-id="7e0f5-139">escape</span></span>](escape.md)
-   [<span data-ttu-id="7e0f5-140">**index**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-140">**index**</span></span>](./windows-multimedia-start-page.md)
-   [<span data-ttu-id="7e0f5-141">**interrupção de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-141">**MCI\_BREAK**</span></span>](mci-break.md)
-   [<span data-ttu-id="7e0f5-142">**\_parâmetros de interrupção MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-142">**MCI\_BREAK\_PARMS**</span></span>](mci-break-parms.md)
-   [<span data-ttu-id="7e0f5-143">**configurar o MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-143">**MCI\_CONFIGURE**</span></span>](mci-configure.md)
-   [<span data-ttu-id="7e0f5-144">**\_parâmetros de \_ conjunto MCI DGV \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-144">**MCI\_DGV\_SET\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms)
-   [<span data-ttu-id="7e0f5-145">**\_parâmetros de \_ áudio DGV \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-145">**MCI\_DGV\_SETAUDIO\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa)
-   [<span data-ttu-id="7e0f5-146">**\_parâmetros de \_ vídeo DGV \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-146">**MCI\_DGV\_SETVIDEO\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa)
-   [<span data-ttu-id="7e0f5-147">**\_escape MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-147">**MCI\_ESCAPE**</span></span>](mci-escape.md)
-   [<span data-ttu-id="7e0f5-148">**\_índice MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-148">**MCI\_INDEX**</span></span>](mci-index.md)
-   [<span data-ttu-id="7e0f5-149">**\_parâmetros de \_ conjunto de Seq MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-149">**MCI\_SEQ\_SET\_PARMS**</span></span>](mci-seq-set-parms.md)
-   [<span data-ttu-id="7e0f5-150">**conjunto de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-150">**MCI\_SET**</span></span>](mci-set.md)
-   [<span data-ttu-id="7e0f5-151">**\_parâmetros do conjunto MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-151">**MCI\_SET\_PARMS**</span></span>](mci-set-parms.md)
-   [<span data-ttu-id="7e0f5-152">**\_áudio MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-152">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
-   [<span data-ttu-id="7e0f5-153">**MCI \_ SETcode**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-153">**MCI\_SETTIMECODE**</span></span>](mci-settimecode.md)
-   [<span data-ttu-id="7e0f5-154">**setajuster do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-154">**MCI\_SETTUNER**</span></span>](mci-settuner.md)
-   [<span data-ttu-id="7e0f5-155">**VÍDEO do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-155">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
-   [<span data-ttu-id="7e0f5-156">**rotação do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-156">**MCI\_SPIN**</span></span>](mci-spin.md)
-   [<span data-ttu-id="7e0f5-157">**\_parâmetros de \_ conjunto de VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-157">**MCI\_VCR\_SET\_PARMS**</span></span>](mci-vcr-set-parms.md)
-   [<span data-ttu-id="7e0f5-158">**\_parâmetros de \_ áudio do VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-158">**MCI\_VCR\_SETAUDIO\_PARMS**</span></span>](mci-vcr-setaudio-parms.md)
-   [<span data-ttu-id="7e0f5-159">**\_parâmetros do \_ setajuster \_ VCR MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-159">**MCI\_VCR\_SETTUNER\_PARMS**</span></span>](mci-vcr-settuner-parms.md)
-   [<span data-ttu-id="7e0f5-160">**\_parâmetros de \_ vídeo do VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-160">**MCI\_VCR\_SETVIDEO\_PARMS**</span></span>](mci-vcr-setvideo-parms.md)
-   [<span data-ttu-id="7e0f5-161">**\_parâmetros de \_ escape de VD do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-161">**MCI\_VD\_ESCAPE\_PARMS**</span></span>](mci-vd-escape-parms.md)
-   [<span data-ttu-id="7e0f5-162">**\_parâmetros do \_ conjunto de ondas MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-162">**MCI\_WAVE\_SET\_PARMS**</span></span>](mci-wave-set-parms.md)
-   [<span data-ttu-id="7e0f5-163">**Definição**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-163">**set**</span></span>](set.md)
-   [<span data-ttu-id="7e0f5-164">**SetAudio**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-164">**setaudio**</span></span>](setaudio.md)
-   [<span data-ttu-id="7e0f5-165">**SetCode**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-165">**settimecode**</span></span>](settimecode.md)
-   [<span data-ttu-id="7e0f5-166">**setajuster**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-166">**settuner**</span></span>](settuner.md)
-   [<span data-ttu-id="7e0f5-167">**setvideo**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-167">**setvideo**</span></span>](setvideo.md)
-   [<span data-ttu-id="7e0f5-168">**ativa**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-168">**spin**</span></span>](spin.md)

## <a name="controlling-playback"></a><span data-ttu-id="7e0f5-169">Controlando a reprodução</span><span class="sxs-lookup"><span data-stu-id="7e0f5-169">Controlling Playback</span></span>

-   [<span data-ttu-id="7e0f5-170">**Trave**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-170">**freeze**</span></span>](freeze.md)
-   [<span data-ttu-id="7e0f5-171">**carrega**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-171">**load**</span></span>](load.md)
-   [<span data-ttu-id="7e0f5-172">**\_DGV de \_ congelamento do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-172">**MCI\_DGV\_FREEZE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms)
-   <span data-ttu-id="7e0f5-173">[**\_parâmetros de \_ carga \_ DGV MCI**](/previous-versions//dd743391(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-173">[**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-174">[**\_parâmetros de \_ pausa de DGV MCI \_**](/previous-versions//dd743395(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-174">[**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-175">[**parâmetros de reprodução do MCI \_ DGV \_ \_**](/previous-versions//dd743396(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-175">[**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-176">[**\_parâmetros de \_ retomada do MCI DGV \_**](/previous-versions//dd743403(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-176">[**MCI\_DGV\_RESUME\_PARMS**](/previous-versions//dd743403(v=vs.85))</span></span>
-   <span data-ttu-id="7e0f5-177">[**DGV do MCI de \_ \_ parada de \_ parâmetros**](/previous-versions//dd743411(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-177">[**MCI\_DGV\_STOP\_PARMS**](/previous-versions//dd743411(v=vs.85))</span></span>
-   [<span data-ttu-id="7e0f5-178">**congelamento de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-178">**MCI\_FREEZE**</span></span>](mci-freeze.md)
-   [<span data-ttu-id="7e0f5-179">**\_carga MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-179">**MCI\_LOAD**</span></span>](mci-load.md)
-   [<span data-ttu-id="7e0f5-180">**\_parâmetros de carga MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-180">**MCI\_LOAD\_PARMS**</span></span>](mci-load-parms.md)
-   [<span data-ttu-id="7e0f5-181">**\_parâmetros de \_ carga \_ OVLY MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-181">**MCI\_OVLY\_LOAD\_PARMS**</span></span>](mci-ovly-load-parms.md)
-   [<span data-ttu-id="7e0f5-182">**pausa de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-182">**MCI\_PAUSE**</span></span>](mci-pause.md)
-   [<span data-ttu-id="7e0f5-183">**\_reprodução MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-183">**MCI\_PLAY**</span></span>](mci-play.md)
-   [<span data-ttu-id="7e0f5-184">**\_parâmetros de reprodução MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-184">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
-   [<span data-ttu-id="7e0f5-185">**retomar MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-185">**MCI\_RESUME**</span></span>](mci-resume.md)
-   [<span data-ttu-id="7e0f5-186">**parada do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-186">**MCI\_STOP**</span></span>](mci-stop.md)
-   [<span data-ttu-id="7e0f5-187">**descongelar MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-187">**MCI\_UNFREEZE**</span></span>](mci-unfreeze.md)
-   [<span data-ttu-id="7e0f5-188">**\_parâmetros de \_ reprodução de VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-188">**MCI\_VCR\_PLAY\_PARMS**</span></span>](mci-vcr-play-parms.md)
-   [<span data-ttu-id="7e0f5-189">**\_parâmetros de \_ reprodução de VD do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-189">**MCI\_VD\_PLAY\_PARMS**</span></span>](mci-vd-play-parms.md)
-   [<span data-ttu-id="7e0f5-190">**temporariamente**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-190">**pause**</span></span>](pause.md)
-   [<span data-ttu-id="7e0f5-191">**reproduzir**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-191">**play**</span></span>](play.md)
-   [<span data-ttu-id="7e0f5-192">**Volte**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-192">**resume**</span></span>](resume.md)
-   [<span data-ttu-id="7e0f5-193">**deixar**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-193">**stop**</span></span>](stop.md)
-   [<span data-ttu-id="7e0f5-194">**descongelar**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-194">**unfreeze**</span></span>](unfreeze.md)

## <a name="controlling-the-position"></a><span data-ttu-id="7e0f5-195">Controlando a posição</span><span class="sxs-lookup"><span data-stu-id="7e0f5-195">Controlling the Position</span></span>

-   [<span data-ttu-id="7e0f5-196">**advertência**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-196">**cue**</span></span>](cue.md)
-   [<span data-ttu-id="7e0f5-197">**marca**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-197">**mark**</span></span>](mark.md)
-   [<span data-ttu-id="7e0f5-198">**indicação de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-198">**MCI\_CUE**</span></span>](mci-cue.md)
-   [<span data-ttu-id="7e0f5-199">**\_parâmetros de \_ indicação de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-199">**MCI\_DGV\_CUE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms)
-   [<span data-ttu-id="7e0f5-200">**\_parâmetros de \_ sinal MCI DGV \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-200">**MCI\_DGV\_SIGNAL\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)
-   [<span data-ttu-id="7e0f5-201">**\_parâmetros da \_ etapa MCI DGV \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-201">**MCI\_DGV\_STEP\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms)
-   [<span data-ttu-id="7e0f5-202">**\_marca MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-202">**MCI\_MARK**</span></span>](mci-mark.md)
-   [<span data-ttu-id="7e0f5-203">**busca de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-203">**MCI\_SEEK**</span></span>](mci-seek.md)
-   [<span data-ttu-id="7e0f5-204">**\_parâmetros de busca do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-204">**MCI\_SEEK\_PARMS**</span></span>](mci-seek-parms.md)
-   [<span data-ttu-id="7e0f5-205">**\_sinal MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-205">**MCI\_SIGNAL**</span></span>](mci-signal.md)
-   [<span data-ttu-id="7e0f5-206">**\_etapa MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-206">**MCI\_STEP**</span></span>](mci-step.md)
-   [<span data-ttu-id="7e0f5-207">**\_parâmetros de \_ sinalização de VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-207">**MCI\_VCR\_CUE\_PARMS**</span></span>](mci-vcr-cue-parms.md)
-   [<span data-ttu-id="7e0f5-208">**\_parâmetros de \_ busca de VCR do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-208">**MCI\_VCR\_SEEK\_PARMS**</span></span>](mci-vcr-seek-parms.md)
-   [<span data-ttu-id="7e0f5-209">**\_parâmetros da \_ etapa do VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-209">**MCI\_VCR\_STEP\_PARMS**</span></span>](mci-vcr-step-parms.md)
-   [<span data-ttu-id="7e0f5-210">**\_parâmetros da \_ etapa de VD do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-210">**MCI\_VD\_STEP\_PARMS**</span></span>](mci-vd-step-parms.md)
-   [<span data-ttu-id="7e0f5-211">**Procure**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-211">**seek**</span></span>](seek.md)
-   [<span data-ttu-id="7e0f5-212">**aviso**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-212">**signal**</span></span>](signal.md)
-   [<span data-ttu-id="7e0f5-213">**etapa**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-213">**step**</span></span>](step.md)

## <a name="editing"></a><span data-ttu-id="7e0f5-214">Edição</span><span class="sxs-lookup"><span data-stu-id="7e0f5-214">Editing</span></span>

-   [<span data-ttu-id="7e0f5-215">**CopiarObjeto**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-215">**copy**</span></span>](copy.md)
-   [<span data-ttu-id="7e0f5-216">**migração**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-216">**cut**</span></span>](cut.md)
-   [<span data-ttu-id="7e0f5-217">**apagar**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-217">**delete**</span></span>](delete.md)
-   [<span data-ttu-id="7e0f5-218">**cópia do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-218">**MCI\_COPY**</span></span>](mci-copy.md)
-   [<span data-ttu-id="7e0f5-219">**recorte de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-219">**MCI\_CUT**</span></span>](mci-cut.md)
-   [<span data-ttu-id="7e0f5-220">**exclusão de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-220">**MCI\_DELETE**</span></span>](mci-delete.md)
-   [<span data-ttu-id="7e0f5-221">**\_parâmetros de \_ cópia MCI DGV \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-221">**MCI\_DGV\_COPY\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms)
-   [<span data-ttu-id="7e0f5-222">**\_parâmetros de \_ recorte de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-222">**MCI\_DGV\_CUT\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms)
-   [<span data-ttu-id="7e0f5-223">**\_parâmetros de \_ exclusão de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-223">**MCI\_DGV\_DELETE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms)
-   [<span data-ttu-id="7e0f5-224">**\_parâmetros de \_ colagem de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-224">**MCI\_DGV\_PASTE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)
-   [<span data-ttu-id="7e0f5-225">**\_colar MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-225">**MCI\_PASTE**</span></span>](mci-paste.md)
-   [<span data-ttu-id="7e0f5-226">**\_desfazer MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-226">**MCI\_UNDO**</span></span>](mci-undo.md)
-   [<span data-ttu-id="7e0f5-227">**\_parâmetros de \_ exclusão de Wave MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-227">**MCI\_WAVE\_DELETE\_PARMS**</span></span>](mci-wave-delete-parms.md)
-   [<span data-ttu-id="7e0f5-228">**Olar**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-228">**paste**</span></span>](paste.md)
-   [<span data-ttu-id="7e0f5-229">**operação**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-229">**undo**</span></span>](undo.md)

## <a name="miscellaneous"></a><span data-ttu-id="7e0f5-230">Diversos</span><span class="sxs-lookup"><span data-stu-id="7e0f5-230">Miscellaneous</span></span>

-   [<span data-ttu-id="7e0f5-231">**\_parâmetros genéricos do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-231">**MCI\_GENERIC\_PARMS**</span></span>](mci-generic-parms.md)

## <a name="opening-and-closing"></a><span data-ttu-id="7e0f5-232">Abrindo e fechando</span><span class="sxs-lookup"><span data-stu-id="7e0f5-232">Opening and Closing</span></span>

-   [<span data-ttu-id="7e0f5-233">**inclui**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-233">**close**</span></span>](close.md)
-   [<span data-ttu-id="7e0f5-234">**fechamento de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-234">**MCI\_CLOSE**</span></span>](mci-close.md)
-   [<span data-ttu-id="7e0f5-235">**\_parâmetros de \_ abertura de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-235">**MCI\_DGV\_OPEN\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa)
-   [<span data-ttu-id="7e0f5-236">**MCI \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-236">**MCI\_OPEN**</span></span>](mci-open.md)
-   [<span data-ttu-id="7e0f5-237">**\_parâmetros de abertura do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-237">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
-   [<span data-ttu-id="7e0f5-238">**\_parâmetros de \_ abertura de OVLY MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-238">**MCI\_OVLY\_OPEN\_PARMS**</span></span>](mci-ovly-open-parms.md)
-   [<span data-ttu-id="7e0f5-239">**\_parâmetros de \_ abertura \_ Wave MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-239">**MCI\_WAVE\_OPEN\_PARMS**</span></span>](mci-wave-open-parms.md)
-   [<span data-ttu-id="7e0f5-240">**abrir**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-240">**open**</span></span>](open.md)

## <a name="realizing-a-palette"></a><span data-ttu-id="7e0f5-241">Concretizando uma paleta</span><span class="sxs-lookup"><span data-stu-id="7e0f5-241">Realizing a Palette</span></span>

-   [<span data-ttu-id="7e0f5-242">**percepção do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-242">**MCI\_REALIZE**</span></span>](mci-realize.md)
-   [<span data-ttu-id="7e0f5-243">**State**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-243">**realize**</span></span>](realize.md)

## <a name="repainting-a-frame"></a><span data-ttu-id="7e0f5-244">Repintando um quadro</span><span class="sxs-lookup"><span data-stu-id="7e0f5-244">Repainting a Frame</span></span>

-   [<span data-ttu-id="7e0f5-245">**parâmetros de atualização do MCI \_ DGV \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-245">**MCI\_DGV\_UPDATE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms)
-   [<span data-ttu-id="7e0f5-246">**atualização do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-246">**MCI\_UPDATE**</span></span>](mci-update.md)
-   [<span data-ttu-id="7e0f5-247">**cumulativo**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-247">**update**</span></span>](update.md)

## <a name="retrieving-information"></a><span data-ttu-id="7e0f5-248">Recuperando informações</span><span class="sxs-lookup"><span data-stu-id="7e0f5-248">Retrieving Information</span></span>

-   [<span data-ttu-id="7e0f5-249">**recursos**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-249">**capability**</span></span>](capability.md)
-   [<span data-ttu-id="7e0f5-250">**detalhes**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-250">**info**</span></span>](info.md)
-   [<span data-ttu-id="7e0f5-251">**lista**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-251">**list**</span></span>](list.md)
-   [<span data-ttu-id="7e0f5-252">**\_parâmetros de \_ informações de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-252">**MCI\_DGV\_INFO\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa)
-   [<span data-ttu-id="7e0f5-253">**\_parâmetros da \_ lista de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-253">**MCI\_DGV\_LIST\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa)
-   [<span data-ttu-id="7e0f5-254">**parâmetros de status do MCI \_ DGV \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-254">**MCI\_DGV\_STATUS\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa)
-   [<span data-ttu-id="7e0f5-255">**\_GETDEVCAPS MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-255">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
-   [<span data-ttu-id="7e0f5-256">**\_parâmetros MCI GETDEVCAPS \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-256">**MCI\_GETDEVCAPS\_PARMS**</span></span>](mci-getdevcaps-parms.md)
-   [<span data-ttu-id="7e0f5-257">**informações do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-257">**MCI\_INFO**</span></span>](mci-info.md)
-   [<span data-ttu-id="7e0f5-258">**\_parâmetros de informações do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-258">**MCI\_INFO\_PARMS**</span></span>](mci-info-parms.md)
-   [<span data-ttu-id="7e0f5-259">**lista de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-259">**MCI\_LIST**</span></span>](mci-list.md)
-   [<span data-ttu-id="7e0f5-260">**STATUS do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-260">**MCI\_STATUS**</span></span>](mci-status.md)
-   [<span data-ttu-id="7e0f5-261">**\_parâmetros de status do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-261">**MCI\_STATUS\_PARMS**</span></span>](mci-status-parms.md)
-   [<span data-ttu-id="7e0f5-262">**SysInfo do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-262">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
-   [<span data-ttu-id="7e0f5-263">**\_parâmetros do sysinfo do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-263">**MCI\_SYSINFO\_PARMS**</span></span>](mci-sysinfo-parms.md)
-   [<span data-ttu-id="7e0f5-264">**\_parâmetros da lista de videocassetes MCI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-264">**MCI\_VCR\_LIST\_PARMS**</span></span>](mci-vcr-list-parms.md)
-   [<span data-ttu-id="7e0f5-265">**\_parâmetros de \_ status do VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-265">**MCI\_VCR\_STATUS\_PARMS**</span></span>](mci-vcr-status-parms.md)
-   [<span data-ttu-id="7e0f5-266">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-266">**status**</span></span>](status.md)
-   [<span data-ttu-id="7e0f5-267">SysInfo</span><span class="sxs-lookup"><span data-stu-id="7e0f5-267">sysinfo</span></span>](sysinfo.md)

## <a name="saving"></a><span data-ttu-id="7e0f5-268">Saving</span><span class="sxs-lookup"><span data-stu-id="7e0f5-268">Saving</span></span>

-   [<span data-ttu-id="7e0f5-269">**\_parâmetros de \_ registro MCI DGV \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-269">**MCI\_DGV\_RECORD\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms)
-   [<span data-ttu-id="7e0f5-270">**\_parâmetros de \_ salvamento de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-270">**MCI\_DGV\_SAVE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa)
-   <span data-ttu-id="7e0f5-271">[**\_parâmetros de \_ salvamento de OVLY MCI \_**](/previous-versions//dd743447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-271">[**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85))</span></span>
-   [<span data-ttu-id="7e0f5-272">**\_registro MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-272">**MCI\_RECORD**</span></span>](mci-record.md)
-   [<span data-ttu-id="7e0f5-273">**\_parâmetros de registro MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-273">**MCI\_RECORD\_PARMS**</span></span>](mci-record-parms.md)
-   [<span data-ttu-id="7e0f5-274">**\_salvar MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-274">**MCI\_SAVE**</span></span>](mci-save.md)
-   [<span data-ttu-id="7e0f5-275">**\_parâmetros de salvamento de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-275">**MCI\_SAVE\_PARMS**</span></span>](mci-save-parms.md)
-   [<span data-ttu-id="7e0f5-276">**\_parâmetros de \_ registro do VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-276">**MCI\_VCR\_RECORD\_PARMS**</span></span>](mci-vcr-record-parms.md)
-   [<span data-ttu-id="7e0f5-277">**gravável**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-277">**record**</span></span>](record.md)
-   [<span data-ttu-id="7e0f5-278">**Guarde**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-278">**save**</span></span>](save.md)

## <a name="video-control"></a><span data-ttu-id="7e0f5-279">Controle de vídeo</span><span class="sxs-lookup"><span data-stu-id="7e0f5-279">Video Control</span></span>

-   [<span data-ttu-id="7e0f5-280">**captura**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-280">**capture**</span></span>](capture.md)
-   [<span data-ttu-id="7e0f5-281">**\_captura MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-281">**MCI\_CAPTURE**</span></span>](mci-capture.md)
-   [<span data-ttu-id="7e0f5-282">**\_parâmetros do \_ Monitor de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-282">**MCI\_DGV\_MONITOR\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms)
-   [<span data-ttu-id="7e0f5-283">**\_parâmetros de \_ qualidade MCI DGV \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-283">**MCI\_DGV\_QUALITY\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)
-   [<span data-ttu-id="7e0f5-284">**\_parâmetros de \_ reserva de DGV MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-284">**MCI\_DGV\_RESERVE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)
-   [<span data-ttu-id="7e0f5-285">**parâmetros de restauração do MCI \_ DGV \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-285">**MCI\_DGV\_RESTORE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa)
-   [<span data-ttu-id="7e0f5-286">**\_Monitor MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-286">**MCI\_MONITOR**</span></span>](mci-monitor.md)
-   [<span data-ttu-id="7e0f5-287">**qualidade do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-287">**MCI\_QUALITY**</span></span>](mci-quality.md)
-   [<span data-ttu-id="7e0f5-288">**Reserva de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-288">**MCI\_RESERVE**</span></span>](mci-reserve.md)
-   [<span data-ttu-id="7e0f5-289">**restauração de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-289">**MCI\_RESTORE**</span></span>](mci-restore.md)
-   [<span data-ttu-id="7e0f5-290">**monitor**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-290">**monitor**</span></span>](monitor.md)
-   [<span data-ttu-id="7e0f5-291">**PrintQuality**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-291">**quality**</span></span>](quality.md)
-   [<span data-ttu-id="7e0f5-292">**reservado**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-292">**reserve**</span></span>](reserve.md)
-   [<span data-ttu-id="7e0f5-293">**restaurar**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-293">**restore**</span></span>](restore.md)

## <a name="window-or-display-rectangles"></a><span data-ttu-id="7e0f5-294">Janelas ou retângulos de exibição</span><span class="sxs-lookup"><span data-stu-id="7e0f5-294">Window or Display Rectangles</span></span>

-   <span data-ttu-id="7e0f5-295">[**DGV do MCI \_ \_ colocar \_ parâmetros**](/previous-versions//dd743397(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e0f5-295">[**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85))</span></span>
-   [<span data-ttu-id="7e0f5-296">**parâmetros do MCI \_ DGV \_ Rect \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-296">**MCI\_DGV\_RECT\_PARMS**</span></span>](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)
-   [<span data-ttu-id="7e0f5-297">**\_parâmetros da \_ janela MCI DGV \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-297">**MCI\_DGV\_WINDOW\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa)
-   [<span data-ttu-id="7e0f5-298">**parâmetros do MCI \_ OVLY \_ Rect \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-298">**MCI\_OVLY\_RECT\_PARMS**</span></span>](mci-ovly-rect-parms.md)
-   [<span data-ttu-id="7e0f5-299">**\_parâmetros da \_ janela MCI OVLY \_**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-299">**MCI\_OVLY\_WINDOW\_PARMS**</span></span>](mci-ovly-window-parms.md)
-   [<span data-ttu-id="7e0f5-300">**\_Put MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-300">**MCI\_PUT**</span></span>](mci-put.md)
-   [<span data-ttu-id="7e0f5-301">**MCI \_ onde**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-301">**MCI\_WHERE**</span></span>](mci-where.md)
-   [<span data-ttu-id="7e0f5-302">**\_janela MCI**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-302">**MCI\_WINDOW**</span></span>](mci-window.md)
-   [<span data-ttu-id="7e0f5-303">**Posicione**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-303">**put**</span></span>](put.md)
-   [<span data-ttu-id="7e0f5-304">**posição**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-304">**where**</span></span>](where.md)
-   [<span data-ttu-id="7e0f5-305">**Window**</span><span class="sxs-lookup"><span data-stu-id="7e0f5-305">**window**</span></span>](window.md)

## <a name="related-topics"></a><span data-ttu-id="7e0f5-306">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e0f5-306">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e0f5-307">MCI</span><span class="sxs-lookup"><span data-stu-id="7e0f5-307">MCI</span></span>](mci.md)
</dt> </dl>

 

 