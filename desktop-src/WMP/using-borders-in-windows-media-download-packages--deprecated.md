---
title: Usando bordas em pacotes de download do Windows Media (preterido)
description: Usando bordas em pacotes de download do Windows Media (preterido)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Metaarquivos do Windows Media, pacotes de download do Windows Media
- Windows Media Player, pacotes de download do Windows Media
- metaarquivos, pacotes de download do Windows Media
- Windows Media, pacotes de download do Windows Media
- bordas, sobre
- Pacotes de download do Windows Media, bordas
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364089"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="33618-109">Usando bordas em pacotes de download do Windows Media (preterido)</span><span class="sxs-lookup"><span data-stu-id="33618-109">Using Borders in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="33618-110">Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="33618-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="33618-111">As bordas permitem que você crie uma interface gráfica do usuário personalizada para o conteúdo do pacote.</span><span class="sxs-lookup"><span data-stu-id="33618-111">Borders enable you to create a customized graphical user interface for your packaged content.</span></span> <span data-ttu-id="33618-112">A borda pode incluir elementos como imagens, controles interativos e links para sites.</span><span class="sxs-lookup"><span data-stu-id="33618-112">The border can include elements such as images, interactive controls, and links to websites.</span></span> <span data-ttu-id="33618-113">Você pode usar bordas em casos em que deseja adicionar valor adicional ao conteúdo do pacote, como para identidade visual ou publicidade.</span><span class="sxs-lookup"><span data-stu-id="33618-113">You can use borders in cases where you want to add additional value to your packaged content, such as for branding or advertising.</span></span> <span data-ttu-id="33618-114">Depois que os usuários baixarem e abrirem o pacote de download do Windows Media, o Windows Media Player exibirá automaticamente sua borda personalizada quando ele reproduzir o conteúdo empacotado.</span><span class="sxs-lookup"><span data-stu-id="33618-114">After users download and open your Windows Media Download package, Windows Media Player automatically displays your custom border when it plays the packaged content.</span></span>

<span data-ttu-id="33618-115">Ao contrário de uma capa, que permite que os usuários substituam completamente a interface do usuário do Windows Media Player, uma borda é exibida apenas no painel em **execução** do player de modo completo.</span><span class="sxs-lookup"><span data-stu-id="33618-115">Unlike a skin, which enables users to completely replace the Windows Media Player user interface, a border is displayed only in the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="33618-116">No entanto, as mesmas ferramentas e tecnologias que você usa para criar capas também são usadas para criar bordas.</span><span class="sxs-lookup"><span data-stu-id="33618-116">However, the same tools and technologies that you use to create skins are also used to create borders.</span></span> <span data-ttu-id="33618-117">A ilustração a seguir mostra uma borda.</span><span class="sxs-lookup"><span data-stu-id="33618-117">The following illustration shows a border.</span></span>

![uma borda exibida no Windows Media Player 10](images/border-v10.png)

<span data-ttu-id="33618-119">É importante entender as técnicas básicas para criar uma capa antes de tentar criar uma borda.</span><span class="sxs-lookup"><span data-stu-id="33618-119">It is important to understand the basic techniques for creating a skin before attempting to create a border.</span></span> <span data-ttu-id="33618-120">A programação de borda é realizada usando duas linguagens de programação: linguagem XML (XML) e Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="33618-120">Border programming is accomplished using two programming languages: Extensible Markup Language (XML) and Microsoft JScript.</span></span> <span data-ttu-id="33618-121">O XML é usado para definir elementos de interface, como botões, controles deslizantes e caixas de texto.</span><span class="sxs-lookup"><span data-stu-id="33618-121">XML is used to define interface elements such as buttons, sliders, and text boxes.</span></span> <span data-ttu-id="33618-122">Você não precisa entender todos os detalhes do XML, já que não precisa escrever novos elementos de código XML; Você pode simplesmente usar aquelas fornecidas pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="33618-122">You don't need to understand all the details of XML since you don't have to write new XML code elements; you can simply use the ones provided by Windows Media Player.</span></span> <span data-ttu-id="33618-123">Embora o JScript não seja necessário para a criação de bordas, ele pode ser usado para fornecer funcionalidade adicional.</span><span class="sxs-lookup"><span data-stu-id="33618-123">Although JScript is not required for creating borders, it can be used to provide additional functionality.</span></span>

<span data-ttu-id="33618-124">Um arquivo de borda compactado com uma extensão de nome de arquivo. wmz inclui um arquivo de definição de borda com uma extensão de nome de arquivo. WMS e todos os arquivos de imagem usados dentro da borda.</span><span class="sxs-lookup"><span data-stu-id="33618-124">A compressed border file with a .wmz file name extension includes a border definition file with a .wms file name extension and all the image files used within the border.</span></span>

<span data-ttu-id="33618-125">Para incluir uma borda em um pacote de download do Windows Media, basta criar uma borda e fazer referência a essa borda em uma lista de reprodução do metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="33618-125">To include a border in a Windows Media Download package, simply create a border and reference that border in a Windows Media metafile playlist.</span></span> <span data-ttu-id="33618-126">O arquivo de borda é carregado no Windows Media Player depois que o Player analisa o metarquivo e interpreta o elemento de **capa** que faz referência à borda.</span><span class="sxs-lookup"><span data-stu-id="33618-126">The border file is loaded into Windows Media Player after the Player parses the metafile and interprets the **SKIN** element that references the border.</span></span> <span data-ttu-id="33618-127">O elemento **Skin** é usado somente para as bordas, e o atributo href do elemento **Skin** pode fazer referência a apenas uma capa para cada pacote.</span><span class="sxs-lookup"><span data-stu-id="33618-127">The **SKIN** element is used only for borders, and the HREF attribute of the **SKIN** element can reference only one skin for each package.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33618-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33618-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33618-129">**Bordas do Windows Media Player (preterido)**</span><span class="sxs-lookup"><span data-stu-id="33618-129">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="33618-130">**Pacotes de download do Windows Media (preterido)**</span><span class="sxs-lookup"><span data-stu-id="33618-130">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="33618-131">**Capas do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="33618-131">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




