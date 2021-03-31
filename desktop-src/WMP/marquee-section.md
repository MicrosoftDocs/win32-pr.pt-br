---
title: Seção de letreiro
description: Seção de letreiro
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Aparências móveis do Windows Media Player, letreiros
- capas, letreiros
- Criando capas, seção Marquee
- escrevendo código para capas, seção Marquee
- letreiros em capas, seção Marquee
- arquivos de definição de capa, seção de letreiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637241"
---
# <a name="marquee-section"></a><span data-ttu-id="ec3f9-109">Seção de letreiro</span><span class="sxs-lookup"><span data-stu-id="ec3f9-109">Marquee Section</span></span>

<span data-ttu-id="ec3f9-110">A seção Marquee contém informações sobre a caixa de texto Marquee, que exibirá o texto de rolagem:</span><span class="sxs-lookup"><span data-stu-id="ec3f9-110">The Marquee section contains information about the marquee text box, which will display scrolling text:</span></span>


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



<span data-ttu-id="ec3f9-111">Isso exibirá o título e o autor do item de mídia atual, embora você possa exibir qualquer tipo de texto no letreiro.</span><span class="sxs-lookup"><span data-stu-id="ec3f9-111">This will display the title and author of the current media item although you can display any text type in the marquee.</span></span> <span data-ttu-id="ec3f9-112">Por exemplo, você também pode incluir nome de arquivo, status e lista de reprodução em seu letreiro.</span><span class="sxs-lookup"><span data-stu-id="ec3f9-112">For example, you could also include Filename, Status, and Playlist in your marquee.</span></span>

> [!Note]  
> <span data-ttu-id="ec3f9-113">Para manter a compatibilidade com versões do Windows Media Player Mobile anteriores ao Windows Media Player 10 Mobile, o uso de "Marquis" em um arquivo de definição de capa ainda é considerado válido.</span><span class="sxs-lookup"><span data-stu-id="ec3f9-113">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="ec3f9-114">Para obter mais informações sobre a seção Marquee, consulte [letreiro](marquee.md) na referência de capa.</span><span class="sxs-lookup"><span data-stu-id="ec3f9-114">For more about the Marquee section, see [Marquee](marquee.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec3f9-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec3f9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec3f9-116">**Escrevendo o código**</span><span class="sxs-lookup"><span data-stu-id="ec3f9-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




