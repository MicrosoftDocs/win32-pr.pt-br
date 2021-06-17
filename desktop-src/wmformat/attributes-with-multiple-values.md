---
title: Atributos com vários valores (Windows Media Format SDK 11)
description: Saiba mais sobre atributos com vários valores no SDK Windows Media Format 11. Alguns atributos de item de mídia podem ter vários valores.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK,atributos
- ASF (Advanced Systems Format), attributes
- ASF (Formato de Sistemas Avançados), atributos
- atributos, vários valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262688"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="8df1f-108">Atributos com vários valores (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="8df1f-108">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="8df1f-109">Alguns dos atributos predefinidos podem ter vários valores atribuídos a eles.</span><span class="sxs-lookup"><span data-stu-id="8df1f-109">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="8df1f-110">Por exemplo, **Artist** é um atributo que pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="8df1f-110">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="8df1f-111">Você pode chamar [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) várias vezes para adicionar quantos valores **de** Artista você precisar.</span><span class="sxs-lookup"><span data-stu-id="8df1f-111">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="8df1f-112">Se você fizer várias chamadas para **AddAttribute** para atributos que não suportam vários valores, o método poderá retornar um código de erro ou simplesmente ignorar sua solicitação.</span><span class="sxs-lookup"><span data-stu-id="8df1f-112">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="8df1f-113">A tabela a seguir lista os atributos que suportam vários valores.</span><span class="sxs-lookup"><span data-stu-id="8df1f-113">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="8df1f-114">Alguns atributos podem ter vários valores somente em arquivos ASF, enquanto outros podem ter vários valores em arquivos ASF e MP3.</span><span class="sxs-lookup"><span data-stu-id="8df1f-114">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="8df1f-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="8df1f-115">Attribute</span></span>                                                 | <span data-ttu-id="8df1f-116">Suporte para vários valores</span><span class="sxs-lookup"><span data-stu-id="8df1f-116">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="8df1f-117">**Autor**</span><span class="sxs-lookup"><span data-stu-id="8df1f-117">**Author**</span></span>](author.md)                                  | <span data-ttu-id="8df1f-118">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="8df1f-118">ASF, MP3</span></span>                    |
| [<span data-ttu-id="8df1f-119">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="8df1f-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="8df1f-120">ASF</span><span class="sxs-lookup"><span data-stu-id="8df1f-120">ASF</span></span>                         |
| [<span data-ttu-id="8df1f-121">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="8df1f-121">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="8df1f-122">ASF</span><span class="sxs-lookup"><span data-stu-id="8df1f-122">ASF</span></span>                         |
| [<span data-ttu-id="8df1f-123">**WM/Categoria**</span><span class="sxs-lookup"><span data-stu-id="8df1f-123">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="8df1f-124">ASF</span><span class="sxs-lookup"><span data-stu-id="8df1f-124">ASF</span></span>                         |
| [<span data-ttu-id="8df1f-125">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="8df1f-125">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="8df1f-126">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="8df1f-126">ASF, MP3</span></span>                    |
| [<span data-ttu-id="8df1f-127">**WM/Wm/Wm**</span><span class="sxs-lookup"><span data-stu-id="8df1f-127">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="8df1f-128">ASF</span><span class="sxs-lookup"><span data-stu-id="8df1f-128">ASF</span></span>                         |
| [<span data-ttu-id="8df1f-129">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="8df1f-129">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="8df1f-130">ASF</span><span class="sxs-lookup"><span data-stu-id="8df1f-130">ASF</span></span>                         |
| [<span data-ttu-id="8df1f-131">**WM/Gênero**</span><span class="sxs-lookup"><span data-stu-id="8df1f-131">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="8df1f-132">ASF</span><span class="sxs-lookup"><span data-stu-id="8df1f-132">ASF</span></span>                         |
| [<span data-ttu-id="8df1f-133">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="8df1f-133">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="8df1f-134">ASF</span><span class="sxs-lookup"><span data-stu-id="8df1f-134">ASF</span></span>                         |
| [<span data-ttu-id="8df1f-135">**WM/Language**</span><span class="sxs-lookup"><span data-stu-id="8df1f-135">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="8df1f-136">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="8df1f-136">ASF, MP3</span></span>                    |
| [<span data-ttu-id="8df1f-137">**\_WM/Synchronizado**</span><span class="sxs-lookup"><span data-stu-id="8df1f-137">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="8df1f-138">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="8df1f-138">ASF, MP3</span></span>                    |
| [<span data-ttu-id="8df1f-139">**WM/Wm/Wm**</span><span class="sxs-lookup"><span data-stu-id="8df1f-139">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="8df1f-140">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="8df1f-140">ASF, MP3</span></span>                    |
| [<span data-ttu-id="8df1f-141">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="8df1f-141">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="8df1f-142">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="8df1f-142">ASF, MP3</span></span>                    |
| [<span data-ttu-id="8df1f-143">**WM/Produtor**</span><span class="sxs-lookup"><span data-stu-id="8df1f-143">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="8df1f-144">ASF</span><span class="sxs-lookup"><span data-stu-id="8df1f-144">ASF</span></span>                         |
| [<span data-ttu-id="8df1f-145">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="8df1f-145">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="8df1f-146">ASF</span><span class="sxs-lookup"><span data-stu-id="8df1f-146">ASF</span></span>                         |
| [<span data-ttu-id="8df1f-147">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="8df1f-147">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="8df1f-148">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="8df1f-148">ASF, MP3</span></span>                    |
| [<span data-ttu-id="8df1f-149">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="8df1f-149">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="8df1f-150">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="8df1f-150">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="8df1f-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8df1f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8df1f-152">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="8df1f-152">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




