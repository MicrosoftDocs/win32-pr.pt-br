---
title: Arquivo desabilitado
description: Arquivo desabilitado
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos desabilitados
- Capas móveis do Windows Media Player, arquivos desabilitados
- capas, arquivos desabilitados
- Arquivos desabilitados em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005768"
---
# <a name="disabled-file"></a><span data-ttu-id="dce20-110">Arquivo desabilitado</span><span class="sxs-lookup"><span data-stu-id="dce20-110">Disabled File</span></span>

<span data-ttu-id="dce20-111">O arquivo desabilitado contém as imagens que serão exibidas quando uma função de botão específica não puder ser usada ou se um estado de botão estiver desativado.</span><span class="sxs-lookup"><span data-stu-id="dce20-111">The Disabled file contains the images that will be displayed when a particular button function cannot be used or a button state is off.</span></span> <span data-ttu-id="dce20-112">Por exemplo, se uma lista de reprodução vazia for definida, os botões **Avançar** e **anterior** serão exibidos e deverão ser exibidos usando uma imagem desabilitada.</span><span class="sxs-lookup"><span data-stu-id="dce20-112">For example, if an empty playlist is defined, the **Next** and **Prev** buttons will be displayed, and they should be displayed using a disabled image.</span></span> <span data-ttu-id="dce20-113">Além disso, para botões de alternância, a imagem desabilitada é usada para indicar que o estado é desativado.</span><span class="sxs-lookup"><span data-stu-id="dce20-113">Also, for toggle buttons, the Disabled image is used to indicate that the state is off.</span></span>

<span data-ttu-id="dce20-114">A imagem a seguir é um arquivo desabilitado típico.</span><span class="sxs-lookup"><span data-stu-id="dce20-114">The following image is a typical Disabled file.</span></span>

![arquivo desabilitado](images/cesdkdis.png)

<span data-ttu-id="dce20-116">Isso armazena as imagens para botões de tipo de clique que estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="dce20-116">This stores the images for hit-type buttons that are disabled.</span></span> <span data-ttu-id="dce20-117">As imagens são semelhantes ao arquivo de plano de fundo, mas as cores são mais claras.</span><span class="sxs-lookup"><span data-stu-id="dce20-117">The images are similar to the Background file, but the colors are lighter.</span></span> <span data-ttu-id="dce20-118">Usando o deslocamento definido na seção bitmaps do arquivo de definição de capa, as imagens de botão são alinhadas com a imagem do arquivo de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="dce20-118">Using the offset defined in the Bitmaps section of the skin definition file, the button images line up with the Background file image.</span></span>

<span data-ttu-id="dce20-119">Observe que o plano de fundo da imagem do botão corresponde exatamente à área correspondente no arquivo de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="dce20-119">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="dce20-120">Isso é importante, porque quando um botão de tipo de ocorrência está indisponível, o retângulo inteiro definido para a imagem desabilitada substituirá a área correspondente no arquivo em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="dce20-120">This is important, because when a hit-type button is unavailable, the entire rectangle defined for the disabled image will replace the matching area in the Background file.</span></span> <span data-ttu-id="dce20-121">Mantenha o gráfico consistente com a imagem de plano de fundo para garantir que apenas as partes do botão que você deseja que sejam diferentes sejam alteradas de fato.</span><span class="sxs-lookup"><span data-stu-id="dce20-121">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dce20-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dce20-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dce20-123">**Arquivos de arte**</span><span class="sxs-lookup"><span data-stu-id="dce20-123">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




