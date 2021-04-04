---
title: Granularidade da parte de vídeo e áudio
description: Granularidade da parte de vídeo e áudio
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- Arquivos AVI, granularidade de partes
- Classe AVICap, partes de preenchimento
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916387"
---
# <a name="video-and-audio-chunk-granularity"></a><span data-ttu-id="5e046-109">Granularidade da parte de vídeo e áudio</span><span class="sxs-lookup"><span data-stu-id="5e046-109">Video and Audio Chunk Granularity</span></span>

<span data-ttu-id="5e046-110">A granularidade da parte é um tamanho de bloco lógico para um arquivo AVI que é usado para gravar e recuperar partes de dados de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e046-110">The chunk granularity is a logical block size for an AVI file that is used for writing and retrieving audio and video data chunks.</span></span> <span data-ttu-id="5e046-111">Ao gravar partes de áudio e vídeo em disco, o AVICap adiciona partes de preenchimento (partes "lixo eletrônico" do RIFF) conforme necessário para preencher cada bloco lógico de dados.</span><span class="sxs-lookup"><span data-stu-id="5e046-111">When writing audio and video chunks to disk, AVICap adds filler chunks (RIFF "JUNK" chunks) as necessary to fill each logical block of data.</span></span>

<span data-ttu-id="5e046-112">Você pode recuperar a configuração de granularidade de bloco atual usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="5e046-112">You can retrieve the current chunk granularity setting by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="5e046-113">A granularidade de bloco atual é armazenada no membro **wChunkGranularity** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="5e046-113">The current chunk granularity is stored in the **wChunkGranularity** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="5e046-114">Você pode especificar uma nova granularidade de bloco como o valor de **wChunkGranularity** e, em seguida, enviar a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração de sequência do WM \_ Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="5e046-114">You can specify a new chunk granularity as the value of **wChunkGranularity** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="5e046-115">Você também pode especificar zero para esse membro para definir a granularidade da parte para o tamanho do setor do disco.</span><span class="sxs-lookup"><span data-stu-id="5e046-115">You can also specify zero for this member to set the chunk granularity to the sector size of the disk.</span></span>

 

 




