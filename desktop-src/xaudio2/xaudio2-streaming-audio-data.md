---
description: Streaming é o processo de manutenção de apenas uma pequena parte de um arquivo de áudio de reprodução na memória. Isso permite que arquivos de áudio grandes, como música em segundo plano, sejam reproduzidos, e não ocupam uma grande quantidade de memória.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: Dados de áudio de streaming XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762424"
---
# <a name="xaudio2-streaming-audio-data"></a><span data-ttu-id="e053c-104">Dados de áudio de streaming XAudio2</span><span class="sxs-lookup"><span data-stu-id="e053c-104">XAudio2 Streaming Audio Data</span></span>

<span data-ttu-id="e053c-105">Streaming é o processo de manutenção de apenas uma pequena parte de um arquivo de áudio de reprodução na memória.</span><span class="sxs-lookup"><span data-stu-id="e053c-105">Streaming is the process of maintaining only a small portion of a playing audio file in memory.</span></span> <span data-ttu-id="e053c-106">Isso permite que arquivos de áudio grandes, como música em segundo plano, sejam reproduzidos, e não ocupam uma grande quantidade de memória.</span><span class="sxs-lookup"><span data-stu-id="e053c-106">This allows large audio files such as background music to be played, and not take up a large amount of memory.</span></span>

<span data-ttu-id="e053c-107">Quando um arquivo de áudio é transmitido, seus dados são lidos do disco em partes em vez de carregar todo o arquivo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e053c-107">When an audio file is streamed, its data is read from disk in chunks rather than loading the entire file at once.</span></span> <span data-ttu-id="e053c-108">O streaming é feito por meio da leitura assíncrona de dados de áudio em uma fila de buffers de disco.</span><span class="sxs-lookup"><span data-stu-id="e053c-108">Streaming is accomplished by asynchronously reading audio data into a queue of disk buffers.</span></span> <span data-ttu-id="e053c-109">Cada buffer é preenchido e enviado para uma voz de origem.</span><span class="sxs-lookup"><span data-stu-id="e053c-109">Each buffer is filled, and then submitted to a source voice.</span></span> <span data-ttu-id="e053c-110">Depois que a voz termina de reproduzir um buffer, o buffer fica disponível para leitura novamente.</span><span class="sxs-lookup"><span data-stu-id="e053c-110">After the voice finishes playing a buffer, the buffer becomes available for reading again.</span></span> <span data-ttu-id="e053c-111">O loop pelos buffers de disco dessa maneira permite que um arquivo de áudio grande seja reproduzido enquanto apenas uma parte de seus dados é carregada.</span><span class="sxs-lookup"><span data-stu-id="e053c-111">Looping through the disk buffers in this manner allows a large audio file to be played while only a portion of its data is loaded.</span></span> <span data-ttu-id="e053c-112">O código de streaming deve ser colocado em um thread separado, no qual ele pode dormir enquanto aguarda a conclusão de operações de disco e áudio de execução demorada.</span><span class="sxs-lookup"><span data-stu-id="e053c-112">The streaming code should be placed in a separate thread, where it can sleep while waiting for long-running disk and audio operations to finish.</span></span> <span data-ttu-id="e053c-113">Uma classe de retorno de chamada é usada para ativar o thread disparando eventos quando as operações de áudio são concluídas.</span><span class="sxs-lookup"><span data-stu-id="e053c-113">A callback class is used to wake the thread by triggering events when audio operations have finished.</span></span>

<span data-ttu-id="e053c-114">Para obter um exemplo de como o streaming pode ser realizado com o XAudio2, consulte [como transmitir um som do disco](how-to--stream-a-sound-from-disk.md).</span><span class="sxs-lookup"><span data-stu-id="e053c-114">For an example of how streaming can be accomplished with XAudio2, see [How to: Stream a Sound from Disk](how-to--stream-a-sound-from-disk.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e053c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e053c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e053c-116">Transmitindo dados de áudio</span><span class="sxs-lookup"><span data-stu-id="e053c-116">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="e053c-117">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="e053c-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



