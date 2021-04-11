---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Armazenamentos online do Windows Media Player, artist.csv
- lojas online, artist.csv
- Digite 1 lojas online, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292796"
---
# <a name="artistcsv"></a><span data-ttu-id="922bc-107">artist.csv</span><span class="sxs-lookup"><span data-stu-id="922bc-107">artist.csv</span></span>

<span data-ttu-id="922bc-108">Esse arquivo contém uma entrada para cada artista no catálogo.</span><span class="sxs-lookup"><span data-stu-id="922bc-108">This file contains an entry for each artist in the catalog.</span></span> <span data-ttu-id="922bc-109">Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="922bc-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="922bc-110">Os campos devem aparecer na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="922bc-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="922bc-111">Todos os campos em artist.csv são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="922bc-111">All fields in artist.csv are required.</span></span>

<span data-ttu-id="922bc-112">A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado.</span><span class="sxs-lookup"><span data-stu-id="922bc-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="922bc-113">Ele não se refere ao tipo de dados do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="922bc-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="922bc-114">Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.</span><span class="sxs-lookup"><span data-stu-id="922bc-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="922bc-115">Campo</span><span class="sxs-lookup"><span data-stu-id="922bc-115">Field</span></span>                  | <span data-ttu-id="922bc-116">Formatar</span><span class="sxs-lookup"><span data-stu-id="922bc-116">Format</span></span>                                            | <span data-ttu-id="922bc-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="922bc-117">Description</span></span>                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="922bc-118">Artistaid</span><span class="sxs-lookup"><span data-stu-id="922bc-118">ArtistID</span></span>               | <span data-ttu-id="922bc-119">Inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="922bc-119">Non-negative integer.</span></span> <span data-ttu-id="922bc-120">Exemplo: 65832</span><span class="sxs-lookup"><span data-stu-id="922bc-120">Example: 65832</span></span>              | <span data-ttu-id="922bc-121">Identificador exclusivo para o artista, exclusivo dentro do artist.csv.</span><span class="sxs-lookup"><span data-stu-id="922bc-121">Unique identifier for the artist, unique within artist.csv.</span></span> <span data-ttu-id="922bc-122">Deve ser menor que 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="922bc-122">Must be less than 2^32.</span></span>                        |
| <span data-ttu-id="922bc-123">ArtistName</span><span class="sxs-lookup"><span data-stu-id="922bc-123">ArtistName</span></span>             | <span data-ttu-id="922bc-124">Cadeia de caracteres Unicode. Exemplo: Don funk</span><span class="sxs-lookup"><span data-stu-id="922bc-124">Unicode string.Example: Don Funk</span></span><br/>       | <span data-ttu-id="922bc-125">Nome de exibição do artista.</span><span class="sxs-lookup"><span data-stu-id="922bc-125">Display name for the artist.</span></span>                                                                               |
| <span data-ttu-id="922bc-126">LinkedGenreID</span><span class="sxs-lookup"><span data-stu-id="922bc-126">LinkedGenreID</span></span>          | <span data-ttu-id="922bc-127">Inteiro não negativo. Exemplo: 313</span><span class="sxs-lookup"><span data-stu-id="922bc-127">Non-negative integer.Example: 313</span></span><br/>      | <span data-ttu-id="922bc-128">Gêneroid do gênero principal do artista.</span><span class="sxs-lookup"><span data-stu-id="922bc-128">GenreID of the artist's primary genre.</span></span> <span data-ttu-id="922bc-129">Deve ser um gênero principal e não um subgênero.</span><span class="sxs-lookup"><span data-stu-id="922bc-129">Must be a main genre and not a subgenre.</span></span> <span data-ttu-id="922bc-130">Apenas um valor é permitido.</span><span class="sxs-lookup"><span data-stu-id="922bc-130">Only one value is allowed.</span></span> |
| <span data-ttu-id="922bc-131">LinkedSimilarArtistIDs</span><span class="sxs-lookup"><span data-stu-id="922bc-131">LinkedSimilarArtistIDs</span></span> | <span data-ttu-id="922bc-132">N/D</span><span class="sxs-lookup"><span data-stu-id="922bc-132">N/A</span></span>                                               | <span data-ttu-id="922bc-133">Não usado nesta versão.</span><span class="sxs-lookup"><span data-stu-id="922bc-133">Not used in this release.</span></span> <span data-ttu-id="922bc-134">Deve estar vazio.</span><span class="sxs-lookup"><span data-stu-id="922bc-134">Should be empty.</span></span>                                                                 |
| <span data-ttu-id="922bc-135">Popularidade</span><span class="sxs-lookup"><span data-stu-id="922bc-135">Popularity</span></span>             | <span data-ttu-id="922bc-136">Pode ser um valor inteiro ou Decimal.</span><span class="sxs-lookup"><span data-stu-id="922bc-136">Can be integer or decimal value.</span></span> <span data-ttu-id="922bc-137">Exemplo: 1252,25</span><span class="sxs-lookup"><span data-stu-id="922bc-137">Example: 1252.25</span></span> | <span data-ttu-id="922bc-138">Classificação de popularidade.</span><span class="sxs-lookup"><span data-stu-id="922bc-138">Popularity ranking.</span></span> <span data-ttu-id="922bc-139">Pode ser a posição na lista quando classificada por popularidade.</span><span class="sxs-lookup"><span data-stu-id="922bc-139">Can be the position in the list when sorted by popularity.</span></span>                             |
| <span data-ttu-id="922bc-140">FeedsAvailable</span><span class="sxs-lookup"><span data-stu-id="922bc-140">FeedsAvailable</span></span>         | <span data-ttu-id="922bc-141">Booliano.</span><span class="sxs-lookup"><span data-stu-id="922bc-141">Boolean.</span></span> <span data-ttu-id="922bc-142">Formato: \[ 0 \| 1 \] exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="922bc-142">Format: \[0\|1\]Example: 0</span></span><br/>    | <span data-ttu-id="922bc-143">Não usado nesta versão.</span><span class="sxs-lookup"><span data-stu-id="922bc-143">Not used in this release.</span></span> <span data-ttu-id="922bc-144">Deve estar vazio.</span><span class="sxs-lookup"><span data-stu-id="922bc-144">Should be empty.</span></span>                                                                 |



 

 

 





