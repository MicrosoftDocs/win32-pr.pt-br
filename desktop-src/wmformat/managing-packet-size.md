---
title: Gerenciamento do tamanho do pacote
description: Gerenciamento do tamanho do pacote
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- SDK do Windows Media Format, gerenciando tamanhos de pacotes
- SDK do Windows Media Format, tamanhos de pacotes
- perfis, tamanhos de pacotes
- perfis, gerenciando tamanhos de pacotes
- pacotes, tamanhos
- pacotes, interface IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365750"
---
# <a name="managing-packet-size"></a><span data-ttu-id="ba750-110">Gerenciamento do tamanho do pacote</span><span class="sxs-lookup"><span data-stu-id="ba750-110">Managing Packet Size</span></span>

<span data-ttu-id="ba750-111">O gravador foi projetado para gerenciar o tamanho dos pacotes internamente.</span><span class="sxs-lookup"><span data-stu-id="ba750-111">The writer is designed to manage the size of packets internally.</span></span> <span data-ttu-id="ba750-112">No entanto, você pode ter requisitos específicos para seu aplicativo que chamam algum controle manual sobre o tamanho dos pacotes nos arquivos ASF que você escreve.</span><span class="sxs-lookup"><span data-stu-id="ba750-112">However, you may have specific requirements for your application that call for some manual control over the size of packets in the ASF files that you write.</span></span> <span data-ttu-id="ba750-113">O Windows Media Format SDK fornece duas interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) e [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , que permitem controlar o tamanho máximo e mínimo dos pacotes.</span><span class="sxs-lookup"><span data-stu-id="ba750-113">The Windows Media Format SDK provides two interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) and [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) that enable you to control the maximum and minimum size of packets.</span></span>

<span data-ttu-id="ba750-114">Ambas as interfaces de tamanho de pacote são expostas no objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="ba750-114">Both packet size interfaces are exposed in the profile object.</span></span> <span data-ttu-id="ba750-115">Eles também estão disponíveis para o objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="ba750-115">They are also available to the reader object.</span></span> <span data-ttu-id="ba750-116">Assim como acontece com outras interfaces relacionadas a perfil, o leitor pode acessar apenas os métodos de leitura.</span><span class="sxs-lookup"><span data-stu-id="ba750-116">As with other profile-related interfaces, the reader can access only the reading methods.</span></span>

<span data-ttu-id="ba750-117">O tamanho dos pacotes tem algum efeito sobre o desempenho.</span><span class="sxs-lookup"><span data-stu-id="ba750-117">The size of packets has some effect on performance.</span></span> <span data-ttu-id="ba750-118">Em geral, quanto menor o tamanho do pacote, mais fragmentados os dados estão dentro de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="ba750-118">In general, the smaller the packet size, the more fragmented the data is within a file.</span></span> <span data-ttu-id="ba750-119">Quanto mais fragmentado um arquivo for, menos eficiente será reconstruí-lo.</span><span class="sxs-lookup"><span data-stu-id="ba750-119">The more fragmented a file is, the less efficient it will be to reconstruct it.</span></span> <span data-ttu-id="ba750-120">Em um cenário de streaming, isso pode não ser uma consideração importante, pois o processo de leitura de um arquivo de uma fonte da Internet geralmente é ineficiente.</span><span class="sxs-lookup"><span data-stu-id="ba750-120">In a streaming scenario, this may not be an important consideration, as the process of reading a file from an Internet source is generally inefficient.</span></span> <span data-ttu-id="ba750-121">Ao lidar com um arquivo localmente no entanto, isso pode ser uma consideração.</span><span class="sxs-lookup"><span data-stu-id="ba750-121">When dealing with a file locally however, this might be a consideration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba750-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba750-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba750-123">**Interface IWMPacketSize**</span><span class="sxs-lookup"><span data-stu-id="ba750-123">**IWMPacketSize Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[<span data-ttu-id="ba750-124">**Interface IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="ba750-124">**IWMPacketSize2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[<span data-ttu-id="ba750-125">**Trabalhando com perfis**</span><span class="sxs-lookup"><span data-stu-id="ba750-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




