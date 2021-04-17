---
title: Super arquivos
description: Super arquivos
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos de Super arquivos
- Capas móveis do Windows Media Player, arquivos de superarquivos
- capas, Super arquivos
- Super arquivos em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105812232"
---
# <a name="super-files"></a><span data-ttu-id="4fb2b-110">Super arquivos</span><span class="sxs-lookup"><span data-stu-id="4fb2b-110">Super Files</span></span>

<span data-ttu-id="4fb2b-111">Super arquivos são usados para armazenar as imagens desabilitadas para trackbars.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-111">Super files are used to store the Disabled images for trackbars.</span></span> <span data-ttu-id="4fb2b-112">Como a imagem principal do TrackBar é exibida no arquivo em segundo plano e o usuário toca na imagem do Thumb, não na imagem do TrackBar, apenas a imagem desabilitada é necessária para trackbars.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-112">Because the main trackbar image is displayed in the Background file, and the user taps on the thumb image, not the trackbar image, only the Disabled image is needed for trackbars.</span></span> <span data-ttu-id="4fb2b-113">Ele é armazenado no arquivo definido por super na seção bitmaps do arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-113">It is stored in the file defined by Super in the Bitmaps section of the skin definition file.</span></span> <span data-ttu-id="4fb2b-114">Um superarquivo também pode armazenar as imagens enviadas e desativadas para outros botões, como mudo, o que não é necessário para um botão de tipo de clique.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-114">A Super file can also store the Pushed and Disabled images for other buttons such as Mute, which is not required to be a hit-type button.</span></span>

> [!Note]  
> <span data-ttu-id="4fb2b-115">Arquivos de superarte não são usados em capas para o Windows Media Player 10 Mobile ou posterior porque as imagens desabilitadas para o trackbars de busca estão localizadas no arquivo seekthumb.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-115">Super art files are not used in skins for Windows Media Player 10 Mobile or later because the disabled images for seek trackbars are located in the seekthumb file.</span></span>

 

<span data-ttu-id="4fb2b-116">A imagem a seguir é um super arquivo típico.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-116">The following image is a typical Super file.</span></span>

![Super arquivo](images/cesdksup.png)

<span data-ttu-id="4fb2b-118">Isso armazena as imagens desabilitadas para o trackbars e o botão mudo.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-118">This stores the disabled images for the trackbars and the mute button.</span></span> <span data-ttu-id="4fb2b-119">Essas imagens são deslocadas conforme definido pela seção bitmaps.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-119">These images are offset as defined by the Bitmaps section.</span></span>

<span data-ttu-id="4fb2b-120">A área de plano de fundo da imagem TrackBar desabilitada corresponde exatamente à área correspondente no arquivo de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-120">The background area of the disabled trackbar image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="4fb2b-121">Isso é importante, pois o retângulo inteiro definido para a imagem TrackBar desabilitada substituirá a área correspondente no arquivo de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-121">This is important, because the entire rectangle defined for the disabled trackbar image will replace the matching area in the Background file.</span></span> <span data-ttu-id="4fb2b-122">Isso garante que a imagem TrackBar desabilitada se misture diretamente na imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="4fb2b-122">This ensures that the disabled trackbar image blends seamlessly into the background image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fb2b-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4fb2b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fb2b-124">**Arquivos de arte**</span><span class="sxs-lookup"><span data-stu-id="4fb2b-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




