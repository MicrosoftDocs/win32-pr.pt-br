---
title: Enumeração de formato de saída
description: Enumeração de formato de saída
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- SDK do Windows Media Format, enumerações de formato de saída
- ASF (Advanced Systems Format), enumerações de formato de saída
- ASF (formato de sistemas avançados), enumerações de formato de saída
- SDK do Windows Media Format, interface IWMReaderTypeNegotiation
- Formato de sistema avançado (ASF), interface IWMReaderTypeNegotiation
- ASF (formato de sistemas avançados), interface IWMReaderTypeNegotiation
- enumerações de formato de saída
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007066"
---
# <a name="output-format-enumeration"></a><span data-ttu-id="0d5c8-111">Enumeração de formato de saída</span><span class="sxs-lookup"><span data-stu-id="0d5c8-111">Output Format Enumeration</span></span>

<span data-ttu-id="0d5c8-112">O objeto leitor e o objeto leitor síncrono se comunicam com os codecs para enumerar os formatos de saída possíveis para fluxos compactados.</span><span class="sxs-lookup"><span data-stu-id="0d5c8-112">Both the reader object and the synchronous reader object communicate with the codecs to enumerate the possible output formats for compressed streams.</span></span> <span data-ttu-id="0d5c8-113">Ao ler um arquivo com conteúdo compactado com um ou mais dos codecs de mídia do Windows, você pode examinar os possíveis formatos de saída para escolher aquele que melhor atenda às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="0d5c8-113">When you read a file containing content compressed with one or more of the Windows Media codecs, you can examine the possible output formats to choose the one that best suits your needs.</span></span> <span data-ttu-id="0d5c8-114">Para sua conveniência, cada codec tem um formato de saída padrão que é definido para o formato usado com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="0d5c8-114">For convenience, each codec has a default output format which is set to the most commonly used format.</span></span> <span data-ttu-id="0d5c8-115">Para obter mais informações sobre a enumeração de saída, consulte [trabalhando com saídas](working-with-outputs.md).</span><span class="sxs-lookup"><span data-stu-id="0d5c8-115">For more information about output enumeration, see [Working with Outputs](working-with-outputs.md).</span></span>

<span data-ttu-id="0d5c8-116">Você pode fazer determinadas alterações em um formato de saída, dependendo do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="0d5c8-116">You can make certain changes to an output format depending upon the media type.</span></span> <span data-ttu-id="0d5c8-117">Para fluxos de vídeo, por exemplo, você pode alterar o tamanho do quadro e a intensidade da cor.</span><span class="sxs-lookup"><span data-stu-id="0d5c8-117">For video streams, for example, you can change the frame size and color depth.</span></span> <span data-ttu-id="0d5c8-118">Os objetos de leitura dão suporte a uma interface para testar as alterações feitas no formato de saída, chamado [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span><span class="sxs-lookup"><span data-stu-id="0d5c8-118">The reading objects both support an interface to test changes you make to the output format, called [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d5c8-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d5c8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d5c8-120">**Recursos de leitura de arquivo**</span><span class="sxs-lookup"><span data-stu-id="0d5c8-120">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




