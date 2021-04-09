---
title: Atributos com vários valores (SDK do Windows Media Format 11)
description: Atributos com vários valores
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, vários valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008712"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="6bce7-107">Atributos com vários valores (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="6bce7-107">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="6bce7-108">Alguns dos atributos predefinidos podem ter vários valores atribuídos a eles.</span><span class="sxs-lookup"><span data-stu-id="6bce7-108">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="6bce7-109">Por exemplo, **artista** é um atributo que pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="6bce7-109">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="6bce7-110">Você pode chamar [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) várias vezes para adicionar quantos valores de **artista** forem necessários.</span><span class="sxs-lookup"><span data-stu-id="6bce7-110">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="6bce7-111">Se você fizer várias chamadas para **AddAttribute** para atributos que não dão suporte a vários valores, o método poderá retornar um código de erro ou simplesmente ignorar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6bce7-111">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="6bce7-112">A tabela a seguir lista os atributos que dão suporte a vários valores.</span><span class="sxs-lookup"><span data-stu-id="6bce7-112">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="6bce7-113">Alguns atributos podem ter vários valores somente em arquivos ASF, enquanto outros podem ter vários valores em arquivos ASF e MP3.</span><span class="sxs-lookup"><span data-stu-id="6bce7-113">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="6bce7-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="6bce7-114">Attribute</span></span>                                                 | <span data-ttu-id="6bce7-115">Suporte para vários valores</span><span class="sxs-lookup"><span data-stu-id="6bce7-115">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="6bce7-116">**Autor**</span><span class="sxs-lookup"><span data-stu-id="6bce7-116">**Author**</span></span>](author.md)                                  | <span data-ttu-id="6bce7-117">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6bce7-117">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6bce7-118">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="6bce7-118">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="6bce7-119">ASF</span><span class="sxs-lookup"><span data-stu-id="6bce7-119">ASF</span></span>                         |
| [<span data-ttu-id="6bce7-120">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="6bce7-120">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="6bce7-121">ASF</span><span class="sxs-lookup"><span data-stu-id="6bce7-121">ASF</span></span>                         |
| [<span data-ttu-id="6bce7-122">**WM/categoria**</span><span class="sxs-lookup"><span data-stu-id="6bce7-122">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="6bce7-123">ASF</span><span class="sxs-lookup"><span data-stu-id="6bce7-123">ASF</span></span>                         |
| [<span data-ttu-id="6bce7-124">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="6bce7-124">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="6bce7-125">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6bce7-125">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6bce7-126">**WM/condutor**</span><span class="sxs-lookup"><span data-stu-id="6bce7-126">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="6bce7-127">ASF</span><span class="sxs-lookup"><span data-stu-id="6bce7-127">ASF</span></span>                         |
| [<span data-ttu-id="6bce7-128">**WM/diretor**</span><span class="sxs-lookup"><span data-stu-id="6bce7-128">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="6bce7-129">ASF</span><span class="sxs-lookup"><span data-stu-id="6bce7-129">ASF</span></span>                         |
| [<span data-ttu-id="6bce7-130">**WM/gênero**</span><span class="sxs-lookup"><span data-stu-id="6bce7-130">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="6bce7-131">ASF</span><span class="sxs-lookup"><span data-stu-id="6bce7-131">ASF</span></span>                         |
| [<span data-ttu-id="6bce7-132">**WM/Gêneroid**</span><span class="sxs-lookup"><span data-stu-id="6bce7-132">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="6bce7-133">ASF</span><span class="sxs-lookup"><span data-stu-id="6bce7-133">ASF</span></span>                         |
| [<span data-ttu-id="6bce7-134">**WM/linguagem**</span><span class="sxs-lookup"><span data-stu-id="6bce7-134">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="6bce7-135">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6bce7-135">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6bce7-136">**WM/letras de música \_ sincronizadas**</span><span class="sxs-lookup"><span data-stu-id="6bce7-136">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="6bce7-137">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6bce7-137">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6bce7-138">**WM/humor**</span><span class="sxs-lookup"><span data-stu-id="6bce7-138">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="6bce7-139">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6bce7-139">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6bce7-140">**WM/imagem**</span><span class="sxs-lookup"><span data-stu-id="6bce7-140">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="6bce7-141">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6bce7-141">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6bce7-142">**WM/produtor**</span><span class="sxs-lookup"><span data-stu-id="6bce7-142">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="6bce7-143">ASF</span><span class="sxs-lookup"><span data-stu-id="6bce7-143">ASF</span></span>                         |
| [<span data-ttu-id="6bce7-144">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="6bce7-144">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="6bce7-145">ASF</span><span class="sxs-lookup"><span data-stu-id="6bce7-145">ASF</span></span>                         |
| [<span data-ttu-id="6bce7-146">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="6bce7-146">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="6bce7-147">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6bce7-147">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6bce7-148">**WM/gravador**</span><span class="sxs-lookup"><span data-stu-id="6bce7-148">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="6bce7-149">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6bce7-149">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="6bce7-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6bce7-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bce7-151">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="6bce7-151">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




