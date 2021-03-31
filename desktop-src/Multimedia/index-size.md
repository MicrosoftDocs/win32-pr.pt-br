---
title: Tamanho do Índice
description: Tamanho do Índice
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636263"
---
# <a name="index-size"></a><span data-ttu-id="1b758-107">Tamanho do Índice</span><span class="sxs-lookup"><span data-stu-id="1b758-107">Index Size</span></span>

<span data-ttu-id="1b758-108">Cada arquivo AVI usa um índice de um tamanho especificado para localizar partes de dados de vídeo e áudio dentro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1b758-108">Each AVI file uses an index of a specified size to locate video and audio data chunks within the file.</span></span> <span data-ttu-id="1b758-109">Uma entrada no índice localiza um quadro de vídeo ou um buffer de áudio de formato de onda.</span><span class="sxs-lookup"><span data-stu-id="1b758-109">An entry in the index locates one video frame or waveform-audio buffer.</span></span> <span data-ttu-id="1b758-110">Consequentemente, o valor do tamanho do índice define indiretamente o limite superior no número de quadros que podem ser capturados em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1b758-110">Consequently, the value of the index size indirectly sets the upper limit on the number of frames that can be captured in a file.</span></span>

<span data-ttu-id="1b758-111">Você pode recuperar o tamanho do índice atual usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="1b758-111">You can retrieve the current index size by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="1b758-112">O tamanho atual do índice é armazenado no membro **dwIndexSize** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="1b758-112">The current index size is stored in the **dwIndexSize** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="1b758-113">Você pode especificar um novo tamanho de índice como o valor de **dwIndexSize** e, em seguida, enviar a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="1b758-113">You can specify a new index size as the value of **dwIndexSize** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="1b758-114">O tamanho de índice padrão é 34.952 entradas (permitindo quadros de 32K e um número proporcional de buffers de áudio).</span><span class="sxs-lookup"><span data-stu-id="1b758-114">The default index size is 34,952 entries (allowing 32K frames and a proportional number of audio buffers).</span></span>

 

 




