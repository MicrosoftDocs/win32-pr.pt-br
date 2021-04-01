---
title: Usando comandos de script com suporte no Windows Media Player
description: Usando comandos de script com suporte no Windows Media Player
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- SDK do Windows Media Format, comandos de script
- SDK do Windows Media Format, Windows Media Player
- ASF (Advanced Systems Format), comandos de script
- ASF (formato de sistemas avançados), comandos de script
- ASF (Advanced Systems Format), Windows Media Player
- ASF (formato de sistemas avançados), Windows Media Player
- scripts, comandos
- scripts, Windows Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005602"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a><span data-ttu-id="e6cbf-112">Usando comandos de script com suporte no Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="e6cbf-112">Using Script Commands Supported by Windows Media Player</span></span>

<span data-ttu-id="e6cbf-113">O Windows Media Format SDK não fornece suporte nativo para análise e resposta a comandos de script.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-113">The Windows Media Format SDK does not provide native support for parsing and responding to script commands.</span></span> <span data-ttu-id="e6cbf-114">Você deve incluir qualquer lógica relacionada aos comandos de script em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-114">You must include any logic related to script commands in your application.</span></span> <span data-ttu-id="e6cbf-115">Os tipos de script que você usa também devem ser definidos em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-115">The script types that you use must also be defined in your application.</span></span>

<span data-ttu-id="e6cbf-116">Você pode incluir código para lidar com os mesmos comandos de script suportados pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-116">You can include code to handle the same script commands that are supported by Windows Media Player.</span></span> <span data-ttu-id="e6cbf-117">Manter a compatibilidade com o Windows Media Player torna seus arquivos mais universais do que se você inserir comandos de script personalizados.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-117">Maintaining compatibility with Windows Media Player makes your files more universal than if you embed custom script commands.</span></span>

<span data-ttu-id="e6cbf-118">A tabela a seguir lista os tipos de script que têm suporte do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-118">The following table lists script types that are supported by Windows Media Player.</span></span>



| <span data-ttu-id="e6cbf-119">Tipo de script</span><span class="sxs-lookup"><span data-stu-id="e6cbf-119">Script type</span></span> | <span data-ttu-id="e6cbf-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6cbf-120">Description</span></span>                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6cbf-121">URL</span><span class="sxs-lookup"><span data-stu-id="e6cbf-121">URL</span></span>         | <span data-ttu-id="e6cbf-122">O Player envia a URL especificada para o navegador para exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-122">The player sends the specified URL to the browser for display to the user.</span></span> <span data-ttu-id="e6cbf-123">Se um controle de Player inserido estiver sendo usado, você poderá adicionar uma referência de quadro específica à URL usando a sintaxe &&*FrameName* .</span><span class="sxs-lookup"><span data-stu-id="e6cbf-123">If an embedded player control is being used, you can add a specific frame reference to the URL by using the &&*framename* syntax.</span></span>                                                                             |
| <span data-ttu-id="e6cbf-124">NOME do arquivo</span><span class="sxs-lookup"><span data-stu-id="e6cbf-124">FILENAME</span></span>    | <span data-ttu-id="e6cbf-125">Uma URL para outro arquivo de mídia a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-125">A URL to another media file to be played.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="e6cbf-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="e6cbf-126">CAPTION</span></span>     | <span data-ttu-id="e6cbf-127">Uma cadeia de texto que é exibida na área de legendas do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-127">A text string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="e6cbf-128">Esse tipo dá suporte à formatação HTML padrão, portanto, o texto pode ser formatado como desejar.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-128">This type supports standard HTML formatting, so the text can be formatted as you wish.</span></span> <span data-ttu-id="e6cbf-129">Um exemplo de uso é a legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-129">An example of use is closed captioning.</span></span>                                                                             |
| <span data-ttu-id="e6cbf-130">CIRCUNSTÂNCIA</span><span class="sxs-lookup"><span data-stu-id="e6cbf-130">EVENT</span></span>       | <span data-ttu-id="e6cbf-131">O nome de um evento que deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-131">The name of an event that is to occur.</span></span> <span data-ttu-id="e6cbf-132">O tipo de evento dá suporte à personalização para seus próprios usos.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-132">The EVENT type supports customization for your own uses.</span></span> <span data-ttu-id="e6cbf-133">O código para o evento especificado deve ser definido no metarquivo do Windows Media para o fluxo para que o Player execute o evento especificado.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-133">The code for the specified event must be defined in the Windows Media metafile for the stream in order for the player to perform the specified event.</span></span> <span data-ttu-id="e6cbf-134">Um exemplo de uso é a inserção de anúncios.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-134">An example of use is ad insertion.</span></span> |
| <span data-ttu-id="e6cbf-135">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="e6cbf-135">OPENEVENT</span></span>   | <span data-ttu-id="e6cbf-136">Esse script precede o evento real.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-136">This script precedes the actual EVENT.</span></span> <span data-ttu-id="e6cbf-137">O OPENEVENT permite que o Player bufferu previamente o conteúdo para que, quando o evento ocorrer, a mudança entre os fluxos pareça ser direta.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-137">The OPENEVENT allows the player to pre-buffer the content so that when the EVENT occurs, the switch between streams appears to be seamless.</span></span>                                                                                                       |
| <span data-ttu-id="e6cbf-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="e6cbf-138">TEXT</span></span>        | <span data-ttu-id="e6cbf-139">Uma cadeia de texto que é exibida na área de legendas do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-139">A TEXT string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="e6cbf-140">Pode ser texto sem formatação, SAMI ou HTML formatado.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-140">Can be plain text, SAMI, or HTML formatted text.</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="e6cbf-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6cbf-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6cbf-142">**Usando comandos de script**</span><span class="sxs-lookup"><span data-stu-id="e6cbf-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




