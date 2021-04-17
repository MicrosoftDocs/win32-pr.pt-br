---
title: Fluxos de dados arbitrários personalizados
description: Fluxos de dados arbitrários personalizados
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- SDK do Windows Media Format, fluxos de dados arbitrários personalizados
- ASF (Advanced Systems Format), fluxos de dados arbitrários personalizados
- ASF (formato de sistemas avançados), fluxos de dados arbitrários personalizados
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- fluxos de dados arbitrários personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780429"
---
# <a name="custom-arbitrary-data-streams"></a><span data-ttu-id="5c49c-110">Fluxos de dados arbitrários personalizados</span><span class="sxs-lookup"><span data-stu-id="5c49c-110">Custom Arbitrary Data Streams</span></span>

<span data-ttu-id="5c49c-111">Você pode criar um fluxo em um arquivo ASF para conter qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5c49c-111">You can create a stream in an ASF file to contain any sort of data.</span></span> <span data-ttu-id="5c49c-112">Se nenhum dos tipos de fluxo com suporte atender às suas necessidades, você deverá usar um fluxo de dados arbitrário.</span><span class="sxs-lookup"><span data-stu-id="5c49c-112">If none of the supported stream types suits your needs, you must use an arbitrary data stream.</span></span> <span data-ttu-id="5c49c-113">O objeto do gravador manipula um fluxo de dados arbitrários da mesma forma que faz qualquer fluxo descompactado; Os exemplos são incluídos em pacotes e combinados com os exemplos de outros fluxos na seção de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c49c-113">The writer object handles an arbitrary data stream just as it does any uncompressed stream; the samples are packetized and combined with the samples from other streams in the data section of the file.</span></span> <span data-ttu-id="5c49c-114">É claro que apenas um aplicativo de leitura que tenha sido programado especificamente para lidar com seu tipo arbitrário poderá manipular os dados depois que eles forem entregues pelo objeto de leitura.</span><span class="sxs-lookup"><span data-stu-id="5c49c-114">Of course, only a reading application that has been specifically programmed to deal with your arbitrary type will be able to handle the data after it is delivered by the reading object.</span></span>

<span data-ttu-id="5c49c-115">Um uso comum de fluxos de dados arbitrários é para dados de mídia codificados usando um codec de terceiros.</span><span class="sxs-lookup"><span data-stu-id="5c49c-115">One common use of arbitrary data streams is for media data encoded by using a third-party codec.</span></span> <span data-ttu-id="5c49c-116">Como os objetos desse SDK não interagem diretamente com codecs de terceiros, seu aplicativo de escrita deve processar os exemplos com a parte de codificação do codec e passar os exemplos compactados para o gravador.</span><span class="sxs-lookup"><span data-stu-id="5c49c-116">Because the objects of this SDK do not interact directly with third-party codecs, your writing application must process the samples with the encoding portion of the codec and pass the compressed samples to the writer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c49c-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c49c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c49c-118">**Fluxos arbitrários**</span><span class="sxs-lookup"><span data-stu-id="5c49c-118">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="5c49c-119">**Configurando fluxos arbitrários personalizados**</span><span class="sxs-lookup"><span data-stu-id="5c49c-119">**Configuring Custom Arbitrary Streams**</span></span>](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




