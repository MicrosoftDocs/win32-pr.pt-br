---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Armazenamentos online do Windows Media Player, genre.csv
- lojas online, genre.csv
- Digite 1 lojas online, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916482"
---
# <a name="genrecsv"></a><span data-ttu-id="1177f-107">genre.csv</span><span class="sxs-lookup"><span data-stu-id="1177f-107">genre.csv</span></span>

<span data-ttu-id="1177f-108">Esse arquivo contém uma entrada para cada gênero representado no catálogo.</span><span class="sxs-lookup"><span data-stu-id="1177f-108">This file contains an entry for each genre represented in the catalog.</span></span> <span data-ttu-id="1177f-109">Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1177f-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="1177f-110">Os campos devem aparecer na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="1177f-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="1177f-111">Todos os campos em genre.csv são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1177f-111">All fields in genre.csv are required.</span></span>

<span data-ttu-id="1177f-112">A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado.</span><span class="sxs-lookup"><span data-stu-id="1177f-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="1177f-113">Ele não se refere ao tipo de dados do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1177f-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="1177f-114">Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.</span><span class="sxs-lookup"><span data-stu-id="1177f-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="1177f-115">Campo</span><span class="sxs-lookup"><span data-stu-id="1177f-115">Field</span></span>             | <span data-ttu-id="1177f-116">Formatar</span><span class="sxs-lookup"><span data-stu-id="1177f-116">Format</span></span>                                                    | <span data-ttu-id="1177f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1177f-117">Description</span></span>                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1177f-118">ID do gênero \_</span><span class="sxs-lookup"><span data-stu-id="1177f-118">Genre\_ID</span></span>         | <span data-ttu-id="1177f-119">Inteiro não negativo. Exemplo: 22</span><span class="sxs-lookup"><span data-stu-id="1177f-119">Non-negative integer.Example: 22</span></span><br/>               | <span data-ttu-id="1177f-120">Identificador de gênero, exclusivo dentro de genre.csv.</span><span class="sxs-lookup"><span data-stu-id="1177f-120">Genre identifier, unique within genre.csv.</span></span> <span data-ttu-id="1177f-121">Deve ser menor que 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="1177f-121">Must be less than 2^32.</span></span> <span data-ttu-id="1177f-122">Um máximo de 64 gêneros é possível.</span><span class="sxs-lookup"><span data-stu-id="1177f-122">A maximum of 64 genres is possible.</span></span>                                             |
| <span data-ttu-id="1177f-123">GenreTitle</span><span class="sxs-lookup"><span data-stu-id="1177f-123">GenreTitle</span></span>        | <span data-ttu-id="1177f-124">Cadeia de caracteres Unicode. Exemplo: Rock</span><span class="sxs-lookup"><span data-stu-id="1177f-124">Unicode string.Example: Rock</span></span><br/>                   | <span data-ttu-id="1177f-125">Nome de exibição do gênero.</span><span class="sxs-lookup"><span data-stu-id="1177f-125">Genre display name.</span></span>                                                                                                                                |
| <span data-ttu-id="1177f-126">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="1177f-126">FeedsAreAvailable</span></span> | <span data-ttu-id="1177f-127">Booliano. formato: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="1177f-127">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="1177f-128">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="1177f-128">Example: 0</span></span><br/> | <span data-ttu-id="1177f-129">Indica se o comportamento de "toque de rádio" é possível ao saltar para um feed.</span><span class="sxs-lookup"><span data-stu-id="1177f-129">Indicates whether "radio play" behavior is possible by jumping to a feed.</span></span>                                                                          |
| <span data-ttu-id="1177f-130">HasComposer</span><span class="sxs-lookup"><span data-stu-id="1177f-130">HasComposer</span></span>       | <span data-ttu-id="1177f-131">Booliano. formato: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="1177f-131">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="1177f-132">Example: 1</span><span class="sxs-lookup"><span data-stu-id="1177f-132">Example: 1</span></span><br/> | <span data-ttu-id="1177f-133">True se este gênero deve salvar informações do compositor no catálogo.</span><span class="sxs-lookup"><span data-stu-id="1177f-133">True if this genre should save composer information in the catalog.</span></span> <span data-ttu-id="1177f-134">Se não estiver definido, as informações do Composer serão ignoradas e não compiladas no catálogo.</span><span class="sxs-lookup"><span data-stu-id="1177f-134">If not set, composer information is ignored and not compiled into the catalog.</span></span> |



 

 

 





