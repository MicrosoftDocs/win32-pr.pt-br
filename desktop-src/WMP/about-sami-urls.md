---
title: Sobre URLs SAMI
description: Sobre URLs SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- Modelo de objeto do Windows Media Player, SAMI (sincronização de mídia acessível)
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player Mobile, SAMI (sincronização de mídia acessível) sincronizado
- Controle ActiveX do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX móvel do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX, SAMI (sincronização de mídia acessível)
- Arquivos SAMI (intercâmbio de mídia acessível) sincronizados
- SAMI (sincronizado com o intercâmbio de mídia acessível), arquivos
- SAMI (sincronização de mídia acessível), URLs
- SAMI (sincronizado com o intercâmbio de mídia acessível), URLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159629"
---
# <a name="about-sami-urls"></a><span data-ttu-id="7bbba-114">Sobre URLs SAMI</span><span class="sxs-lookup"><span data-stu-id="7bbba-114">About SAMI URLs</span></span>

<span data-ttu-id="7bbba-115">Os arquivos SAMI podem ser associados a arquivos de mídia digital usando uma única URL.</span><span class="sxs-lookup"><span data-stu-id="7bbba-115">SAMI files can be associated with digital media files by using a single URL.</span></span> <span data-ttu-id="7bbba-116">Isso é feito usando *o parâmetro de URL Sami* .</span><span class="sxs-lookup"><span data-stu-id="7bbba-116">This is accomplished by using *the sami* URL parameter.</span></span> <span data-ttu-id="7bbba-117">O parâmetro de URL é precedido pela URL base e um?</span><span class="sxs-lookup"><span data-stu-id="7bbba-117">The URL parameter is preceded by the base URL and a ?</span></span> <span data-ttu-id="7bbba-118">.</span><span class="sxs-lookup"><span data-stu-id="7bbba-118">character.</span></span> <span data-ttu-id="7bbba-119">Uma URL com um parâmetro *Sami* segue esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="7bbba-119">A URL with a *sami* parameter follows this syntax:</span></span>

<span data-ttu-id="7bbba-120">*URL*? *Sami* = *captionsURL*.</span><span class="sxs-lookup"><span data-stu-id="7bbba-120">*URL*?*sami*=*captionsURL*.</span></span>

<span data-ttu-id="7bbba-121">O valor do parâmetro URL segue o nome do parâmetro e um sinal de igual, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="7bbba-121">The value of the URL parameter follows the parameter name and an equals sign, as in the following example:</span></span>


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



<span data-ttu-id="7bbba-122">Essa sintaxe de URL é comumente usada em um hiperlink ou um metarquivo do Windows Media para vincular diretamente os locais do arquivo de mídia digital e do arquivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="7bbba-122">This URL syntax is commonly used in a hyperlink or a Windows Media metafile to link directly to the locations of both the digital media file and the SAMI file.</span></span> <span data-ttu-id="7bbba-123">Quando o usuário clica no hiperlink, o Windows Media Player é iniciado no modo completo e reproduz o conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="7bbba-123">When the user clicks on the hyperlink, Windows Media Player launches in full mode and plays the digital media content.</span></span>

<span data-ttu-id="7bbba-124">Se o parâmetro de URL *Sami* não for especificado, o Windows Media Player procurará um arquivo Sami que esteja no mesmo local que o arquivo de mídia digital e que tenha o mesmo nome de arquivo, exceto para a extensão de nome de arquivo, que deve ser. SMI.</span><span class="sxs-lookup"><span data-stu-id="7bbba-124">If the *sami* URL parameter is not specified, Windows Media Player will look for a SAMI file that is in the same location as the digital media file and that has the same file name except for the file name extension, which must be .smi.</span></span> <span data-ttu-id="7bbba-125">Se esse arquivo estiver presente, ele será aberto automaticamente se a exibição da legenda tiver sido habilitada no Player.</span><span class="sxs-lookup"><span data-stu-id="7bbba-125">If such a file is present, it will be opened automatically if caption display has been enabled in the Player.</span></span>

<span data-ttu-id="7bbba-126">As legendas ocultas são habilitadas no Windows Media Player clicando no menu **reproduzir** , clicando em **legendas e legendas** e, em seguida, clicando **em**.</span><span class="sxs-lookup"><span data-stu-id="7bbba-126">Closed captions are enabled in Windows Media Player by clicking the **Play** menu, then clicking **Captions and Subtitles**, and then clicking **On**.</span></span> <span data-ttu-id="7bbba-127">Se as legendas ocultas estiverem habilitadas, as legendas contidas no arquivo SAMI serão exibidas enquanto o item de mídia for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="7bbba-127">If closed captions are enabled, the captions contained in the SAMI file will display while the media item plays.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bbba-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bbba-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bbba-129">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="7bbba-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




