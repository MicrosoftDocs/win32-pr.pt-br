---
title: Objeto de propriedades de mídia de entrada
description: Objeto de propriedades de mídia de entrada
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- SDK do Windows Media Format, objetos de propriedades de mídia de entrada
- ASF (Advanced Systems Format), objetos de propriedades de mídia de entrada
- ASF (formato de sistemas avançados), objetos de propriedades de mídia de entrada
- objetos, objetos de propriedades de mídia de entrada
- objetos de propriedades de mídia de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823558"
---
# <a name="input-media-properties-object"></a><span data-ttu-id="e5a7b-108">Objeto de propriedades de mídia de entrada</span><span class="sxs-lookup"><span data-stu-id="e5a7b-108">Input Media Properties Object</span></span>

<span data-ttu-id="e5a7b-109">Um objeto de propriedades de mídia de entrada criado pelo objeto gravador dá suporte às seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="e5a7b-109">An input media properties object created by the writer object supports the following interfaces.</span></span> <span data-ttu-id="e5a7b-110">Essas interfaces são acessadas por uma chamada para **QueryInterface** em uma das interfaces do objeto Writer.</span><span class="sxs-lookup"><span data-stu-id="e5a7b-110">These interfaces are accessed by a call to **QueryInterface** on one of the interfaces of the writer object.</span></span>



| <span data-ttu-id="e5a7b-111">Interface</span><span class="sxs-lookup"><span data-stu-id="e5a7b-111">Interface</span></span>                                        | <span data-ttu-id="e5a7b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5a7b-112">Description</span></span>                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5a7b-113">**IWMInputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="e5a7b-113">**IWMInputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | <span data-ttu-id="e5a7b-114">Recupera as propriedades de um fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e5a7b-114">Retrieves the properties of an input stream.</span></span>                                                               |
| [<span data-ttu-id="e5a7b-115">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="e5a7b-115">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="e5a7b-116">Usado como interface base para as outras interfaces de propriedade de mídia (entrada, saída e vídeo).</span><span class="sxs-lookup"><span data-stu-id="e5a7b-116">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="e5a7b-117">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="e5a7b-117">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="e5a7b-118">Gerencia as propriedades de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e5a7b-118">Manages the properties of a video stream.</span></span> <span data-ttu-id="e5a7b-119">Essa é uma interface opcional, disponível apenas para fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e5a7b-119">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e5a7b-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5a7b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a7b-121">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="e5a7b-121">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="e5a7b-122">**Objeto do gravador**</span><span class="sxs-lookup"><span data-stu-id="e5a7b-122">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




