---
title: Para recuperar amostras compactadas com o leitor síncrono
description: Para recuperar amostras compactadas com o leitor síncrono
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- ASF (Advanced Systems Format), recuperando amostras compactadas
- ASF (formato de sistemas avançados), recuperando amostras compactadas
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- ASF (Advanced Systems Format), amostras compactadas
- ASF (formato de sistemas avançados), amostras compactadas
- leitores síncronos, recuperando amostras compactadas
- leitores síncronos, amostras compactadas
- amostras compactadas, recuperando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084352"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a><span data-ttu-id="3c677-112">Para recuperar amostras compactadas com o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="3c677-112">To Retrieve Compressed Samples with the Synchronous Reader</span></span>

<span data-ttu-id="3c677-113">Como o leitor assíncrono, o leitor síncrono também pode recuperar amostras compactadas.</span><span class="sxs-lookup"><span data-stu-id="3c677-113">Like the asynchronous reader, the synchronous reader can also retrieve compressed samples.</span></span> <span data-ttu-id="3c677-114">Amostras compactadas devem ser usadas ao copiar fluxos de um arquivo para outro.</span><span class="sxs-lookup"><span data-stu-id="3c677-114">Compressed samples should be used when copying streams from one file to another.</span></span>

<span data-ttu-id="3c677-115">O Windows Media Format SDK não fornece nenhum método para decodificar dados depois que ele foi extraído de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="3c677-115">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="3c677-116">Se você receber amostras compactadas e, posteriormente, quiser descompactá-las, precisará fornecer seu próprio código para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="3c677-116">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="3c677-117">Uma maneira de contornar essa limitação é escrever os exemplos compactados em um novo arquivo ASF e, em seguida, lê-los novamente em amostras normais e descompactadas.</span><span class="sxs-lookup"><span data-stu-id="3c677-117">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="3c677-118">Para receber amostras compactadas com o leitor síncrono, chame [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) antes ou durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="3c677-118">To receive compressed samples with the synchronous reader, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) before or during playback.</span></span> <span data-ttu-id="3c677-119">Passe true para *fCompressed*.</span><span class="sxs-lookup"><span data-stu-id="3c677-119">Pass true for *fCompressed*.</span></span>

> [!Note]  
> <span data-ttu-id="3c677-120">Fluxos de imagem não são válidos para entrega de fluxo compactado.</span><span class="sxs-lookup"><span data-stu-id="3c677-120">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="3c677-121">Se você copiar um fluxo de imagem de um arquivo para outro, ele não funcionará no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="3c677-121">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="3c677-122">Para copiar um fluxo de imagem do arquivo para o arquivo, recupere os exemplos de fluxo de imagem por número de saída e inclua-os no novo arquivo como se incluir um novo fluxo de imagem.</span><span class="sxs-lookup"><span data-stu-id="3c677-122">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3c677-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c677-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c677-124">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="3c677-124">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




