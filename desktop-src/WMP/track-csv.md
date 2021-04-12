---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Armazenamentos online do Windows Media Player, track.csv
- lojas online, track.csv
- Digite 1 lojas online, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292354"
---
# <a name="trackcsv"></a><span data-ttu-id="921aa-107">track.csv</span><span class="sxs-lookup"><span data-stu-id="921aa-107">track.csv</span></span>

<span data-ttu-id="921aa-108">Esse arquivo contém uma entrada para cada faixa no catálogo.</span><span class="sxs-lookup"><span data-stu-id="921aa-108">This file contains an entry for each track in the catalog.</span></span> <span data-ttu-id="921aa-109">Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="921aa-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="921aa-110">Os campos devem aparecer na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="921aa-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="921aa-111">A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado.</span><span class="sxs-lookup"><span data-stu-id="921aa-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="921aa-112">Ele não se refere ao tipo de dados do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="921aa-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="921aa-113">Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.</span><span class="sxs-lookup"><span data-stu-id="921aa-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="921aa-114">Campo</span><span class="sxs-lookup"><span data-stu-id="921aa-114">Field</span></span></th>
<th><span data-ttu-id="921aa-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="921aa-115">Required</span></span></th>
<th><span data-ttu-id="921aa-116">Formatar</span><span class="sxs-lookup"><span data-stu-id="921aa-116">Format</span></span></th>
<th><span data-ttu-id="921aa-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="921aa-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="921aa-118">TrackID</span><span class="sxs-lookup"><span data-stu-id="921aa-118">TrackID</span></span></td>
<td><span data-ttu-id="921aa-119">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-119">Yes</span></span></td>
<td><span data-ttu-id="921aa-120">Inteiro não negativo. Exemplo: 32789</span><span class="sxs-lookup"><span data-stu-id="921aa-120">Non-negative integer.Example: 32789</span></span><br/></td>
<td><span data-ttu-id="921aa-121">Identificador exclusivo fornecido pelo provedor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="921aa-121">Unique identifier provided by the content provider.</span></span> <span data-ttu-id="921aa-122">Deve ser menor que 2 ^ 32. dica de desempenho: se as IDs atribuídas a faixas do mesmo álbum forem numeradas consecutivamente, a compactação do catálogo será mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="921aa-122">Must be less than 2^32.Performance tip: If the IDs assigned to tracks from the same album are numbered consecutively, catalog compression will be more efficient.</span></span> <span data-ttu-id="921aa-123">No entanto, a numeração consecutiva de faixas do álbum não é necessária.</span><span class="sxs-lookup"><span data-stu-id="921aa-123">However, consecutive numbering of album tracks is not required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="921aa-124">TrackTitle</span><span class="sxs-lookup"><span data-stu-id="921aa-124">TrackTitle</span></span></td>
<td><span data-ttu-id="921aa-125">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-125">Yes</span></span></td>
<td><span data-ttu-id="921aa-126">Cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="921aa-126">Unicode string.</span></span> <span data-ttu-id="921aa-127">Exemplo: O Raygun Robbers ' azuis</span><span class="sxs-lookup"><span data-stu-id="921aa-127">Example: Raygun Robbers' Blues</span></span></td>
<td><span data-ttu-id="921aa-128">Nome da faixa.</span><span class="sxs-lookup"><span data-stu-id="921aa-128">Name of the track.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="921aa-129">Duration</span><span class="sxs-lookup"><span data-stu-id="921aa-129">Duration</span></span></td>
<td><span data-ttu-id="921aa-130">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-130">Yes</span></span></td>
<td><span data-ttu-id="921aa-131">Inteiro não negativo. Exemplo: 543</span><span class="sxs-lookup"><span data-stu-id="921aa-131">Non-negative integer.Example: 543</span></span><br/></td>
<td><span data-ttu-id="921aa-132">Duração da faixa em segundos.</span><span class="sxs-lookup"><span data-stu-id="921aa-132">Duration of the track in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="921aa-133">TrackNumber</span><span class="sxs-lookup"><span data-stu-id="921aa-133">TrackNumber</span></span></td>
<td><span data-ttu-id="921aa-134">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-134">Yes</span></span></td>
<td><span data-ttu-id="921aa-135">Inteiro não negativo. Exemplo: 7</span><span class="sxs-lookup"><span data-stu-id="921aa-135">Non-negative integer.Example: 7</span></span><br/></td>
<td><span data-ttu-id="921aa-136">Faixa número no álbum da faixa.</span><span class="sxs-lookup"><span data-stu-id="921aa-136">Track number on the track's album.</span></span> <span data-ttu-id="921aa-137">Os números de faixa começam em 1 e aumentam em conjuntos de discos.</span><span class="sxs-lookup"><span data-stu-id="921aa-137">Track numbers begin at 1 and increase across disc sets.</span></span> <span data-ttu-id="921aa-138">O número de faixa deve ser menor que 256.</span><span class="sxs-lookup"><span data-stu-id="921aa-138">The track number must be less than 256.</span></span> <span data-ttu-id="921aa-139">Um número de faixa maior ou igual a 256 causará um comportamento inesperado no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="921aa-139">A track number greater than or equal to 256 will cause unexpected behavior in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="921aa-140">TrackPrice</span><span class="sxs-lookup"><span data-stu-id="921aa-140">TrackPrice</span></span></td>
<td><span data-ttu-id="921aa-141">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-141">Yes</span></span></td>
<td><span data-ttu-id="921aa-142">Cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="921aa-142">Unicode string.</span></span> <span data-ttu-id="921aa-143">Exemplo: $0.99.</span><span class="sxs-lookup"><span data-stu-id="921aa-143">Example: $0.99.</span></span></td>
<td><span data-ttu-id="921aa-144">Preço de acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="921aa-144">Track price.</span></span> <span data-ttu-id="921aa-145">O símbolo de moeda deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="921aa-145">The currency symbol should be included.</span></span> <span data-ttu-id="921aa-146">A cadeia de caracteres vazia, 0 e-ter significado especial.</span><span class="sxs-lookup"><span data-stu-id="921aa-146">The empty string, 0, and - have special meaning.</span></span> <span data-ttu-id="921aa-147">Uma cadeia de caracteres vazia indica que o preço é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="921aa-147">An empty string indicates that the price is unknown.</span></span> <span data-ttu-id="921aa-148">Um zero neste campo significa que a faixa é gratuita e um hífen (-) indica que a faixa não pode ser comprada.</span><span class="sxs-lookup"><span data-stu-id="921aa-148">A zero in this field means the track is free, and a hyphen (-) indicates that the track cannot be bought.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="921aa-149">Canstream</span><span class="sxs-lookup"><span data-stu-id="921aa-149">CanStream</span></span></td>
<td><span data-ttu-id="921aa-150">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-150">Yes</span></span></td>
<td><span data-ttu-id="921aa-151">Booliano.</span><span class="sxs-lookup"><span data-stu-id="921aa-151">Boolean.</span></span> <span data-ttu-id="921aa-152">Pode ser 0 ou 1. exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="921aa-152">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="921aa-153">Indica se a faixa pode ser transmitida.</span><span class="sxs-lookup"><span data-stu-id="921aa-153">Indicates whether the track can be streamed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="921aa-154">Canbaixado</span><span class="sxs-lookup"><span data-stu-id="921aa-154">CanDownload</span></span></td>
<td><span data-ttu-id="921aa-155">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-155">Yes</span></span></td>
<td><span data-ttu-id="921aa-156">Booliano.</span><span class="sxs-lookup"><span data-stu-id="921aa-156">Boolean.</span></span> <span data-ttu-id="921aa-157">Pode ser 0 ou 1. exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="921aa-157">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="921aa-158">Indica se a faixa pode ser baixada.</span><span class="sxs-lookup"><span data-stu-id="921aa-158">Indicates whether the track can be downloaded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="921aa-159">HasPreviewClip</span><span class="sxs-lookup"><span data-stu-id="921aa-159">HasPreviewClip</span></span></td>
<td><span data-ttu-id="921aa-160">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-160">Yes</span></span></td>
<td><span data-ttu-id="921aa-161">Booliano.</span><span class="sxs-lookup"><span data-stu-id="921aa-161">Boolean.</span></span> <span data-ttu-id="921aa-162">Pode ser 0 ou 1. exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="921aa-162">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="921aa-163">Indica se a faixa tem um clipe de visualização.</span><span class="sxs-lookup"><span data-stu-id="921aa-163">Indicates whether the track has a preview clip.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="921aa-164">HasVideoClip</span><span class="sxs-lookup"><span data-stu-id="921aa-164">HasVideoClip</span></span></td>
<td><span data-ttu-id="921aa-165">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-165">Yes</span></span></td>
<td><span data-ttu-id="921aa-166">Booliano.</span><span class="sxs-lookup"><span data-stu-id="921aa-166">Boolean.</span></span> <span data-ttu-id="921aa-167">Pode ser 0 ou 1. exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="921aa-167">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="921aa-168">Indica se a faixa tem um clipe de vídeo.</span><span class="sxs-lookup"><span data-stu-id="921aa-168">Indicates whether the track has a video clip.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="921aa-169">ParentalRating</span><span class="sxs-lookup"><span data-stu-id="921aa-169">ParentalRating</span></span></td>
<td><span data-ttu-id="921aa-170">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-170">Yes</span></span></td>
<td><span data-ttu-id="921aa-171">Enumeração.</span><span class="sxs-lookup"><span data-stu-id="921aa-171">Enumeration.</span></span> <span data-ttu-id="921aa-172">Pode ser N, E ou C. exemplo: N</span><span class="sxs-lookup"><span data-stu-id="921aa-172">Can be N, E, or C.Example: N</span></span><br/></td>
<td><span data-ttu-id="921aa-173">Indica a classificação de consultoria do responsável.</span><span class="sxs-lookup"><span data-stu-id="921aa-173">Indicates the Parental Advisory Rating.</span></span> <span data-ttu-id="921aa-174">Os valores N, E e C são para normal, explícita e limpa.</span><span class="sxs-lookup"><span data-stu-id="921aa-174">The values N, E, and C stand for Normal, Explicit, and Clean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="921aa-175">LinkedAlbumID</span><span class="sxs-lookup"><span data-stu-id="921aa-175">LinkedAlbumID</span></span></td>
<td><span data-ttu-id="921aa-176">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-176">Yes</span></span></td>
<td><span data-ttu-id="921aa-177">Inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="921aa-177">Non-negative integer.</span></span> <span data-ttu-id="921aa-178">Deve ser a ID de um álbum.</span><span class="sxs-lookup"><span data-stu-id="921aa-178">Must be the ID of an Album.</span></span> <span data-ttu-id="921aa-179">Exemplo: 32423</span><span class="sxs-lookup"><span data-stu-id="921aa-179">Example: 32423</span></span></td>
<td><span data-ttu-id="921aa-180">A ID do álbum que contém essa faixa.</span><span class="sxs-lookup"><span data-stu-id="921aa-180">The ID of the album that contains this track.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="921aa-181">Cada faixa deve pertencer a um álbum.</span><span class="sxs-lookup"><span data-stu-id="921aa-181">Every track must belong to an album.</span></span> <span data-ttu-id="921aa-182">Ou seja, para cada faixa, o campo LinkedAlbumID deve ser igual a uma das IDs do álbum no arquivo album.csv.</span><span class="sxs-lookup"><span data-stu-id="921aa-182">That is, for each track, the LinkedAlbumID field must be equal to one of the album IDs in the album.csv file.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="921aa-183">LinkedTrackArtist_ArtistIDs</span><span class="sxs-lookup"><span data-stu-id="921aa-183">LinkedTrackArtist_ArtistIDs</span></span></td>
<td><span data-ttu-id="921aa-184">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-184">Yes</span></span></td>
<td><span data-ttu-id="921aa-185">Lista de inteiros.</span><span class="sxs-lookup"><span data-stu-id="921aa-185">List of integers.</span></span> <span data-ttu-id="921aa-186">A lista contém IDs de artista, separadas por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="921aa-186">The list contains artist IDs, separated by semicolons.</span></span> <span data-ttu-id="921aa-187">Exemplo: 41322; 12321; 82123;</span><span class="sxs-lookup"><span data-stu-id="921aa-187">Example: 41322;12321; 82123;</span></span></td>
<td><span data-ttu-id="921aa-188">Uma lista de IDs correspondentes aos artistas colaboradores.</span><span class="sxs-lookup"><span data-stu-id="921aa-188">A list of IDs corresponding to the contributing artists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="921aa-189">Compositor</span><span class="sxs-lookup"><span data-stu-id="921aa-189">Composer</span></span></td>
<td><span data-ttu-id="921aa-190">Não</span><span class="sxs-lookup"><span data-stu-id="921aa-190">No</span></span></td>
<td><span data-ttu-id="921aa-191">Cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="921aa-191">Unicode string.</span></span> <span data-ttu-id="921aa-192">Exemplo: Sinfonia</span><span class="sxs-lookup"><span data-stu-id="921aa-192">Example: Beethoven</span></span></td>
<td><span data-ttu-id="921aa-193">O compositor da faixa. Se o gênero da faixa não tiver o campo HasComposer definido, o valor do campo do compositor será ignorado.</span><span class="sxs-lookup"><span data-stu-id="921aa-193">The composer of the track. If the track's genre does not have the HasComposer field set, the value of the Composer field will be ignored.</span></span> <span data-ttu-id="921aa-194">Normalmente usado apenas para faixas de jazz ou clássicas.</span><span class="sxs-lookup"><span data-stu-id="921aa-194">Typically used only for jazz or classical tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="921aa-195">Popularidade</span><span class="sxs-lookup"><span data-stu-id="921aa-195">Popularity</span></span></td>
<td><span data-ttu-id="921aa-196">Sim</span><span class="sxs-lookup"><span data-stu-id="921aa-196">Yes</span></span></td>
<td><span data-ttu-id="921aa-197">Inteiro ou float não negativo. exemplo: 1252,6</span><span class="sxs-lookup"><span data-stu-id="921aa-197">Non-negative integer or Float.Example: 1252.6</span></span><br/></td>
<td><span data-ttu-id="921aa-198">Determina a posição da faixa na lista quando classificada por popularidade.</span><span class="sxs-lookup"><span data-stu-id="921aa-198">Determines the position of the track in the list when sorted by popularity.</span></span> <span data-ttu-id="921aa-199">Um número mais baixo indica maior popularidade.</span><span class="sxs-lookup"><span data-stu-id="921aa-199">A lower number indicates higher popularity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="921aa-200">StarRating</span><span class="sxs-lookup"><span data-stu-id="921aa-200">StarRating</span></span></td>
<td><span data-ttu-id="921aa-201">Não</span><span class="sxs-lookup"><span data-stu-id="921aa-201">No</span></span></td>
<td><span data-ttu-id="921aa-202">Float. example: 4,21</span><span class="sxs-lookup"><span data-stu-id="921aa-202">Float.Example: 4.21</span></span><br/></td>
<td><span data-ttu-id="921aa-203">A classificação por estrelas será arredondada para a estrela de 1/4 a mais próxima do Windows Media Player antes de ser exibida na interface de usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="921aa-203">The star rating will be rounded to the nearest 1/4 star by Windows Media Player before being displayed in the Windows Media Player user interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 





