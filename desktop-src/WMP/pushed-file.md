---
title: Arquivo enviado por push
description: Arquivo enviado por push
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos enviados por push
- Capas móveis do Windows Media Player, arquivos enviados por push
- capas, arquivos enviados por push
- Arquivos enviados por push em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364083"
---
# <a name="pushed-file"></a><span data-ttu-id="8e9f4-110">Arquivo enviado por push</span><span class="sxs-lookup"><span data-stu-id="8e9f4-110">Pushed File</span></span>

<span data-ttu-id="8e9f4-111">O arquivo enviado contém as imagens que serão exibidas quando o usuário tocar em um botão.</span><span class="sxs-lookup"><span data-stu-id="8e9f4-111">The Pushed file contains the images that will be displayed when the user taps on a button.</span></span> <span data-ttu-id="8e9f4-112">Você também pode incluir as imagens normal e push para o estado de pausa do botão PlayPause.</span><span class="sxs-lookup"><span data-stu-id="8e9f4-112">You can also include the normal and pushed images for the pause state of the PlayPause button.</span></span>

<span data-ttu-id="8e9f4-113">A imagem a seguir é um arquivo Push típico.</span><span class="sxs-lookup"><span data-stu-id="8e9f4-113">The following image is a typical Pushed file.</span></span>

![arquivo enviado por push](images/cesdkpus.png)

<span data-ttu-id="8e9f4-115">Isso armazena as imagens que serão exibidas quando os botões de tipo de clique forem tocados.</span><span class="sxs-lookup"><span data-stu-id="8e9f4-115">This stores the images that will be displayed when the hit-type buttons are tapped.</span></span> <span data-ttu-id="8e9f4-116">Também armazenados nesse arquivo são as imagens normais e enviadas por push para a imagem pausada do botão PlayPause.</span><span class="sxs-lookup"><span data-stu-id="8e9f4-116">Also stored in this file are the normal and pushed images for the paused image of the PlayPause button.</span></span> <span data-ttu-id="8e9f4-117">Exceto pelas imagens secundárias PlayPause à direita, as outras imagens de botão são alinhadas com a imagem de plano de fundo, usando o deslocamento definido na seção bitmaps do arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="8e9f4-117">Except for the PlayPause secondary images on the right, the other button images line up with the Background image, using the offset defined in the Bitmaps section of the skin definition file.</span></span>

<span data-ttu-id="8e9f4-118">Observe que o plano de fundo da imagem do botão corresponde exatamente à área correspondente no arquivo de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="8e9f4-118">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="8e9f4-119">Isso é importante, porque quando o usuário toca em um botão de tipo de ocorrência, o retângulo inteiro definido para a imagem enviada por push substituirá a área correspondente no arquivo em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="8e9f4-119">This is important, because when the user taps a hit-type button, the entire rectangle defined for the pushed image will replace the matching area in the Background file.</span></span> <span data-ttu-id="8e9f4-120">Mantenha o gráfico consistente com a imagem de plano de fundo para garantir que apenas as partes do botão que você deseja que sejam diferentes sejam alteradas de fato.</span><span class="sxs-lookup"><span data-stu-id="8e9f4-120">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e9f4-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e9f4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e9f4-122">**Arquivos de arte**</span><span class="sxs-lookup"><span data-stu-id="8e9f4-122">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




