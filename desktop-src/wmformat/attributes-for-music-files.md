---
title: Atributos para arquivos de música
description: Atributos para arquivos de música
ms.assetid: 098d9241-c8b0-4b0c-b9c1-668497f91e8c
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, arquivos de áudio
- atributos, arquivos de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5956296da5ef43ed3a8d35ecc2d7e6d0a4c97e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635324"
---
# <a name="attributes-for-music-files"></a><span data-ttu-id="f75b9-108">Atributos para arquivos de música</span><span class="sxs-lookup"><span data-stu-id="f75b9-108">Attributes for Music Files</span></span>

<span data-ttu-id="f75b9-109">Esta seção lista os atributos normalmente usados para arquivos de áudio que contêm música.</span><span class="sxs-lookup"><span data-stu-id="f75b9-109">This section lists the attributes commonly used for audio files containing music.</span></span> <span data-ttu-id="f75b9-110">É recomendável que você defina atributos para arquivos de acordo com essas listas para garantir que seus arquivos sejam totalmente compatíveis com uma ampla variedade de aplicativos de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f75b9-110">It is recommended that you set attributes for files according to these lists to ensure that your files are fully compatible with a wide variety of playback applications.</span></span> <span data-ttu-id="f75b9-111">Os atributos nesta seção são listados em três categorias: primário, secundário e terciário.</span><span class="sxs-lookup"><span data-stu-id="f75b9-111">The attributes in this section are listed in three categories: primary, secondary, and tertiary.</span></span>

<span data-ttu-id="f75b9-112">Os atributos primários transmitem as informações mais básicas sobre um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f75b9-112">Primary attributes convey the most basic information about a file.</span></span> <span data-ttu-id="f75b9-113">Se você estiver criando arquivos de áudio para distribuição, esse é o conjunto mínimo de atributos que você deve usar.</span><span class="sxs-lookup"><span data-stu-id="f75b9-113">If you are creating audio files for distribution, this is the minimum set of attributes you should use.</span></span>

<span data-ttu-id="f75b9-114">Os atributos secundários contêm metadados comuns que são importantes, mas não são universais para todos os arquivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="f75b9-114">Secondary attributes contain common metadata that is important but not universal to all audio files.</span></span>

<span data-ttu-id="f75b9-115">Os atributos terciários devem ser incluídos conforme necessário, mas não são essenciais para descrever o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f75b9-115">Tertiary attributes should be included as needed, but are not essential to describing the file.</span></span>

## <a name="primary-attributes-for-music"></a><span data-ttu-id="f75b9-116">Atributos primários para música</span><span class="sxs-lookup"><span data-stu-id="f75b9-116">Primary Attributes for Music</span></span>

