---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Armazenamentos online do Windows Media Player, listitem.csv
- lojas online, listitem.csv
- Digite 1 lojas online, listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363865"
---
# <a name="listitemcsv"></a><span data-ttu-id="1faf3-107">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="1faf3-107">listitem.csv</span></span>

<span data-ttu-id="1faf3-108">Esse arquivo contém entradas para cada item incluído em uma lista.</span><span class="sxs-lookup"><span data-stu-id="1faf3-108">This file contains entries for each item that is included in a list.</span></span> <span data-ttu-id="1faf3-109">Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1faf3-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="1faf3-110">Os campos devem aparecer na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="1faf3-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="1faf3-111">Todos os campos são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1faf3-111">All fields are required.</span></span>

<span data-ttu-id="1faf3-112">A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado.</span><span class="sxs-lookup"><span data-stu-id="1faf3-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="1faf3-113">Ele não se refere ao tipo de dados do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1faf3-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="1faf3-114">Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.</span><span class="sxs-lookup"><span data-stu-id="1faf3-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="1faf3-115">Campo</span><span class="sxs-lookup"><span data-stu-id="1faf3-115">Field</span></span>              | <span data-ttu-id="1faf3-116">Formatar</span><span class="sxs-lookup"><span data-stu-id="1faf3-116">Format</span></span>                                          | <span data-ttu-id="1faf3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1faf3-117">Description</span></span>                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1faf3-118">\_ListId vinculado</span><span class="sxs-lookup"><span data-stu-id="1faf3-118">Linked\_ListID</span></span>     | <span data-ttu-id="1faf3-119">Inteiro não negativo. Exemplo: 465</span><span class="sxs-lookup"><span data-stu-id="1faf3-119">Non-negative integer.Example: 465</span></span><br/>    | <span data-ttu-id="1faf3-120">A ID da lista da qual este item faz parte.</span><span class="sxs-lookup"><span data-stu-id="1faf3-120">The ID of the list this item is part of.</span></span>                                                                               |
| <span data-ttu-id="1faf3-121">\_ListItem vinculado</span><span class="sxs-lookup"><span data-stu-id="1faf3-121">Linked\_ListItem</span></span>   | <span data-ttu-id="1faf3-122">Inteiro não negativo. Exemplo: 684793</span><span class="sxs-lookup"><span data-stu-id="1faf3-122">Non-negative integer.Example: 684793</span></span><br/> | <span data-ttu-id="1faf3-123">O ID do item.</span><span class="sxs-lookup"><span data-stu-id="1faf3-123">The ID of the item.</span></span> <span data-ttu-id="1faf3-124">Pode ser a ID de uma faixa, um álbum, um artista, um gênero, um subgênero, um feed de rádio ou outra lista.</span><span class="sxs-lookup"><span data-stu-id="1faf3-124">Can be the ID of a track, an album, an artist, a genre, a subgenre, a radio feed, or another list.</span></span> |
| <span data-ttu-id="1faf3-125">ItemPositionInList</span><span class="sxs-lookup"><span data-stu-id="1faf3-125">ItemPositionInList</span></span> | <span data-ttu-id="1faf3-126">Inteiro não negativo. Exemplo: 5</span><span class="sxs-lookup"><span data-stu-id="1faf3-126">Non-negative integer.Example: 5</span></span><br/>      | <span data-ttu-id="1faf3-127">A posição do item dentro de sua lista.</span><span class="sxs-lookup"><span data-stu-id="1faf3-127">The position of the item within its list.</span></span> <span data-ttu-id="1faf3-128">O primeiro item em uma lista está na posição 0.</span><span class="sxs-lookup"><span data-stu-id="1faf3-128">The first item in a list is at position 0.</span></span>                                   |



 

 

 





