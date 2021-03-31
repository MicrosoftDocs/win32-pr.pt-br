---
title: Seção de descrição
description: Seção de descrição
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Capas móveis do Windows Media Player, seção Descrição
- capas, seção de descrição
- Criando capas, seção de descrição
- escrevendo código para capas, seção de descrição
- Seção de descrição em capas
- arquivos de definição de capa, seção de descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822958"
---
# <a name="description-section"></a><span data-ttu-id="af10c-109">Seção de descrição</span><span class="sxs-lookup"><span data-stu-id="af10c-109">Description Section</span></span>

<span data-ttu-id="af10c-110">Em seguida, você deve fornecer uma seção que descreve o tamanho e a orientação da capa ao criar uma capa para o Windows Media Player 9 Series para Windows Mobile 2003 e versões posteriores:</span><span class="sxs-lookup"><span data-stu-id="af10c-110">Next, you must provide a section that describes the size and orientation of the skin when creating a skin for Windows Media Player 9 Series for Windows Mobile 2003 and later versions:</span></span>


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



<span data-ttu-id="af10c-111">A seção descrição deve começar com a palavra descrição entre colchetes e, em seguida, incluir uma linha que especifica as dimensões e a resolução de exibição da capa.</span><span class="sxs-lookup"><span data-stu-id="af10c-111">The Description section must begin with the word Description in brackets, and then include a line that specifies the dimensions and display resolution for the skin.</span></span>

<span data-ttu-id="af10c-112">As linhas que começam com duas barras invertidas não são processadas e podem ser usadas para comentários ou, conforme mostrado no código anterior, um modelo para ajudá-lo a se lembrar do que acontece em uma seção.</span><span class="sxs-lookup"><span data-stu-id="af10c-112">Lines beginning with two forward slashes are not processed, and can be used for comments or, as shown in the previous code, a template to help you remember what goes in a section.</span></span> <span data-ttu-id="af10c-113">Você também pode usar modelos para ajudar a alinhar tudo em colunas.</span><span class="sxs-lookup"><span data-stu-id="af10c-113">You can also use templates to help align everything into columns.</span></span>

<span data-ttu-id="af10c-114">Para obter mais informações sobre a seção Descrição, consulte [Descrição](description.md) na referência de capa.</span><span class="sxs-lookup"><span data-stu-id="af10c-114">For more information about the Description section, see [Description](description.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af10c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af10c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af10c-116">**Escrevendo o código**</span><span class="sxs-lookup"><span data-stu-id="af10c-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




