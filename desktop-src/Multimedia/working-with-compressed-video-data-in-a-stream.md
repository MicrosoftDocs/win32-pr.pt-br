---
title: Trabalhando com dados de vídeo compactados em um fluxo
description: Trabalhando com dados de vídeo compactados em um fluxo
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007442"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a><span data-ttu-id="3457f-103">Trabalhando com dados de vídeo compactados em um fluxo</span><span class="sxs-lookup"><span data-stu-id="3457f-103">Working with Compressed Video Data in a Stream</span></span>

<span data-ttu-id="3457f-104">O AVIFile fornece várias maneiras de acessar fluxos de vídeo compactados.</span><span class="sxs-lookup"><span data-stu-id="3457f-104">AVIFile provides several ways for you to access compressed video streams.</span></span>

<span data-ttu-id="3457f-105">Se você quiser exibir um ou mais quadros de um fluxo de vídeo compactado, poderá recuperar os quadros usando a função [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) e encaminhar os dados do quadro compactado para o DrawDib Functions para exibi-los.</span><span class="sxs-lookup"><span data-stu-id="3457f-105">If you want to display one or more frames of a compressed video stream, you can retrieve the frames by using the [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) function and forwarding the compressed frame data to DrawDib functions to display them.</span></span> <span data-ttu-id="3457f-106">As funções DrawDib podem exibir imagens de várias profundidades de imagem e pontilhar automaticamente imagens para exibições que não podem lidar com certos tipos de bitmaps independentes de dispositivo (DIBs).</span><span class="sxs-lookup"><span data-stu-id="3457f-106">DrawDib functions can display images of several image depths and automatically dither images for displays that cannot handle certain types of device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="3457f-107">Essas funções funcionam com imagens compactadas e descompactadas.</span><span class="sxs-lookup"><span data-stu-id="3457f-107">These functions work with uncompressed and compressed images.</span></span> <span data-ttu-id="3457f-108">Para obter mais informações sobre as funções do DrawDib, consulte [funções do DrawDib](drawdib-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3457f-108">For more information about DrawDib functions, see [DrawDib Functions](drawdib-functions.md).</span></span>

<span data-ttu-id="3457f-109">O AVIFile fornece funções para descompactar um único quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3457f-109">AVIFile provides functions for decompressing a single video frame.</span></span> <span data-ttu-id="3457f-110">Para alocar recursos, use a função [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) .</span><span class="sxs-lookup"><span data-stu-id="3457f-110">To allocate resources, use the [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) function.</span></span> <span data-ttu-id="3457f-111">Essa função cria um buffer para os dados descompactados.</span><span class="sxs-lookup"><span data-stu-id="3457f-111">This function creates a buffer for the decompressed data.</span></span>

<span data-ttu-id="3457f-112">Você pode descompactar um único quadro de vídeo usando a função [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) .</span><span class="sxs-lookup"><span data-stu-id="3457f-112">You can decompress a single video frame by using the [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) function.</span></span> <span data-ttu-id="3457f-113">Essa função descompacta o quadro e recupera um quadro completo de dados de imagem, retornando o endereço do DIB na estrutura [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3457f-113">This function decompresses the frame and retrieves a complete frame of image data, returning the address of the DIB in the [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) structure.</span></span> <span data-ttu-id="3457f-114">Seu aplicativo pode exibir o DIB usando funções de desenho padrão ou usando as funções DrawDib.</span><span class="sxs-lookup"><span data-stu-id="3457f-114">Your application can display the DIB by using standard drawing functions or by using the DrawDib functions.</span></span>

<span data-ttu-id="3457f-115">Se seu aplicativo fizer chamadas sucessivas para **AVIStreamGetFrame**, a função substituirá seu buffer por cada quadro recuperado.</span><span class="sxs-lookup"><span data-stu-id="3457f-115">If your application makes successive calls to **AVIStreamGetFrame**, the function overwrites its buffer with each retrieved frame.</span></span>

<span data-ttu-id="3457f-116">Quando você terminar de usar o **AVIStreamGetFrame** e o DIB descompactado estiver em seu buffer, poderá liberar os recursos alocados usando a função [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) .</span><span class="sxs-lookup"><span data-stu-id="3457f-116">When you finish using **AVIStreamGetFrame** and the decompressed DIB is in its buffer, you can release the allocated resources by using the [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) function.</span></span>

<span data-ttu-id="3457f-117">Para obter mais informações sobre como descompactar imagens, consulte [Gerenciador de compactação de vídeo](video-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="3457f-117">For more information about decompressing images, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 