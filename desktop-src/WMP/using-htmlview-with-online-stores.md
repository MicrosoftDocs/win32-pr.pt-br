---
title: Usando o HTMLView com lojas online
description: Usando o HTMLView com lojas online
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Armazenamentos online do Windows Media Player, HTMLView
- lojas online, HTMLView
- Digite 1 lojas online, HTMLView
- Digite 2 lojas online, HTMLView
- HTMLView, lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d136be4f7866b6911b8b007de7e784d6133c217
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763435"
---
# <a name="using-htmlview-with-online-stores"></a><span data-ttu-id="ca17d-108">Usando o HTMLView com lojas online</span><span class="sxs-lookup"><span data-stu-id="ca17d-108">Using HTMLView with Online Stores</span></span>

<span data-ttu-id="ca17d-109">O Windows Media Player solicita aos usuários a permissão para exibir o conteúdo do HTMLView no **momento em execução**.</span><span class="sxs-lookup"><span data-stu-id="ca17d-109">Windows Media Player prompts users for permission to display HTMLView content in **Now Playing**.</span></span> <span data-ttu-id="ca17d-110">As lojas online podem desabilitar esse prompt especificando um valor de URL base no elemento **HtmlView** do documento serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="ca17d-110">Online stores can disable this prompt by specifying a base URL value in the **HTMLView** element of the ServiceInfo document.</span></span> <span data-ttu-id="ca17d-111">Quando o Windows Media Player abre uma lista de reprodução que especifica o conteúdo do HTMLView a ser exibido, o Player compara a URL base do documento do serviceInfo do repositório online ativo atual com a URL base do conteúdo do HTMLView.</span><span class="sxs-lookup"><span data-stu-id="ca17d-111">When Windows Media Player opens a playlist that specifies HTMLView content to display, the Player compares the base URL from the ServiceInfo document of the current active online store to the base URL of the HTMLView content.</span></span> <span data-ttu-id="ca17d-112">Se eles corresponderem, o Windows Media Player exibirá o conteúdo do HTMLView sem avisar o usuário.</span><span class="sxs-lookup"><span data-stu-id="ca17d-112">If they match, Windows Media Player displays the HTMLView content without prompting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca17d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca17d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca17d-114">**Exibindo páginas da Web no Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="ca17d-114">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="ca17d-115">**Elemento HTMLView**</span><span class="sxs-lookup"><span data-stu-id="ca17d-115">**HTMLView Element**</span></span>](htmlview-element.md)
</dt> <dt>

[<span data-ttu-id="ca17d-116">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="ca17d-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




