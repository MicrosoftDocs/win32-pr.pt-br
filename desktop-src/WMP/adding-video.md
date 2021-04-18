---
title: Adicionando vídeo
description: Adicionando vídeo
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- Criando capas, vídeo
- Capas do Windows Media Player, vídeo
- capas, vídeo
- vídeo em capas, adicionando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783640"
---
# <a name="adding-video"></a><span data-ttu-id="2c0de-107">Adicionando vídeo</span><span class="sxs-lookup"><span data-stu-id="2c0de-107">Adding Video</span></span>

<span data-ttu-id="2c0de-108">Você pode adicionar um vídeo ao seu arquivo simplesmente usando o elemento **Video** e definindo onde deseja que a janela de vídeo seja colocada.</span><span class="sxs-lookup"><span data-stu-id="2c0de-108">You can add a video to your file by simply using the **VIDEO** element and defining where you want the video window to be placed.</span></span>

<span data-ttu-id="2c0de-109">Use o mesmo código que você fez na seção escolhendo arquivos; Tudo o que você precisa fazer é adicionar o elemento de **vídeo** com os atributos superior, esquerdo, largura e altura.</span><span class="sxs-lookup"><span data-stu-id="2c0de-109">Use the same code as you did in the Choosing Files section; all you need to do is add the **VIDEO** element with the top, left, width, and height attributes.</span></span>


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



<span data-ttu-id="2c0de-110">Quando você reproduzir um vídeo, ele será exibido na janela.</span><span class="sxs-lookup"><span data-stu-id="2c0de-110">Then when you play a video, it will be displayed in the window.</span></span> <span data-ttu-id="2c0de-111">A arte para o exemplo de vídeo foi modificada para fazer uma capa ligeiramente maior.</span><span class="sxs-lookup"><span data-stu-id="2c0de-111">The art for the video sample was modified to make a slightly larger skin.</span></span> <span data-ttu-id="2c0de-112">Como as camadas foram usadas no Photoshop, os botões foram facilmente movidos e um novo conjunto foi criado muito rapidamente.</span><span class="sxs-lookup"><span data-stu-id="2c0de-112">Because layers were used in Photoshop, the buttons were easily moved around and a new set was created very quickly.</span></span> <span data-ttu-id="2c0de-113">Somente a imagem de plano de fundo foi alterada.</span><span class="sxs-lookup"><span data-stu-id="2c0de-113">Only the background image was changed.</span></span> <span data-ttu-id="2c0de-114">Um preenchimento foi usado em uma camada em branco e um efeito de bisel e entalhe foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="2c0de-114">A fill was used in a blank layer and a bevel and emboss effect was added.</span></span>

<span data-ttu-id="2c0de-115">Você pode ver uma aparência de vídeo funcional semelhante na seção de exemplo do SDK.</span><span class="sxs-lookup"><span data-stu-id="2c0de-115">You can see a similar working video skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c0de-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c0de-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c0de-117">**Guia de criação de capa**</span><span class="sxs-lookup"><span data-stu-id="2c0de-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




