---
title: Convenção de trabalho BITS do Windows Media Player
description: O Windows Media Player pode baixar e adicionar automaticamente itens de mídia digital à biblioteca se você usar Serviço de Transferência Inteligente em Segundo Plano (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Armazenamentos online do Windows Media Player, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- lojas online, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- tipo 2 lojas online, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- BITS
- BITS (Serviço de Transferência Inteligente em Segundo Plano)
- Lojas online do Windows Media Player, Convenção de trabalho BITS
- lojas online, Convenção de trabalho BITS
- tipo 2 lojas online, Convenção de trabalho BITS
- Convenção de trabalho BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162375"
---
# <a name="windows-media-player-bits-job-convention"></a><span data-ttu-id="832dc-112">Convenção de trabalho BITS do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="832dc-112">Windows Media Player BITS Job Convention</span></span>

<span data-ttu-id="832dc-113">O Windows Media Player pode baixar e adicionar automaticamente itens de mídia digital à biblioteca se você usar [serviço de transferência inteligente em segundo plano (bits)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span><span class="sxs-lookup"><span data-stu-id="832dc-113">Windows Media Player can automatically download and add digital media items to the library if you use [Background Intelligent Transfer Service (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span></span> <span data-ttu-id="832dc-114">Para aproveitar esse recurso, você deve adicionar seu trabalho à fila de transferência de BITS e chamar **método ibackgroundcopyjob:: SetDescription**, fornecendo uma cadeia de caracteres de descrição que usa o formato correto.</span><span class="sxs-lookup"><span data-stu-id="832dc-114">To take advantage of this feature, you must add your job to the BITS transfer queue and call **IBackgroundCopyJob::SetDescription**, providing a description string that uses the correct format.</span></span>

> [!Note]  
> <span data-ttu-id="832dc-115">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="832dc-115">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="832dc-116">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="832dc-116">Use of this functionality outside the context of an online store is not supported.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="832dc-117">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="832dc-117">Syntax</span></span>

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a><span data-ttu-id="832dc-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="832dc-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="832dc-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span><span class="sxs-lookup"><span data-stu-id="832dc-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span></span>
</dt> <dd>

<span data-ttu-id="832dc-120">Um valor de 32 bits gerado aleatoriamente que o Windows Media Player usa para identificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="832dc-120">A randomly generated 32-bit value that Windows Media Player uses to identify the service.</span></span>

</dd> <dt>

<span data-ttu-id="832dc-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Operador*</span><span class="sxs-lookup"><span data-stu-id="832dc-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Provider*</span></span>
</dt> <dd>

<span data-ttu-id="832dc-122">O nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="832dc-122">The provider name.</span></span> <span data-ttu-id="832dc-123">Esse valor deve corresponder a um nome de chave de loja online válido.</span><span class="sxs-lookup"><span data-stu-id="832dc-123">This value must match a valid online store key name.</span></span>

</dd> <dt>

<span data-ttu-id="832dc-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span><span class="sxs-lookup"><span data-stu-id="832dc-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span></span>
</dt> <dd>

<span data-ttu-id="832dc-125">O nome do artista principal para o álbum.</span><span class="sxs-lookup"><span data-stu-id="832dc-125">The name of the primary artist for the album.</span></span>

</dd> <dt>

<span data-ttu-id="832dc-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*Campos AlbumTitle*</span><span class="sxs-lookup"><span data-stu-id="832dc-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span></span>
</dt> <dd>

<span data-ttu-id="832dc-127">O título do álbum.</span><span class="sxs-lookup"><span data-stu-id="832dc-127">The title of the album.</span></span>

</dd> <dt>

<span data-ttu-id="832dc-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span><span class="sxs-lookup"><span data-stu-id="832dc-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span></span>
</dt> <dd>

<span data-ttu-id="832dc-129">O número de faixas do CD.</span><span class="sxs-lookup"><span data-stu-id="832dc-129">The CD track number.</span></span>

</dd> <dt>

<span data-ttu-id="832dc-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Título*</span><span class="sxs-lookup"><span data-stu-id="832dc-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Title*</span></span>
</dt> <dd>

<span data-ttu-id="832dc-131">O título do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="832dc-131">The title of the content.</span></span>

</dd> <dt>

<span data-ttu-id="832dc-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Permanência*</span><span class="sxs-lookup"><span data-stu-id="832dc-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duration*</span></span>
</dt> <dd>

<span data-ttu-id="832dc-133">A duração do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="832dc-133">The duration of the content.</span></span>

</dd> <dt>

<span data-ttu-id="832dc-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Avaliações*</span><span class="sxs-lookup"><span data-stu-id="832dc-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Rating*</span></span>
</dt> <dd>

<span data-ttu-id="832dc-135">A classificação do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="832dc-135">The rating for the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="832dc-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="832dc-136">Remarks</span></span>

<span data-ttu-id="832dc-137">Quando o Windows Media Player 10 ou posterior usa BITS para baixar conteúdo, ele enumera os trabalhos na fila de transferência e inspeciona a cadeia de caracteres de descrição para cada trabalho.</span><span class="sxs-lookup"><span data-stu-id="832dc-137">When Windows Media Player 10 or later uses BITS to download content, it enumerates the jobs in the transfer queue and inspects the description string for each job.</span></span> <span data-ttu-id="832dc-138">Se a cadeia de caracteres de descrição corresponder à Convenção esperada, o Windows Media Player baixará o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="832dc-138">If the description string matches the expected convention, Windows Media Player downloads the content.</span></span>

<span data-ttu-id="832dc-139">Você deve adicionar apenas um arquivo de mídia digital para download em cada trabalho do BITS.</span><span class="sxs-lookup"><span data-stu-id="832dc-139">You must add only one digital media file for download to each BITS job.</span></span>

<span data-ttu-id="832dc-140">Depois de iniciar um trabalho do BITS usando essa convenção, você deve permitir que o Windows Media Player conclua o trabalho.</span><span class="sxs-lookup"><span data-stu-id="832dc-140">After you start a BITS job using this convention, you must let Windows Media Player complete the job.</span></span> <span data-ttu-id="832dc-141">O Windows Media Player também removerá o trabalho da fila BITS, moverá o arquivo baixado para o local em que a música copiada é salva e adicionará o arquivo baixado à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="832dc-141">Windows Media Player will also remove the job from the BITS queue, move the downloaded file to the location where ripped music is saved, and add the downloaded file to the library.</span></span>

<span data-ttu-id="832dc-142">O parâmetro *ServiceId* deve conter um valor de 32 bits diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="832dc-142">The *serviceId* parameter must contain a nonzero 32-bit value.</span></span> <span data-ttu-id="832dc-143">Recomendamos que você use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para criar esse valor.</span><span class="sxs-lookup"><span data-stu-id="832dc-143">We recommend that you use the function [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) to create this value.</span></span>

<span data-ttu-id="832dc-144">O nome de arquivo que você especifica usando o parâmetro *LocalName* de **método ibackgroundcopyjob:: AddFile** deve ter uma extensão de nome de arquivo. WMA,. wmv,. mp3 ou. ASF.</span><span class="sxs-lookup"><span data-stu-id="832dc-144">The file name you specify using the *localName* parameter of **IBackgroundCopyJob::AddFile** must have a .wma, .wmv, .mp3, or .asf file name extension.</span></span>

<span data-ttu-id="832dc-145">Os parâmetros restantes são projetados para conter valores de metadados relacionados ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="832dc-145">The remaining parameters are designed to contain metadata values related to the content.</span></span> <span data-ttu-id="832dc-146">Você pode recuperar esses valores da página da Web da loja online usando **DownloadItem. getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="832dc-146">You can retrieve these values from your online store webpage by using **DownloadItem.getItemInfo**.</span></span> <span data-ttu-id="832dc-147">Você pode recuperar a coleção de download correta chamando **DownloadManager. Getbaixecollection** e fornecendo *ServiceId* como o parâmetro *CollectionId* .</span><span class="sxs-lookup"><span data-stu-id="832dc-147">You can retrieve the correct download collection by calling **DownloadManager.getDownloadCollection** and providing *serviceId* as the *collectionId* parameter.</span></span>

<span data-ttu-id="832dc-148">O Windows Media Player inspeciona a fila BITS periodicamente enquanto o player está em execução.</span><span class="sxs-lookup"><span data-stu-id="832dc-148">Windows Media Player inspects the BITS queue periodically while the Player is running.</span></span> <span data-ttu-id="832dc-149">Para garantir que o Windows Media Player Verifique a fila BITS para trabalhos de download, você deve criar um valor na seguinte subchave do registro:</span><span class="sxs-lookup"><span data-stu-id="832dc-149">To ensure that Windows Media Player checks the BITS queue for download jobs, you should create a value in the following registry subkey:</span></span>

<span data-ttu-id="832dc-150">**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ Services**</span><span class="sxs-lookup"><span data-stu-id="832dc-150">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Services**</span></span>

<span data-ttu-id="832dc-151">O valor deve ser criado da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="832dc-151">The value should be created as follows.</span></span>



| <span data-ttu-id="832dc-152">Nome</span><span class="sxs-lookup"><span data-stu-id="832dc-152">Name</span></span>                | <span data-ttu-id="832dc-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="832dc-153">Type</span></span>      | <span data-ttu-id="832dc-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="832dc-154">Description</span></span>                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="832dc-155">**RefreshDownload**</span><span class="sxs-lookup"><span data-stu-id="832dc-155">**RefreshDownload**</span></span> | <span data-ttu-id="832dc-156">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="832dc-156">**DWORD**</span></span> | <span data-ttu-id="832dc-157">Especifica se o Windows Media Player deve inspecionar a fila BITS para trabalhos de download.</span><span class="sxs-lookup"><span data-stu-id="832dc-157">Specifies whether Windows Media Player should inspect the BITS queue for download jobs.</span></span> <span data-ttu-id="832dc-158">Se o valor for zero, o Player não inspecionará a fila do BITS.</span><span class="sxs-lookup"><span data-stu-id="832dc-158">If the value is zero, the Player will not inspect the BITS queue.</span></span> <span data-ttu-id="832dc-159">O Player deve inspecionar a fila se o valor for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="832dc-159">The Player must inspect the queue if the value is nonzero.</span></span> |



 

<span data-ttu-id="832dc-160">Você pode usar a seguinte sintaxe alternativa para adicionar trabalhos do BITS que o Windows Media Player não conclui, mas para o qual ele simplesmente mostra informações de status:</span><span class="sxs-lookup"><span data-stu-id="832dc-160">You can use the following alternate syntax to add BITS jobs that Windows Media Player does not complete, but for which it simply shows status information:</span></span>

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

<span data-ttu-id="832dc-161">Ao usar a sintaxe anterior, você deve escrever o código para concluir o download do BITS, organizar o conteúdo no computador do usuário e adicionar o conteúdo à biblioteca, se desejado.</span><span class="sxs-lookup"><span data-stu-id="832dc-161">When you use the preceding syntax, you must write code to complete the BITS download, organize the content on the user's computer, and add the content to the library, if desired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="832dc-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="832dc-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="832dc-163">CryptGenRandom</span><span class="sxs-lookup"><span data-stu-id="832dc-163">CryptGenRandom</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[<span data-ttu-id="832dc-164">**DownloadItem.getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="832dc-164">**DownloadItem.getItemInfo**</span></span>](downloaditem-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="832dc-165">**DownloadManager. getbaixecollection**</span><span class="sxs-lookup"><span data-stu-id="832dc-165">**DownloadManager.getDownloadCollection**</span></span>](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="832dc-166">**Referência para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="832dc-166">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 