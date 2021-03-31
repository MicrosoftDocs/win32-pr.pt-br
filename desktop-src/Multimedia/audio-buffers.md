---
title: Buffers de áudio
description: Buffers de áudio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635461"
---
# <a name="audio-buffers"></a><span data-ttu-id="2e11f-107">Buffers de áudio</span><span class="sxs-lookup"><span data-stu-id="2e11f-107">Audio Buffers</span></span>

<span data-ttu-id="2e11f-108">Você pode controlar a parte de áudio de uma operação de captura de três maneiras:</span><span class="sxs-lookup"><span data-stu-id="2e11f-108">You can control the audio portion of a capture operation in three ways:</span></span>

-   <span data-ttu-id="2e11f-109">Incluir ou excluir áudio da operação de captura.</span><span class="sxs-lookup"><span data-stu-id="2e11f-109">Include or exclude audio from the capture operation.</span></span>
-   <span data-ttu-id="2e11f-110">Solicite um número específico de buffers de áudio.</span><span class="sxs-lookup"><span data-stu-id="2e11f-110">Request a specific number of audio buffers.</span></span>
-   <span data-ttu-id="2e11f-111">Solicite que os buffers de áudio tenham um tamanho específico.</span><span class="sxs-lookup"><span data-stu-id="2e11f-111">Request that audio buffers be a specific size.</span></span>

<span data-ttu-id="2e11f-112">Você pode recuperar as configurações para buffers de áudio usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="2e11f-112">You can retrieve the settings for audio buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="2e11f-113">O membro **fCaptureAudio** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) especifica se o áudio é incluído ou excluído da operação de captura.</span><span class="sxs-lookup"><span data-stu-id="2e11f-113">The **fCaptureAudio** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure specifies whether audio is included or excluded from the capture operation.</span></span> <span data-ttu-id="2e11f-114">O número atual solicitado de buffers de áudio é armazenado no membro **wNumAudioRequested** e o tamanho atual do buffer de áudio é armazenado no membro **dwAudioBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="2e11f-114">The current requested number of audio buffers is stored in the **wNumAudioRequested** member, and the current audio buffer size is stored in the **dwAudioBufferSize** member.</span></span> <span data-ttu-id="2e11f-115">Você pode especificar se deseja incluir a captura de áudio, especificar o tamanho e o número de buffers de áudio atualizando esses membros e enviar a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ \_ Sequence**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="2e11f-115">You can specify whether to include audio capture, specify the size and number of audio buffers by updating these members, and send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

<span data-ttu-id="2e11f-116">Por padrão, o áudio é incluído na operação de captura e quatro buffers de áudio são alocados.</span><span class="sxs-lookup"><span data-stu-id="2e11f-116">By default, audio is included in the capture operation, and four audio buffers are allocated.</span></span> <span data-ttu-id="2e11f-117">O valor padrão de **fCaptureAudio** é **true**.</span><span class="sxs-lookup"><span data-stu-id="2e11f-117">The default value of **fCaptureAudio** is **TRUE**.</span></span> <span data-ttu-id="2e11f-118">O tamanho de buffer padrão (o valor de **dwAudioBufferSize**) pode conter 0,5 segundos de dados de áudio ou 10K, o que for maior.</span><span class="sxs-lookup"><span data-stu-id="2e11f-118">The default buffer size (the value of **dwAudioBufferSize**) can contain 0.5 seconds of audio data or 10K, whichever is greater.</span></span>

 

 




