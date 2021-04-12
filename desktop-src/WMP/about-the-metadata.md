---
title: Sobre os metadados
description: Sobre os metadados
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Windows Media Player, metadados
- metadados, sobre
- metadados, atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291819"
---
# <a name="about-the-metadata"></a><span data-ttu-id="ff25c-106">Sobre os metadados</span><span class="sxs-lookup"><span data-stu-id="ff25c-106">About the Metadata</span></span>

<span data-ttu-id="ff25c-107">O Windows Media Player 10 ou posterior tenta sincronizar os seguintes atributos de metadados.</span><span class="sxs-lookup"><span data-stu-id="ff25c-107">Windows Media Player 10 or later attempts to synchronize the following metadata attributes.</span></span>



| <span data-ttu-id="ff25c-108">Atributo do Player</span><span class="sxs-lookup"><span data-stu-id="ff25c-108">Player attribute</span></span> | <span data-ttu-id="ff25c-109">Constante global WMDM</span><span class="sxs-lookup"><span data-stu-id="ff25c-109">WMDM global constant</span></span>  | <span data-ttu-id="ff25c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff25c-110">Description</span></span>                                                                                                 | <span data-ttu-id="ff25c-111">Versão necessária</span><span class="sxs-lookup"><span data-stu-id="ff25c-111">Required version</span></span>                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="ff25c-112">AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="ff25c-112">AlbumArtist</span></span>      | <span data-ttu-id="ff25c-113">g \_ wszWMDMAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="ff25c-113">g\_wszWMDMAlbumArtist</span></span> | <span data-ttu-id="ff25c-114">**Cadeia de caracteres** terminada em nulo que contém o nome do artista principal para o álbum.</span><span class="sxs-lookup"><span data-stu-id="ff25c-114">Null-terminated **string** containing the name of the primary artist for the album.</span></span>                         | <span data-ttu-id="ff25c-115">Windows Media Player 11 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-115">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="ff25c-116">Álbuns</span><span class="sxs-lookup"><span data-stu-id="ff25c-116">Album</span></span>            | <span data-ttu-id="ff25c-117">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="ff25c-117">g\_wszWMDMAlbumTitle</span></span>  | <span data-ttu-id="ff25c-118">**Cadeia de caracteres** terminada em nulo que contém o título do álbum no qual o conteúdo foi originalmente lançado.</span><span class="sxs-lookup"><span data-stu-id="ff25c-118">Null-terminated **string** containing the title of the album on which the content was originally released.</span></span>  | <span data-ttu-id="ff25c-119">Windows Media Player 11 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-119">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="ff25c-120">Autor</span><span class="sxs-lookup"><span data-stu-id="ff25c-120">Author</span></span>           | <span data-ttu-id="ff25c-121">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="ff25c-121">g\_wszWMDMAuthor</span></span>      | <span data-ttu-id="ff25c-122">**Cadeia de caracteres** terminada em nulo que contém o nome do artista de mídia ou ator associado ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ff25c-122">Null-terminated **string** containing the name of the media artist or actor associated with the content.</span></span>    | <span data-ttu-id="ff25c-123">Windows Media Player 11 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-123">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="ff25c-124">BuyNow</span><span class="sxs-lookup"><span data-stu-id="ff25c-124">BuyNow</span></span>           | <span data-ttu-id="ff25c-125">g \_ wszWMDMBuyNow</span><span class="sxs-lookup"><span data-stu-id="ff25c-125">g\_wszWMDMBuyNow</span></span>      | <span data-ttu-id="ff25c-126">**Booliano** que indica se o usuário optou por comprar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ff25c-126">**Boolean** indicating whether the user has chosen to purchase the content.</span></span>                                 | <span data-ttu-id="ff25c-127">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-127">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="ff25c-128">WM/gênero</span><span class="sxs-lookup"><span data-stu-id="ff25c-128">WM/Genre</span></span>         | <span data-ttu-id="ff25c-129">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="ff25c-129">g\_wszWMDMGenre</span></span>       | <span data-ttu-id="ff25c-130">**Cadeia de caracteres** terminada em nulo que contém o gênero do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ff25c-130">Null-terminated **string** containing the genre of the content.</span></span>                                             | <span data-ttu-id="ff25c-131">Windows Media Player 11 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-131">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="ff25c-132">UserPlayCount</span><span class="sxs-lookup"><span data-stu-id="ff25c-132">UserPlayCount</span></span>    | <span data-ttu-id="ff25c-133">g \_ wszWMDMPlayCount</span><span class="sxs-lookup"><span data-stu-id="ff25c-133">g\_wszWMDMPlayCount</span></span>   | <span data-ttu-id="ff25c-134">**DWORD** que contém o número de vezes que o usuário reproduziu o arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="ff25c-134">**DWORD** containing the number of times the user has played the digital media file.</span></span>                        | <span data-ttu-id="ff25c-135">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-135">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="ff25c-136">Liberado</span><span class="sxs-lookup"><span data-stu-id="ff25c-136">ReleaseDate</span></span>      | <span data-ttu-id="ff25c-137">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="ff25c-137">g\_wszWMDMYear</span></span>        | <span data-ttu-id="ff25c-138">A data da versão original do item.</span><span class="sxs-lookup"><span data-stu-id="ff25c-138">The date of the original release of the item.</span></span>                                                               | <span data-ttu-id="ff25c-139">Windows Media Player 11 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-139">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="ff25c-140">Título</span><span class="sxs-lookup"><span data-stu-id="ff25c-140">Title</span></span>            | <span data-ttu-id="ff25c-141">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="ff25c-141">g\_wszWMDMTitle</span></span>       | <span data-ttu-id="ff25c-142">**Cadeia de caracteres** terminada em nulo que contém o título.</span><span class="sxs-lookup"><span data-stu-id="ff25c-142">Null-terminated **string** containing the title.</span></span>                                                            | <span data-ttu-id="ff25c-143">Windows Media Player 11 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-143">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="ff25c-144">WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="ff25c-144">WM/TrackNumber</span></span>   | <span data-ttu-id="ff25c-145">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="ff25c-145">g\_wszWMDMTrack</span></span>       | <span data-ttu-id="ff25c-146">**DWORD** que contém o número de faixa do item no álbum no qual ele foi originalmente lançado.</span><span class="sxs-lookup"><span data-stu-id="ff25c-146">**DWORD** containing the track number of the item on the album on which it was originally released.</span></span>         | <span data-ttu-id="ff25c-147">Windows Media Player 11 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-147">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="ff25c-148">UserRating</span><span class="sxs-lookup"><span data-stu-id="ff25c-148">UserRating</span></span>       | <span data-ttu-id="ff25c-149">g \_ wszWMDMUserRating</span><span class="sxs-lookup"><span data-stu-id="ff25c-149">g\_wszWMDMUserRating</span></span>  | <span data-ttu-id="ff25c-150">**DWORD** que contém um valor que representa a classificação em estrela que o usuário especificou para o arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="ff25c-150">**DWORD** containing a value that represents the star rating the user specified for the digital media file.</span></span> | <span data-ttu-id="ff25c-151">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff25c-151">Windows Media Player 10 or later.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ff25c-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff25c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff25c-153">**Extensões de dispositivo para transferência de metadados acelerada**</span><span class="sxs-lookup"><span data-stu-id="ff25c-153">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




