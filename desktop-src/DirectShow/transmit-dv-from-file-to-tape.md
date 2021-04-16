---
description: Transmitir DV do arquivo para a fita
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Transmitir DV do arquivo para a fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768521"
---
# <a name="transmit-dv-from-file-to-tape"></a><span data-ttu-id="87194-103">Transmitir DV do arquivo para a fita</span><span class="sxs-lookup"><span data-stu-id="87194-103">Transmit DV from File to Tape</span></span>

<span data-ttu-id="87194-104">Transmitir do arquivo DV AVI para a fita VTR é complicado um pouco pelo fato de que os arquivos podem digitar-1 ou tipo-2.</span><span class="sxs-lookup"><span data-stu-id="87194-104">Transmit from DV AVI file to VTR tape is complicated somewhat by the fact that files can type-1 or type-2.</span></span> <span data-ttu-id="87194-105">Para transmitir um arquivo DV para fita, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="87194-105">To transmit a DV file to tape, do the following:</span></span>

1.  <span data-ttu-id="87194-106">Crie uma instância do filtro de [Driver MSDV](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="87194-106">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="87194-107">Para obter mais informações, consulte [selecionando um dispositivo de captura](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="87194-107">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="87194-108">Verifique se o dispositivo está no modo VTR.</span><span class="sxs-lookup"><span data-stu-id="87194-108">Make sure the device is in VTR mode.</span></span> <span data-ttu-id="87194-109">Caso contrário, você não poderá transmitir para fita. Consulte [modo de dispositivo](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="87194-109">Otherwise, you cannot transmit to tape.See [Device Mode](device-mode.md).</span></span>
3.  <span data-ttu-id="87194-110">Inicialize o construtor de gráficos de captura, conforme descrito em [sobre o construtor de grafo de captura](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="87194-110">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
4.  <span data-ttu-id="87194-111">Crie o grafo.</span><span class="sxs-lookup"><span data-stu-id="87194-111">Build the graph.</span></span> <span data-ttu-id="87194-112">A configuração do grafo depende do tipo de arquivo DV:</span><span class="sxs-lookup"><span data-stu-id="87194-112">The graph configuration depends on the DV file type:</span></span>
    -   [<span data-ttu-id="87194-113">Transmitir do arquivo do tipo-1</span><span class="sxs-lookup"><span data-stu-id="87194-113">Transmit from Type-1 File</span></span>](transmit-from-type-1-file.md)
    -   [<span data-ttu-id="87194-114">Transmitir do arquivo do tipo 2</span><span class="sxs-lookup"><span data-stu-id="87194-114">Transmit from Type-2 File</span></span>](transmit-from-type-2-file.md)
5.  <span data-ttu-id="87194-115">Coloque o dispositivo no modo de pausa de registro, conforme descrito em [controlando uma camcorder DV](controlling-a-dv-camcorder.md).</span><span class="sxs-lookup"><span data-stu-id="87194-115">Put the device into record-pause mode, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span>
6.  <span data-ttu-id="87194-116">Pause o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="87194-116">Pause the filter graph.</span></span> <span data-ttu-id="87194-117">Enquanto o grafo de filtro é pausado, ele envia um fluxo contínuo que repete o primeiro quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="87194-117">While the filter graph is paused, it sends a continuous stream that repeats the first frame of video.</span></span>
7.  <span data-ttu-id="87194-118">Para iniciar a transmissão, coloque o dispositivo no modo de registro e, em seguida, execute o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="87194-118">To start transmitting, put the device into record mode and then run the filter graph.</span></span> <span data-ttu-id="87194-119">O dispositivo leva um determinado período de tempo até que a cabeça de gravação seja capaz de gravar, portanto, aguarde cerca de dois segundos antes de executar o grafo.</span><span class="sxs-lookup"><span data-stu-id="87194-119">It takes the device a certain amount of time until the recording head is able to record, so wait for about two seconds before running the graph.</span></span> <span data-ttu-id="87194-120">Isso pode resultar em alguns quadros duplicados no início da fita, mas garante que nenhum dado seja perdido.</span><span class="sxs-lookup"><span data-stu-id="87194-120">This might result in a few duplicated frames at the beginning of the tape, but it ensures that no data is lost.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87194-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87194-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87194-122">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="87194-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



