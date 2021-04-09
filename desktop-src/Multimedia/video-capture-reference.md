---
title: Referência de captura de vídeo
description: Referência de captura de vídeo
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Video for Windows (VFW), referência de captura de vídeo
- VFW (vídeo para Windows), referência de captura de vídeo
- AVICap, referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005116"
---
# <a name="video-capture-reference"></a><span data-ttu-id="320b1-106">Referência de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="320b1-106">Video Capture Reference</span></span>

<span data-ttu-id="320b1-107">Esta seção descreve as funções, estruturas, mensagens e macros associadas à classe de janela AVICap.</span><span class="sxs-lookup"><span data-stu-id="320b1-107">This section describes the functions, structures, messages, and macros associated with the AVICap window class.</span></span> <span data-ttu-id="320b1-108">Esses elementos são agrupados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="320b1-108">These elements are grouped as follows.</span></span>

## <a name="basic-capture-operations"></a><span data-ttu-id="320b1-109">Operações básicas de captura</span><span class="sxs-lookup"><span data-stu-id="320b1-109">Basic Capture Operations</span></span>

-   [<span data-ttu-id="320b1-110">**capCreateCaptureWindow**</span><span class="sxs-lookup"><span data-stu-id="320b1-110">**capCreateCaptureWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [<span data-ttu-id="320b1-111">**\_abortar Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-111">**WM\_CAP\_ABORT**</span></span>](wm-cap-abort.md)
-   [<span data-ttu-id="320b1-112">**conexão do driver do WM \_ Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-112">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="320b1-113">**\_sequência de Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-113">**WM\_CAP\_SEQUENCE**</span></span>](wm-cap-sequence.md)
-   [<span data-ttu-id="320b1-114">**\_parada da Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-114">**WM\_CAP\_STOP**</span></span>](wm-cap-stop.md)

## <a name="capture-windows"></a><span data-ttu-id="320b1-115">Capturar janelas</span><span class="sxs-lookup"><span data-stu-id="320b1-115">Capture Windows</span></span>

-   [<span data-ttu-id="320b1-116">**CAPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="320b1-116">**CAPSTATUS**</span></span>](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [<span data-ttu-id="320b1-117">**capGetDriverDescription**</span><span class="sxs-lookup"><span data-stu-id="320b1-117">**capGetDriverDescription**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [<span data-ttu-id="320b1-118">**conexão do driver do WM \_ Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-118">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="320b1-119">**desconexão do driver do WM \_ Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-119">**WM\_CAP\_DRIVER\_DISCONNECT**</span></span>](wm-cap-driver-disconnect.md)
-   [<span data-ttu-id="320b1-120">**STATUS da obtenção do WM \_ Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-120">**WM\_CAP\_GET\_STATUS**</span></span>](wm-cap-get-status.md)

## <a name="capture-drivers"></a><span data-ttu-id="320b1-121">Drivers de captura</span><span class="sxs-lookup"><span data-stu-id="320b1-121">Capture Drivers</span></span>

-   [<span data-ttu-id="320b1-122">**CAPDRIVERCAPS**</span><span class="sxs-lookup"><span data-stu-id="320b1-122">**CAPDRIVERCAPS**</span></span>](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [<span data-ttu-id="320b1-123">**Driver do WM \_ Cap \_ \_ obter \_ Caps**</span><span class="sxs-lookup"><span data-stu-id="320b1-123">**WM\_CAP\_DRIVER\_GET\_CAPS**</span></span>](wm-cap-driver-get-caps.md)
-   [<span data-ttu-id="320b1-124">**\_nome de \_ obtenção do driver \_ \_ do WM Cap**</span><span class="sxs-lookup"><span data-stu-id="320b1-124">**WM\_CAP\_DRIVER\_GET\_NAME**</span></span>](wm-cap-driver-get-name.md)
-   [<span data-ttu-id="320b1-125">**\_ \_ \_ versão get do driver \_ do WM Cap**</span><span class="sxs-lookup"><span data-stu-id="320b1-125">**WM\_CAP\_DRIVER\_GET\_VERSION**</span></span>](wm-cap-driver-get-version.md)
-   [<span data-ttu-id="320b1-126">**introdução do WM \_ Cap \_ \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="320b1-126">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="320b1-127">**introdução do WM \_ Cap \_ \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="320b1-127">**WM\_CAP\_GET\_VIDEOFORMAT**</span></span>](wm-cap-get-videoformat.md)
-   [<span data-ttu-id="320b1-128">**WM \_ Cap \_ set \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="320b1-128">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)
-   [<span data-ttu-id="320b1-129">**WM \_ Cap \_ set \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="320b1-129">**WM\_CAP\_SET\_VIDEOFORMAT**</span></span>](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a><span data-ttu-id="320b1-130">Capturar os modos de visualização e sobreposição do driver</span><span class="sxs-lookup"><span data-stu-id="320b1-130">Capture Driver Preview and Overlay Modes</span></span>

-   [<span data-ttu-id="320b1-131">**sobreposição de conjunto de Cap do WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-131">**WM\_CAP\_SET\_OVERLAY**</span></span>](wm-cap-set-overlay.md)
-   [<span data-ttu-id="320b1-132">**\_visualização do \_ conjunto de Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-132">**WM\_CAP\_SET\_PREVIEW**</span></span>](wm-cap-set-preview.md)
-   [<span data-ttu-id="320b1-133">**WM \_ Cap \_ set \_ PREVIEWRATE**</span><span class="sxs-lookup"><span data-stu-id="320b1-133">**WM\_CAP\_SET\_PREVIEWRATE**</span></span>](wm-cap-set-previewrate.md)
-   [<span data-ttu-id="320b1-134">**\_escala de \_ conjunto de Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-134">**WM\_CAP\_SET\_SCALE**</span></span>](wm-cap-set-scale.md)
-   [<span data-ttu-id="320b1-135">**\_ \_ rolagem do conjunto de Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-135">**WM\_CAP\_SET\_SCROLL**</span></span>](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a><span data-ttu-id="320b1-136">Caixas de diálogo de vídeo do driver de captura</span><span class="sxs-lookup"><span data-stu-id="320b1-136">Capture Driver Video Dialog Boxes</span></span>

-   [<span data-ttu-id="320b1-137">**WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION**</span><span class="sxs-lookup"><span data-stu-id="320b1-137">**WM\_CAP\_DLG\_VIDEOCOMPRESSION**</span></span>](wm-cap-dlg-videocompression.md)
-   [<span data-ttu-id="320b1-138">**WM \_ Cap \_ DLG \_ VIDEODISPLAY**</span><span class="sxs-lookup"><span data-stu-id="320b1-138">**WM\_CAP\_DLG\_VIDEODISPLAY**</span></span>](wm-cap-dlg-videodisplay.md)
-   [<span data-ttu-id="320b1-139">**WM \_ Cap \_ DLG \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="320b1-139">**WM\_CAP\_DLG\_VIDEOFORMAT**</span></span>](wm-cap-dlg-videoformat.md)
-   [<span data-ttu-id="320b1-140">**visualização do WM \_ Cap de \_ DLG \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-140">**WM\_CAP\_DLG\_VIDEOSOURCE**</span></span>](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a><span data-ttu-id="320b1-141">Formato de áudio</span><span class="sxs-lookup"><span data-stu-id="320b1-141">Audio Format</span></span>

-   [<span data-ttu-id="320b1-142">**introdução do WM \_ Cap \_ \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="320b1-142">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="320b1-143">**WM \_ Cap \_ set \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="320b1-143">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a><span data-ttu-id="320b1-144">Configurações de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="320b1-144">Video Capture Settings</span></span>

-   [<span data-ttu-id="320b1-145">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="320b1-145">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="320b1-146">**\_configuração da \_ \_ sequência get \_ do WM Cap**</span><span class="sxs-lookup"><span data-stu-id="320b1-146">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="320b1-147">**configuração da sequência do WM \_ Cap \_ set \_ \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-147">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a><span data-ttu-id="320b1-148">Arquivos de captura e buffers</span><span class="sxs-lookup"><span data-stu-id="320b1-148">Capture File and Buffers</span></span>

-   [<span data-ttu-id="320b1-149">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="320b1-149">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="320b1-150">**\_ \_ alocar arquivo do WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-150">**WM\_CAP\_FILE\_ALLOCATE**</span></span>](wm-cap-file-allocate.md)
-   [<span data-ttu-id="320b1-151">**arquivo \_ de \_ \_ captura de \_ obter \_ arquivo do WM Cap**</span><span class="sxs-lookup"><span data-stu-id="320b1-151">**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**</span></span>](wm-cap-file-get-capture-file.md)
-   [<span data-ttu-id="320b1-152">**\_ \_ salvar arquivo do WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-152">**WM\_CAP\_FILE\_SAVEAS**</span></span>](wm-cap-file-saveas.md)
-   [<span data-ttu-id="320b1-153">**\_arquivo de \_ captura do conjunto de arquivos \_ \_ do WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-153">**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**</span></span>](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a><span data-ttu-id="320b1-154">Usando dados de captura diretamente</span><span class="sxs-lookup"><span data-stu-id="320b1-154">Directly Using Capture Data</span></span>

-   [<span data-ttu-id="320b1-155">**Cadeia de extremidade do WM \_ \_ \_ nofile**</span><span class="sxs-lookup"><span data-stu-id="320b1-155">**WM\_CAP\_SEQUENCE\_NOFILE**</span></span>](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a><span data-ttu-id="320b1-156">Capturar do dispositivo MCI</span><span class="sxs-lookup"><span data-stu-id="320b1-156">Capture from MCI Device</span></span>

-   [<span data-ttu-id="320b1-157">**WM \_ Cap \_ set \_ MCI \_ Device**</span><span class="sxs-lookup"><span data-stu-id="320b1-157">**WM\_CAP\_SET\_MCI\_DEVICE**</span></span>](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a><span data-ttu-id="320b1-158">Captura de quadro manual</span><span class="sxs-lookup"><span data-stu-id="320b1-158">Manual Frame Capture</span></span>

-   [<span data-ttu-id="320b1-159">**\_ \_ quadro único do WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-159">**WM\_CAP\_SINGLE\_FRAME**</span></span>](wm-cap-single-frame.md)
-   [<span data-ttu-id="320b1-160">**\_fechamento de \_ \_ quadro único \_ do WM Cap**</span><span class="sxs-lookup"><span data-stu-id="320b1-160">**WM\_CAP\_SINGLE\_FRAME\_CLOSE**</span></span>](wm-cap-single-frame-close.md)
-   [<span data-ttu-id="320b1-161">**\_quadro único do WM Cap \_ \_ \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="320b1-161">**WM\_CAP\_SINGLE\_FRAME\_OPEN**</span></span>](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a><span data-ttu-id="320b1-162">Captura de Still-Image</span><span class="sxs-lookup"><span data-stu-id="320b1-162">Still-Image Capture</span></span>

-   [<span data-ttu-id="320b1-163">**\_cópia de \_ edição da Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-163">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="320b1-164">**SAVEDIB do arquivo do WM \_ Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-164">**WM\_CAP\_FILE\_SAVEDIB**</span></span>](wm-cap-file-savedib.md)
-   [<span data-ttu-id="320b1-165">**\_quadro de \_ captura da Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-165">**WM\_CAP\_GRAB\_FRAME**</span></span>](wm-cap-grab-frame.md)
-   [<span data-ttu-id="320b1-166">**quadro de captura da Cap do WM \_ \_ \_ \_ nostop**</span><span class="sxs-lookup"><span data-stu-id="320b1-166">**WM\_CAP\_GRAB\_FRAME\_NOSTOP**</span></span>](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a><span data-ttu-id="320b1-167">Opções avançadas de captura</span><span class="sxs-lookup"><span data-stu-id="320b1-167">Advanced Capture Options</span></span>

-   [<span data-ttu-id="320b1-168">**\_INFOCHUNK do \_ conjunto de arquivos \_ \_ do WM Cap**</span><span class="sxs-lookup"><span data-stu-id="320b1-168">**WM\_CAP\_FILE\_SET\_INFOCHUNK**</span></span>](wm-cap-file-set-infochunk.md)
-   [<span data-ttu-id="320b1-169">**o \_ WM \_ Cap \_ Obtém \_ dados do usuário**</span><span class="sxs-lookup"><span data-stu-id="320b1-169">**WM\_CAP\_GET\_USER\_DATA**</span></span>](wm-cap-get-user-data.md)
-   [<span data-ttu-id="320b1-170">**WM \_ Cap \_ definir \_ dados do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-170">**WM\_CAP\_SET\_USER\_DATA**</span></span>](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a><span data-ttu-id="320b1-171">Trabalhando com paletas</span><span class="sxs-lookup"><span data-stu-id="320b1-171">Working with Palettes</span></span>

-   [<span data-ttu-id="320b1-172">**\_cópia de \_ edição da Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-172">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="320b1-173">**\_criação de \_ AutoCriar do WM Cap PAL \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-173">**WM\_CAP\_PAL\_AUTOCREATE**</span></span>](wm-cap-pal-autocreate.md)
-   [<span data-ttu-id="320b1-174">**WM \_ Cap \_ PAL \_ MANUALCREATE**</span><span class="sxs-lookup"><span data-stu-id="320b1-174">**WM\_CAP\_PAL\_MANUALCREATE**</span></span>](wm-cap-pal-manualcreate.md)
-   [<span data-ttu-id="320b1-175">**\_PAL Cap do WM \_ \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="320b1-175">**WM\_CAP\_PAL\_OPEN**</span></span>](wm-cap-pal-open.md)
-   [<span data-ttu-id="320b1-176">**\_colar da \_ PAL da Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-176">**WM\_CAP\_PAL\_PASTE**</span></span>](wm-cap-pal-paste.md)
-   [<span data-ttu-id="320b1-177">**\_salvar proteção \_ PAL do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-177">**WM\_CAP\_PAL\_SAVE**</span></span>](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a><span data-ttu-id="320b1-178">Respondendo a outros aplicativos</span><span class="sxs-lookup"><span data-stu-id="320b1-178">Yielding to Other Applications</span></span>

-   [<span data-ttu-id="320b1-179">**\_configuração da \_ \_ sequência get \_ do WM Cap**</span><span class="sxs-lookup"><span data-stu-id="320b1-179">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="320b1-180">**o \_ \_ retorno de \_ chamada de Set Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-180">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="320b1-181">**configuração da sequência do WM \_ Cap \_ set \_ \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-181">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a><span data-ttu-id="320b1-182">Funções de retorno de chamada AVICap</span><span class="sxs-lookup"><span data-stu-id="320b1-182">AVICap Callback Functions</span></span>

-   [<span data-ttu-id="320b1-183">**capControlCallback**</span><span class="sxs-lookup"><span data-stu-id="320b1-183">**capControlCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [<span data-ttu-id="320b1-184">**capErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="320b1-184">**capErrorCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [<span data-ttu-id="320b1-185">**capStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="320b1-185">**capStatusCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [<span data-ttu-id="320b1-186">**capVideoStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="320b1-186">**capVideoStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [<span data-ttu-id="320b1-187">**capWaveStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="320b1-187">**capWaveStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [<span data-ttu-id="320b1-188">**capYieldCallback**</span><span class="sxs-lookup"><span data-stu-id="320b1-188">**capYieldCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [<span data-ttu-id="320b1-189">**WM \_ Cap \_ set \_ callback \_ CAPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="320b1-189">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)
-   [<span data-ttu-id="320b1-190">**\_erro de \_ retorno de \_ chamada de Set Cap \_ do WM**</span><span class="sxs-lookup"><span data-stu-id="320b1-190">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="320b1-191">**\_quadro de \_ retorno de \_ chamada Set \_ Cap do WM**</span><span class="sxs-lookup"><span data-stu-id="320b1-191">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)
-   [<span data-ttu-id="320b1-192">**WM \_ Cap \_ definir \_ status de retorno de chamada \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-192">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="320b1-193">**WM \_ Cap \_ set \_ callback \_ VIDEOSTREAM**</span><span class="sxs-lookup"><span data-stu-id="320b1-193">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="320b1-194">**\_WAVESTREAM de \_ retorno de \_ chamada de Set Cap \_ do WM**</span><span class="sxs-lookup"><span data-stu-id="320b1-194">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)
-   [<span data-ttu-id="320b1-195">**o \_ \_ retorno de \_ chamada de Set Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="320b1-195">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a><span data-ttu-id="320b1-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="320b1-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="320b1-197">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="320b1-197">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 




