---
title: Combinações de texto
description: Combinações de texto
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Aparências móveis do Windows Media Player, letreiros
- capas, letreiros
- referência para capas, letreiros
- letreiros em capas, combinações de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498728"
---
# <a name="text-combinations"></a><span data-ttu-id="6156f-107">Combinações de texto</span><span class="sxs-lookup"><span data-stu-id="6156f-107">Text Combinations</span></span>

<span data-ttu-id="6156f-108">Esse valor é uma lista de combinações de caixa de exibição de texto, separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6156f-108">This value is a list of text display box combinations, separated by commas.</span></span> <span data-ttu-id="6156f-109">As caixas de exibição de texto podem ser Unidas em conjunto por um caractere de adição para criar um novo valor de exibição de letreiro e qualquer tipo de texto definido na seção tipo de texto pode ser usado em seu letreiro.</span><span class="sxs-lookup"><span data-stu-id="6156f-109">Text display boxes can be joined together by a plus character to create a new marquee display value and any text type defined in the Text Type section can be used in your marquee.</span></span>

<span data-ttu-id="6156f-110">Ao determinar o que exibir, o Windows Media Player Mobile avalia cada item na lista para ver se todas as partes estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6156f-110">When determining what to display, Windows Media Player Mobile evaluates each item in the list to see if all parts are available.</span></span> <span data-ttu-id="6156f-111">Caso contrário, o próximo item será avaliado e assim por diante, até que todas as partes disponíveis sejam encontradas.</span><span class="sxs-lookup"><span data-stu-id="6156f-111">If not, the next item is evaluated, and so on, until all the available parts have been found.</span></span> <span data-ttu-id="6156f-112">Por exemplo, se você quiser exibir autor e título, mas não tiver certeza se ambos estão disponíveis, use o seguinte valor:</span><span class="sxs-lookup"><span data-stu-id="6156f-112">For example, if you want to display Author and Title, but you're not sure whether both are available, use the following value:</span></span>


```C++
Title+Author, Title, Author

```



<span data-ttu-id="6156f-113">No exemplo anterior, o título + autor será exibido se o título e o autor tiverem sido definidos para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="6156f-113">In the preceding example, the Title+Author will be displayed if the title and author have been defined for the media item.</span></span> <span data-ttu-id="6156f-114">Se ambos não estiverem definidos, o título será avaliado e exibido se definido.</span><span class="sxs-lookup"><span data-stu-id="6156f-114">If both are not defined, the Title is evaluated and displayed if defined.</span></span> <span data-ttu-id="6156f-115">Se o título não for definido, o autor será exibido, se definido.</span><span class="sxs-lookup"><span data-stu-id="6156f-115">If the Title is not defined, the Author is displayed if defined.</span></span> <span data-ttu-id="6156f-116">Se nenhum for definido, nada será exibido.</span><span class="sxs-lookup"><span data-stu-id="6156f-116">If neither is defined, then nothing is displayed.</span></span>

<span data-ttu-id="6156f-117">Ao usar o sinal de adição para concatenação, certifique-se de que você não tem espaços em nenhum dos lados do sinal de adição.</span><span class="sxs-lookup"><span data-stu-id="6156f-117">When using the plus sign for concatenation, be sure you have no spaces on either side of the plus sign.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6156f-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6156f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6156f-119">**Marquee**</span><span class="sxs-lookup"><span data-stu-id="6156f-119">**Marquee**</span></span>](marquee.md)
</dt> <dt>

[<span data-ttu-id="6156f-120">**Tipo de texto**</span><span class="sxs-lookup"><span data-stu-id="6156f-120">**Text Type**</span></span>](text-type.md)
</dt> </dl>

 

 




