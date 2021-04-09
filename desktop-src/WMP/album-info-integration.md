---
title: Integração de informações de álbum
description: Integração de informações de álbum
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Repositórios online do Windows Media Player, integração de informações de álbum
- lojas online, integração de informações de álbum
- tipo 2 lojas online, integração de informações de álbum
- Lojas online do Windows Media Player, integrando informações de álbum
- lojas online, integrando informações de álbum
- Digite 2 lojas online, integrando informações do álbum
- Windows Media Player, integrando informações de álbum
- Windows Media Player, integração de informações de álbum
- integração de informações de álbum
- Integrando informações do álbum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005437"
---
# <a name="album-info-integration"></a><span data-ttu-id="c67de-113">Integração de informações de álbum</span><span class="sxs-lookup"><span data-stu-id="c67de-113">Album Info Integration</span></span>

<span data-ttu-id="c67de-114">O Windows Media Player permite que os usuários solicitem informações detalhadas sobre o CD ou DVD do qual o conteúdo de mídia digital foi originado clicando em um botão, como **mais informações**.</span><span class="sxs-lookup"><span data-stu-id="c67de-114">Windows Media Player enables users to request detailed information about the CD or DVD from which digital media content originated by clicking a button, such as **More Info**.</span></span> <span data-ttu-id="c67de-115">Quando o usuário clica no botão, o Windows Media Player 10 ou posterior chama o repositório de música atual para exibir os detalhes do álbum.</span><span class="sxs-lookup"><span data-stu-id="c67de-115">When the user clicks the button, Windows Media Player 10 or later calls on the current music store to display the album details.</span></span> <span data-ttu-id="c67de-116">Quando isso acontece, o Player abre o painel de informações do álbum e exibe a página da Web especificada pelo atributo **URL** do elemento **AlbumInfo** do documento serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="c67de-116">When this happens, the Player opens the album information pane and displays the webpage specified by the **URL** attribute of the **AlbumInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="c67de-117">O Windows Media Player acrescenta uma cadeia de caracteres de consulta à URL para fornecer informações à loja online sobre o conteúdo solicitado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c67de-117">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user requested.</span></span> <span data-ttu-id="c67de-118">A cadeia de caracteres de consulta inclui atributos como **título**, **álbum** e **artista**, que o repositório online pode usar para determinar o álbum correto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="c67de-118">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to display.</span></span> <span data-ttu-id="c67de-119">A documentação de referência para o elemento **AlbumInfo** fornece a lista completa de atributos de cadeia de caracteres de consulta e suas descrições.</span><span class="sxs-lookup"><span data-stu-id="c67de-119">The reference documentation for the **AlbumInfo** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-album-info"></a><span data-ttu-id="c67de-120">Diretrizes para informações de álbum</span><span class="sxs-lookup"><span data-stu-id="c67de-120">Guidelines for Album Info</span></span>

<span data-ttu-id="c67de-121">Ao criar a página da Web informações do álbum, use as seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="c67de-121">When creating your album information webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="c67de-122">A página deve identificar claramente a loja online que fornece as informações.</span><span class="sxs-lookup"><span data-stu-id="c67de-122">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="c67de-123">Você pode fazer isso exibindo de forma proeminente seu logotipo, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="c67de-123">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="c67de-124">A página deve incluir um link para a política de privacidade da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="c67de-124">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="c67de-125">Evite a navegação de página dentro do recurso de informações do álbum sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="c67de-125">Avoid page navigation within the album information feature whenever possible.</span></span> <span data-ttu-id="c67de-126">Você deve navegar até sua loja online para a maioria das atividades.</span><span class="sxs-lookup"><span data-stu-id="c67de-126">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="c67de-127">Recomendamos que você forneça informações valiosas sem exigir que o usuário instale programas ou faça logon em sua loja online.</span><span class="sxs-lookup"><span data-stu-id="c67de-127">We recommend that you provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c67de-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c67de-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c67de-129">**Sobre as lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="c67de-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c67de-130">**Elemento AlbumInfo**</span><span class="sxs-lookup"><span data-stu-id="c67de-130">**AlbumInfo Element**</span></span>](albuminfo-element.md)
</dt> </dl>

 

 




