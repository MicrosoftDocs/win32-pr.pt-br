---
title: Lendo metadados na reprodução
description: Lendo metadados na reprodução
ms.assetid: 48d37a9e-5e22-4298-abc4-b69998906dcb
keywords:
- SDK do Windows Media Format, lendo metadados
- SDK do Windows Media Format, leitores assíncronos
- SDK do Windows Media Format, leitores síncronos
- ASF (Advanced Systems Format), lendo metadados
- ASF (formato de sistemas avançados), lendo metadados
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- leitores assíncronos, lendo metadados
- leitores síncronos, lendo metadados
- metadados, lendo na reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a2515dd62092d02a45b0261fe2b501e0833a31
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007230"
---
# <a name="reading-metadata-at-playback"></a><span data-ttu-id="d4715-115">Lendo metadados na reprodução</span><span class="sxs-lookup"><span data-stu-id="d4715-115">Reading Metadata at Playback</span></span>

<span data-ttu-id="d4715-116">O objeto leitor assíncrono e o objeto leitor síncrono podem ler os metadados do cabeçalho de um arquivo ASF carregado.</span><span class="sxs-lookup"><span data-stu-id="d4715-116">Both the asynchronous reader object and the synchronous reader object can read the metadata from the header of a loaded ASF file.</span></span> <span data-ttu-id="d4715-117">Ao ler arquivos, os atributos de metadados são todos somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d4715-117">When reading files, the metadata attributes are all read-only.</span></span> <span data-ttu-id="d4715-118">Ambos os objetos de leitura podem ser consultados para as interfaces [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) e [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="d4715-118">Both reader objects can be queried for the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interfaces.</span></span>

<span data-ttu-id="d4715-119">Para obter mais informações sobre como acessar metadados, consulte [trabalhando com metadados](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="d4715-119">For more information about accessing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4715-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4715-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4715-121">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="d4715-121">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




