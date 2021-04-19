---
title: LISTA de reprodução. colunas
description: O atributo Columns define as colunas que aparecem no elemento PLAYLIST.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- PLAYLIST. Columns Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764149"
---
# <a name="playlistcolumns"></a><span data-ttu-id="cf488-104">LISTA de reprodução. colunas</span><span class="sxs-lookup"><span data-stu-id="cf488-104">PLAYLIST.columns</span></span>

<span data-ttu-id="cf488-105">O atributo **Columns** define as colunas que aparecem no elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="cf488-105">The **columns** attribute defines the columns that appear in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.columns
```

## <a name="possible-values"></a><span data-ttu-id="cf488-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="cf488-106">Possible Values</span></span>

<span data-ttu-id="cf488-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="cf488-107">This attribute is a read/write **String** in the following format:</span></span>

<span data-ttu-id="cf488-108">nome do banco de BD \_ = \_ nome amigável; nome do banco de BD \_ = \_ nome amigável;</span><span class="sxs-lookup"><span data-stu-id="cf488-108">DB\_NAME=FRIENDLY\_NAME;DB\_NAME=FRIENDLY\_NAME;</span></span>

<span data-ttu-id="cf488-109">\_Nome amigável é o valor mostrado no cabeçalho da coluna do elemento playlist e \_ nome do BD é um valor da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf488-109">FRIENDLY\_NAME is the value shown in the column header of the PLAYLIST element, and DB\_NAME is a value from the following table.</span></span> <span data-ttu-id="cf488-110">Observe que um item de playlist pode ser um item de mídia da biblioteca ou de um CD, ou pode ser outra **playlist** que seja criada pelo usuário ou extraída de um CD.</span><span class="sxs-lookup"><span data-stu-id="cf488-110">Note that a Playlist item might be a media item from the library or from a CD, or it might be another **Playlist** that is either user-created or taken from a CD.</span></span> <span data-ttu-id="cf488-111">Algumas colunas são válidas somente com determinados itens da lista de reprodução, conforme indicado na coluna Descrição.</span><span class="sxs-lookup"><span data-stu-id="cf488-111">Some columns are valid only with certain Playlist items as indicated in the Description column.</span></span>



| <span data-ttu-id="cf488-112">Valor</span><span class="sxs-lookup"><span data-stu-id="cf488-112">Value</span></span>             | <span data-ttu-id="cf488-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf488-113">Description</span></span>                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf488-114">Álbuns</span><span class="sxs-lookup"><span data-stu-id="cf488-114">Album</span></span>             | <span data-ttu-id="cf488-115">O nome do álbum.</span><span class="sxs-lookup"><span data-stu-id="cf488-115">The name of the album.</span></span> <span data-ttu-id="cf488-116">Usado somente com itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="cf488-116">Used with media items only.</span></span>                                                                      |
| <span data-ttu-id="cf488-117">Autor</span><span class="sxs-lookup"><span data-stu-id="cf488-117">Artist</span></span>            | <span data-ttu-id="cf488-118">O nome do artista.</span><span class="sxs-lookup"><span data-stu-id="cf488-118">The name of the artist.</span></span> <span data-ttu-id="cf488-119">Não usado com listas de reprodução criadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="cf488-119">Not used with user-created playlists.</span></span>                                                           |
| <span data-ttu-id="cf488-120">Autor</span><span class="sxs-lookup"><span data-stu-id="cf488-120">Author</span></span>            | <span data-ttu-id="cf488-121">O nome do artista.</span><span class="sxs-lookup"><span data-stu-id="cf488-121">The name of the artist.</span></span>                                                                                                 |
| <span data-ttu-id="cf488-122">Bitrate</span><span class="sxs-lookup"><span data-stu-id="cf488-122">Bitrate</span></span>           | <span data-ttu-id="cf488-123">A taxa de bits do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cf488-123">The bit rate of the content.</span></span> <span data-ttu-id="cf488-124">Usado somente com itens de mídia da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cf488-124">Used only with media items from the library.</span></span>                                               |
| <span data-ttu-id="cf488-125">CDTrackEnabled</span><span class="sxs-lookup"><span data-stu-id="cf488-125">CDTrackEnabled</span></span>    | <span data-ttu-id="cf488-126">Indica se a faixa do CD está habilitada.</span><span class="sxs-lookup"><span data-stu-id="cf488-126">Indicates whether the CD track is enabled.</span></span> <span data-ttu-id="cf488-127">Usado somente com itens de mídia de CD.</span><span class="sxs-lookup"><span data-stu-id="cf488-127">Used only with CD media items.</span></span>                                               |
| <span data-ttu-id="cf488-128">Verificado</span><span class="sxs-lookup"><span data-stu-id="cf488-128">Checked</span></span>           | <span data-ttu-id="cf488-129">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf488-129">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="cf488-130">Direitos autorais</span><span class="sxs-lookup"><span data-stu-id="cf488-130">Copyright</span></span>         | <span data-ttu-id="cf488-131">Os direitos autorais da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="cf488-131">The copyright of the playlist.</span></span> <span data-ttu-id="cf488-132">Não usado com playlists de CD ou itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="cf488-132">Not used with CD playlists or media items.</span></span>                                               |
| <span data-ttu-id="cf488-133">CreationDate</span><span class="sxs-lookup"><span data-stu-id="cf488-133">CreationDate</span></span>      | <span data-ttu-id="cf488-134">A data e a hora em que a entrada na biblioteca foi criada.</span><span class="sxs-lookup"><span data-stu-id="cf488-134">The date and time that the entry in the library was created.</span></span> <span data-ttu-id="cf488-135">Usado somente com itens da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cf488-135">Used only with items from the library.</span></span>                     |
| <span data-ttu-id="cf488-136">DigitallySecure</span><span class="sxs-lookup"><span data-stu-id="cf488-136">DigitallySecure</span></span>   | <span data-ttu-id="cf488-137">Indica se o item está protegido com o Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="cf488-137">Indicates whether the item is protected with Windows Media Rights Manager.</span></span> <span data-ttu-id="cf488-138">Usado somente com itens de mídia da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cf488-138">Used only with media items from the library.</span></span> |
| <span data-ttu-id="cf488-139">Duration</span><span class="sxs-lookup"><span data-stu-id="cf488-139">Duration</span></span>          | <span data-ttu-id="cf488-140">A duração do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="cf488-140">The duration of the media item.</span></span>                                                                                         |
| <span data-ttu-id="cf488-141">FileType</span><span class="sxs-lookup"><span data-stu-id="cf488-141">FileType</span></span>          | <span data-ttu-id="cf488-142">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf488-142">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="cf488-143">Gênero</span><span class="sxs-lookup"><span data-stu-id="cf488-143">Genre</span></span>             | <span data-ttu-id="cf488-144">O gênero da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="cf488-144">The genre of the playlist.</span></span> <span data-ttu-id="cf488-145">Não usado com listas de reprodução de CDs.</span><span class="sxs-lookup"><span data-stu-id="cf488-145">Not used with playlists from CDs.</span></span>                                                            |
| <span data-ttu-id="cf488-146">Mediaattribute</span><span class="sxs-lookup"><span data-stu-id="cf488-146">MediaAttribute</span></span>    | <span data-ttu-id="cf488-147">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf488-147">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="cf488-148">MediaType</span><span class="sxs-lookup"><span data-stu-id="cf488-148">MediaType</span></span>         | <span data-ttu-id="cf488-149">O tipo do item de mídia (áudio ou vídeo).</span><span class="sxs-lookup"><span data-stu-id="cf488-149">The type of the media item (audio or video).</span></span>                                                                            |
| <span data-ttu-id="cf488-150">Metadataização</span><span class="sxs-lookup"><span data-stu-id="cf488-150">MetadataSource</span></span>    | <span data-ttu-id="cf488-151">A origem dos metadados para esta faixa de CD (AMG, WindowsMedia.com e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="cf488-151">The source of the metadata for this CD track (AMG, WindowsMedia.com, and so on).</span></span> <span data-ttu-id="cf488-152">Usado somente com itens de mídia de CD.</span><span class="sxs-lookup"><span data-stu-id="cf488-152">Used only with CD media items.</span></span>         |
| <span data-ttu-id="cf488-153">ModifiedBy</span><span class="sxs-lookup"><span data-stu-id="cf488-153">ModifiedBy</span></span>        | <span data-ttu-id="cf488-154">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf488-154">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="cf488-155">Nome</span><span class="sxs-lookup"><span data-stu-id="cf488-155">Name</span></span>              | <span data-ttu-id="cf488-156">O nome da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="cf488-156">The name of the playlist.</span></span>                                                                                               |
| <span data-ttu-id="cf488-157">OriginalIndex</span><span class="sxs-lookup"><span data-stu-id="cf488-157">OriginalIndex</span></span>     | <span data-ttu-id="cf488-158">Se aplicável, o identificador de faixa do CD correspondente.</span><span class="sxs-lookup"><span data-stu-id="cf488-158">If applicable, the corresponding CD track identifier.</span></span> <span data-ttu-id="cf488-159">Usado somente com itens de mídia de CD.</span><span class="sxs-lookup"><span data-stu-id="cf488-159">Used only with CD media items.</span></span>                                    |
| <span data-ttu-id="cf488-160">PlayCount</span><span class="sxs-lookup"><span data-stu-id="cf488-160">PlayCount</span></span>         | <span data-ttu-id="cf488-161">O número de vezes que o conteúdo foi reproduzido até o fim.</span><span class="sxs-lookup"><span data-stu-id="cf488-161">The number of times the content has been played through to the end.</span></span> <span data-ttu-id="cf488-162">Usado somente com itens de mídia da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cf488-162">Used only with media items from the library.</span></span>        |
| <span data-ttu-id="cf488-163">Playlistattribute</span><span class="sxs-lookup"><span data-stu-id="cf488-163">PlaylistAttribute</span></span> | <span data-ttu-id="cf488-164">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf488-164">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="cf488-165">Classificação</span><span class="sxs-lookup"><span data-stu-id="cf488-165">Rating</span></span>            | <span data-ttu-id="cf488-166">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf488-166">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="cf488-167">SourceURL</span><span class="sxs-lookup"><span data-stu-id="cf488-167">SourceURL</span></span>         | <span data-ttu-id="cf488-168">O caminho ou a URL para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cf488-168">The path or URL to the content.</span></span> <span data-ttu-id="cf488-169">Usado somente com itens de mídia da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cf488-169">Used only with media items from the library.</span></span>                                            |
| <span data-ttu-id="cf488-170">Status</span><span class="sxs-lookup"><span data-stu-id="cf488-170">Status</span></span>            | <span data-ttu-id="cf488-171">O status de cópia de uma faixa de CD que está sendo copiada.</span><span class="sxs-lookup"><span data-stu-id="cf488-171">The copying status of a CD track being copied.</span></span> <span data-ttu-id="cf488-172">Usado somente com itens de mídia de CD.</span><span class="sxs-lookup"><span data-stu-id="cf488-172">Used only with CD media items.</span></span>                                           |
| <span data-ttu-id="cf488-173">Estilo</span><span class="sxs-lookup"><span data-stu-id="cf488-173">Style</span></span>             | <span data-ttu-id="cf488-174">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf488-174">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="cf488-175">SUMÁRIO</span><span class="sxs-lookup"><span data-stu-id="cf488-175">TOC</span></span>               | <span data-ttu-id="cf488-176">Se aplicável, o identificador de Sumário do CD correspondente.</span><span class="sxs-lookup"><span data-stu-id="cf488-176">If applicable, the corresponding CD Table of Contents Identifier.</span></span> <span data-ttu-id="cf488-177">Não usado com listas de reprodução criadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="cf488-177">Not used with user-created playlists.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="cf488-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf488-178">Remarks</span></span>

<span data-ttu-id="cf488-179">Se uma das colunas não existir na biblioteca, ela será deixada em branco.</span><span class="sxs-lookup"><span data-stu-id="cf488-179">If one of the columns does not exist in the library, it is left blank.</span></span>

<span data-ttu-id="cf488-180">Um máximo de 31 colunas pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="cf488-180">A maximum of 31 columns may be specified.</span></span>

<span data-ttu-id="cf488-181">Se você especificar uma coluna duplicada, os dados na primeira coluna serão alinhados à esquerda, mas todas as outras colunas duplicadas serão alinhadas à direita.</span><span class="sxs-lookup"><span data-stu-id="cf488-181">If you specify a duplicate column, the data in the first column will be left-aligned but all other duplicate columns will be right-aligned.</span></span> <span data-ttu-id="cf488-182">Por exemplo, se você tiver duas colunas Duration, os dados serão alinhados à esquerda no primeiro e alinhado à direita no segundo.</span><span class="sxs-lookup"><span data-stu-id="cf488-182">For example, if you have two duration columns, the data will be left-aligned in the first and right-aligned in the second.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf488-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf488-183">Requirements</span></span>



| <span data-ttu-id="cf488-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf488-184">Requirement</span></span> | <span data-ttu-id="cf488-185">Valor</span><span class="sxs-lookup"><span data-stu-id="cf488-185">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cf488-186">Versão</span><span class="sxs-lookup"><span data-stu-id="cf488-186">Version</span></span><br/> | <span data-ttu-id="cf488-187">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cf488-187">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf488-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf488-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf488-189">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="cf488-189">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="cf488-190">**PLAYLIST. columnsVisible**</span><span class="sxs-lookup"><span data-stu-id="cf488-190">**PLAYLIST.columnsVisible**</span></span>](playlist-columnsvisible.md)
</dt> </dl>

 

 





