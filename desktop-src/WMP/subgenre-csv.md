---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Armazenamentos online do Windows Media Player, subgenre.csv
- lojas online, subgenre.csv
- Digite 1 lojas online, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765349"
---
# <a name="subgenrecsv"></a><span data-ttu-id="ff562-107">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="ff562-107">subgenre.csv</span></span>

<span data-ttu-id="ff562-108">Esse arquivo contém uma entrada para cada subgênero representado no catálogo.</span><span class="sxs-lookup"><span data-stu-id="ff562-108">This file contains an entry for each subgenre represented in the catalog.</span></span> <span data-ttu-id="ff562-109">Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff562-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="ff562-110">Os campos devem aparecer na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="ff562-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="ff562-111">A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado.</span><span class="sxs-lookup"><span data-stu-id="ff562-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="ff562-112">Ele não se refere ao tipo de dados do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ff562-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="ff562-113">Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.</span><span class="sxs-lookup"><span data-stu-id="ff562-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="ff562-114">Campo</span><span class="sxs-lookup"><span data-stu-id="ff562-114">Field</span></span>             | <span data-ttu-id="ff562-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ff562-115">Required</span></span> | <span data-ttu-id="ff562-116">Formatar</span><span class="sxs-lookup"><span data-stu-id="ff562-116">Format</span></span>                                                                                            | <span data-ttu-id="ff562-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff562-117">Description</span></span>                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff562-118">Subgêneroid</span><span class="sxs-lookup"><span data-stu-id="ff562-118">SubGenreID</span></span>        | <span data-ttu-id="ff562-119">Sim</span><span class="sxs-lookup"><span data-stu-id="ff562-119">Yes</span></span>      | <span data-ttu-id="ff562-120">Inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="ff562-120">Non-negative integer.</span></span>                                                                             | <span data-ttu-id="ff562-121">Identificador de subgênero (ID), exclusivo dentro de subgenre.csv.</span><span class="sxs-lookup"><span data-stu-id="ff562-121">Subgenre identifier (ID), unique within subgenre.csv.</span></span> <span data-ttu-id="ff562-122">Até 1024 subgêneros são permitidos.</span><span class="sxs-lookup"><span data-stu-id="ff562-122">Up to 1024 subgenres are allowed.</span></span>                                                                   |
| <span data-ttu-id="ff562-123">SubGenreTitle</span><span class="sxs-lookup"><span data-stu-id="ff562-123">SubGenreTitle</span></span>     | <span data-ttu-id="ff562-124">Sim</span><span class="sxs-lookup"><span data-stu-id="ff562-124">Yes</span></span>      | <span data-ttu-id="ff562-125">Cadeia de caracteres Unicode. Exemplo: música de dança inteligente (IDM)</span><span class="sxs-lookup"><span data-stu-id="ff562-125">Unicode string.Example: Intelligent Dance Music (IDM)</span></span><br/>                                  | <span data-ttu-id="ff562-126">Nome de exibição do subgênero.</span><span class="sxs-lookup"><span data-stu-id="ff562-126">Subgenre display name.</span></span>                                                                                                                                    |
| <span data-ttu-id="ff562-127">SubGenreSubtitle</span><span class="sxs-lookup"><span data-stu-id="ff562-127">SubGenreSubtitle</span></span>  | <span data-ttu-id="ff562-128">Não</span><span class="sxs-lookup"><span data-stu-id="ff562-128">No</span></span>       | <span data-ttu-id="ff562-129">Cadeia de caracteres Unicode. Exemplo: novo, percussive música eletrônica que não é tão puro cair.</span><span class="sxs-lookup"><span data-stu-id="ff562-129">Unicode string.Example: New, percussive electronic music that's not quite pure techno.</span></span><br/> | <span data-ttu-id="ff562-130">Descreva o significado do nome de exibição do subgênero.</span><span class="sxs-lookup"><span data-stu-id="ff562-130">Describe the meaning of the subgenre display name.</span></span> <span data-ttu-id="ff562-131">Deve ter menos de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ff562-131">Should be less than 64 characters.</span></span>                                                                     |
| <span data-ttu-id="ff562-132">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="ff562-132">FeedsAreAvailable</span></span> | <span data-ttu-id="ff562-133">Sim</span><span class="sxs-lookup"><span data-stu-id="ff562-133">Yes</span></span>      | <span data-ttu-id="ff562-134">Booliano. formato: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="ff562-134">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="ff562-135">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="ff562-135">Example: 0</span></span><br/>                                         | <span data-ttu-id="ff562-136">Indica se a "reprodução de rádio" é possível ao saltar para um feed.</span><span class="sxs-lookup"><span data-stu-id="ff562-136">Indicates whether "radio play" is possible by jumping to a feed.</span></span>                                                                                          |
| <span data-ttu-id="ff562-137">\_Gênero vinculado</span><span class="sxs-lookup"><span data-stu-id="ff562-137">Linked\_GenreID</span></span>   | <span data-ttu-id="ff562-138">Sim</span><span class="sxs-lookup"><span data-stu-id="ff562-138">Yes</span></span>      | <span data-ttu-id="ff562-139">Inteiro não negativo (Gêneroid). Exemplo: 12</span><span class="sxs-lookup"><span data-stu-id="ff562-139">Non-negative integer (GenreID).Example: 12</span></span><br/>                                             | <span data-ttu-id="ff562-140">A Gêneroid do gênero pai.</span><span class="sxs-lookup"><span data-stu-id="ff562-140">The GenreID of the parent genre.</span></span> <span data-ttu-id="ff562-141">Somente um pai é permitido.</span><span class="sxs-lookup"><span data-stu-id="ff562-141">Only one parent is allowed.</span></span>                                                                                              |
| <span data-ttu-id="ff562-142">SortOrderRank</span><span class="sxs-lookup"><span data-stu-id="ff562-142">SortOrderRank</span></span>     | <span data-ttu-id="ff562-143">Sim</span><span class="sxs-lookup"><span data-stu-id="ff562-143">Yes</span></span>      | <span data-ttu-id="ff562-144">Inteiro não negativo. Exemplo: 23</span><span class="sxs-lookup"><span data-stu-id="ff562-144">Non-negative integer.Example: 23</span></span><br/>                                                       | <span data-ttu-id="ff562-145">Uma classificação, idealmente exclusiva, usada para classificar subgêneros na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ff562-145">A ranking, ideally unique, used for sorting subgenres in the user interface.</span></span> <span data-ttu-id="ff562-146">Se o gênero pai tiver 10 subgêneros, isso poderá ser um inteiro de 1 a 10.</span><span class="sxs-lookup"><span data-stu-id="ff562-146">If the parent genre has 10 subgenres, this might be an integer from 1 to 10.</span></span> |



 

 

 