-   [<span data-ttu-id="f75b9-117">**Autor**</span><span class="sxs-lookup"><span data-stu-id="f75b9-117">**Author**</span></span>](author.md)
-   [<span data-ttu-id="f75b9-118">**Título**</span><span class="sxs-lookup"><span data-stu-id="f75b9-118">**Title**</span></span>](title.md)
-   [<span data-ttu-id="f75b9-119">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="f75b9-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)
-   [<span data-ttu-id="f75b9-120">**WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="f75b9-120">**WM/ContentDistributor**</span></span>](wm-contentdistributor.md)
-   [<span data-ttu-id="f75b9-121">**WM/gênero**</span><span class="sxs-lookup"><span data-stu-id="f75b9-121">**WM/Genre**</span></span>](wm-genre.md)
-   <span data-ttu-id="f75b9-122">[**WM/MCDI**](wm-mcdi.md) (se disponível; caso contrário, use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)ou [**WM/WMContentID**](wm-wmcontentid.md))</span><span class="sxs-lookup"><span data-stu-id="f75b9-122">[**WM/MCDI**](wm-mcdi.md) (if available; otherwise use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md), or [**WM/WMContentID**](wm-wmcontentid.md))</span></span>
-   [<span data-ttu-id="f75b9-123">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="f75b9-123">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
-   [<span data-ttu-id="f75b9-124">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="f75b9-124">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
-   [<span data-ttu-id="f75b9-125">**WM/provedor**</span><span class="sxs-lookup"><span data-stu-id="f75b9-125">**WM/Provider**</span></span>](wm-provider.md)
-   [<span data-ttu-id="f75b9-126">**WM/TrackNumber**</span><span class="sxs-lookup"><span data-stu-id="f75b9-126">**WM/TrackNumber**</span></span>](wm-tracknumber.md)

## <a name="secondary-attributes-for-music"></a><span data-ttu-id="f75b9-127">Atributos secundários para música</span><span class="sxs-lookup"><span data-stu-id="f75b9-127">Secondary Attributes for Music</span></span>

-   [<span data-ttu-id="f75b9-128">**Direitos autorais**</span><span class="sxs-lookup"><span data-stu-id="f75b9-128">**Copyright**</span></span>](copyright.md)
-   [<span data-ttu-id="f75b9-129">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="f75b9-129">**WM/Composer**</span></span>](wm-composer.md)
-   [<span data-ttu-id="f75b9-130">**WM/Codificaçãotime**</span><span class="sxs-lookup"><span data-stu-id="f75b9-130">**WM/EncodingTime**</span></span>](wm-encodingtime.md)
-   [<span data-ttu-id="f75b9-131">**WM/linguagem**</span><span class="sxs-lookup"><span data-stu-id="f75b9-131">**WM/Language**</span></span>](wm-language.md)
-   [<span data-ttu-id="f75b9-132">**WM/ParentalRating**</span><span class="sxs-lookup"><span data-stu-id="f75b9-132">**WM/ParentalRating**</span></span>](wm-parentalrating.md)
-   [<span data-ttu-id="f75b9-133">**WM/produtor**</span><span class="sxs-lookup"><span data-stu-id="f75b9-133">**WM/Producer**</span></span>](wm-producer.md)
-   [<span data-ttu-id="f75b9-134">**WM/ToolName**</span><span class="sxs-lookup"><span data-stu-id="f75b9-134">**WM/ToolName**</span></span>](wm-toolname.md)
-   [<span data-ttu-id="f75b9-135">**WM/ToolVersion**</span><span class="sxs-lookup"><span data-stu-id="f75b9-135">**WM/ToolVersion**</span></span>](wm-toolversion.md)
-   [<span data-ttu-id="f75b9-136">**WM/WMCollectionGroupID**</span><span class="sxs-lookup"><span data-stu-id="f75b9-136">**WM/WMCollectionGroupID**</span></span>](wm-wmcollectiongroupid.md)
-   [<span data-ttu-id="f75b9-137">**WM/WMCollectionID**</span><span class="sxs-lookup"><span data-stu-id="f75b9-137">**WM/WMCollectionID**</span></span>](wm-wmcollectionid.md)
-   [<span data-ttu-id="f75b9-138">**WM/WMContentID**</span><span class="sxs-lookup"><span data-stu-id="f75b9-138">**WM/WMContentID**</span></span>](wm-wmcontentid.md)
-   [<span data-ttu-id="f75b9-139">**WM/gravador**</span><span class="sxs-lookup"><span data-stu-id="f75b9-139">**WM/Writer**</span></span>](wm-writer.md)

## <a name="tertiary-attributes-for-music"></a><span data-ttu-id="f75b9-140">Atributos terciários para música</span><span class="sxs-lookup"><span data-stu-id="f75b9-140">Tertiary Attributes for Music</span></span>

-   [<span data-ttu-id="f75b9-141">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f75b9-141">**Description**</span></span>](description.md)
-   [<span data-ttu-id="f75b9-142">**WM/AuthorURL**</span><span class="sxs-lookup"><span data-stu-id="f75b9-142">**WM/AuthorURL**</span></span>](wm-authorurl.md)
-   [<span data-ttu-id="f75b9-143">**WM/BeatsPerMinute**</span><span class="sxs-lookup"><span data-stu-id="f75b9-143">**WM/BeatsPerMinute**</span></span>](wm-beatsperminute.md)
-   [<span data-ttu-id="f75b9-144">**WM/condutor**</span><span class="sxs-lookup"><span data-stu-id="f75b9-144">**WM/Conductor**</span></span>](wm-conductor.md)
-   [<span data-ttu-id="f75b9-145">**WM/ContentGroupDescription**</span><span class="sxs-lookup"><span data-stu-id="f75b9-145">**WM/ContentGroupDescription**</span></span>](wm-contentgroupdescription.md)
-   [<span data-ttu-id="f75b9-146">**WM/EncodedBy**</span><span class="sxs-lookup"><span data-stu-id="f75b9-146">**WM/EncodedBy**</span></span>](wm-encodedby.md)
-   [<span data-ttu-id="f75b9-147">**WM/EncodingSettings**</span><span class="sxs-lookup"><span data-stu-id="f75b9-147">**WM/EncodingSettings**</span></span>](wm-encodingsettings.md)
-   [<span data-ttu-id="f75b9-148">**WM/InitialKey**</span><span class="sxs-lookup"><span data-stu-id="f75b9-148">**WM/InitialKey**</span></span>](wm-initialkey.md)
-   [<span data-ttu-id="f75b9-149">**WM/letras de música**</span><span class="sxs-lookup"><span data-stu-id="f75b9-149">**WM/Lyrics**</span></span>](wm-lyrics.md)
-   [<span data-ttu-id="f75b9-150">**WM/letras de música \_ sincronizadas**</span><span class="sxs-lookup"><span data-stu-id="f75b9-150">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md)
-   [<span data-ttu-id="f75b9-151">**WM/humor**</span><span class="sxs-lookup"><span data-stu-id="f75b9-151">**WM/Mood**</span></span>](wm-mood.md)
-   [<span data-ttu-id="f75b9-152">**WM/PartOfSet**</span><span class="sxs-lookup"><span data-stu-id="f75b9-152">**WM/PartOfSet**</span></span>](wm-partofset.md)
-   [<span data-ttu-id="f75b9-153">**WM/período**</span><span class="sxs-lookup"><span data-stu-id="f75b9-153">**WM/Period**</span></span>](wm-period.md)
-   [<span data-ttu-id="f75b9-154">**WM/imagem**</span><span class="sxs-lookup"><span data-stu-id="f75b9-154">**WM/Picture**</span></span>](wmpicture.md)
-   [<span data-ttu-id="f75b9-155">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="f75b9-155">**WM/PromotionURL**</span></span>](wm-promotionurl.md)
-   [<span data-ttu-id="f75b9-156">**WM/Publicador**</span><span class="sxs-lookup"><span data-stu-id="f75b9-156">**WM/Publisher**</span></span>](wm-publisher.md)
-   [<span data-ttu-id="f75b9-157">**WM/subtítulo**</span><span class="sxs-lookup"><span data-stu-id="f75b9-157">**WM/SubTitle**</span></span>](wm-subtitle.md)
-   [<span data-ttu-id="f75b9-158">**WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="f75b9-158">**WM/UniqueFileIdentifier**</span></span>](wm-uniquefileidentifier.md)
-   [<span data-ttu-id="f75b9-159">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="f75b9-159">**WM/UserWebURL**</span></span>](wm-userweburl.md)

## <a name="related-topics"></a><span data-ttu-id="f75b9-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f75b9-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f75b9-161">**Atributos por tipo**</span><span class="sxs-lookup"><span data-stu-id="f75b9-161">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="f75b9-162">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="f75b9-162">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




