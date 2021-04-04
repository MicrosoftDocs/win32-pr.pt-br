---
title: Gerenciando blocos de dados por sondagem
description: Gerenciando blocos de dados por sondagem
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- áudio de onda, blocos de dados de sondagem
- blocos de dados de áudio, sondagem
- blocos de dados de áudio de sondagem
- Estrutura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007409"
---
# <a name="managing-data-blocks-by-polling"></a><span data-ttu-id="8e13f-107">Gerenciando blocos de dados por sondagem</span><span class="sxs-lookup"><span data-stu-id="8e13f-107">Managing Data Blocks by Polling</span></span>

<span data-ttu-id="8e13f-108">Além de usar uma função de retorno de chamada, você pode sondar o membro **dwFlags** de uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para determinar quando um dispositivo de áudio é concluído com um bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="8e13f-108">In addition to using a callback function, you can poll the **dwFlags** member of a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to determine when an audio device is finished with a data block.</span></span> <span data-ttu-id="8e13f-109">Às vezes, é melhor sondar **dwFlags** do que esperar que outro mecanismo receba mensagens dos drivers.</span><span class="sxs-lookup"><span data-stu-id="8e13f-109">Sometimes it is better to poll **dwFlags** than to wait for another mechanism to receive messages from the drivers.</span></span> <span data-ttu-id="8e13f-110">Por exemplo, depois de chamar a função [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) para liberar blocos de dados pendentes, você pode sondar imediatamente para certificar-se de que os blocos de dados foram liberados antes de chamar [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) e liberar a memória para o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="8e13f-110">For example, after you call the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function to release pending data blocks, you can immediately poll to be sure that the data blocks have been released before calling [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) and freeing the memory for the data block.</span></span>

<span data-ttu-id="8e13f-111">Você pode usar o \_ sinalizador WHDR Done para testar o membro **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="8e13f-111">You can use the WHDR\_DONE flag to test the **dwFlags** member.</span></span> <span data-ttu-id="8e13f-112">Assim que o sinalizador WHDR \_ concluído é definido no membro **dwFlags** da estrutura **WAVEHDR** , o driver é concluído com o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="8e13f-112">As soon as the WHDR\_DONE flag is set in the **dwFlags** member of the **WAVEHDR** structure, the driver is finished with the data block.</span></span>

 

 