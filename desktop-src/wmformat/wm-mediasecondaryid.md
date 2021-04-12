---
title: WM/MediaClassSecondaryID
description: O atributo WM/MediaClassSecondaryID contém o GUID da classe de mídia secundária.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- Formato de mídia do Windows do WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364961"
---
# <a name="wmmediaclasssecondaryid"></a><span data-ttu-id="4290f-104">WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="4290f-104">WM/MediaClassSecondaryID</span></span>

<span data-ttu-id="4290f-105">O atributo **WM/MediaClassSecondaryID** contém o GUID da classe de mídia secundária.</span><span class="sxs-lookup"><span data-stu-id="4290f-105">The **WM/MediaClassSecondaryID** attribute contains the GUID of the secondary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4290f-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="4290f-106">Global Constant</span></span>

<span data-ttu-id="4290f-107">g \_ wszWMMediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="4290f-107">g\_wszWMMediaClassSecondaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="4290f-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="4290f-108">Data Type</span></span>

<span data-ttu-id="4290f-109">**\_GUID do tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="4290f-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="4290f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4290f-110">Remarks</span></span>

<span data-ttu-id="4290f-111">Esse atributo deve ser definido como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4290f-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="4290f-112">GUID de classe secundária</span><span class="sxs-lookup"><span data-stu-id="4290f-112">Secondary class GUID</span></span>                   | <span data-ttu-id="4290f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4290f-113">Description</span></span>                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4290f-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span><span class="sxs-lookup"><span data-stu-id="4290f-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span></span> | <span data-ttu-id="4290f-115">Use para arquivos de livro de áudio.</span><span class="sxs-lookup"><span data-stu-id="4290f-115">Use for audio book files.</span></span>                                                                                                                                                               |
| <span data-ttu-id="4290f-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span><span class="sxs-lookup"><span data-stu-id="4290f-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span></span> | <span data-ttu-id="4290f-117">Use para arquivos de áudio que contenham uma palavra falada, mas não são livros de áudio.</span><span class="sxs-lookup"><span data-stu-id="4290f-117">Use for audio files that contain spoken word, but are not audio books.</span></span> <span data-ttu-id="4290f-118">Por exemplo, rotinas de comédia de reserva.</span><span class="sxs-lookup"><span data-stu-id="4290f-118">For example, stand-up comedy routines.</span></span>                                                                           |
| <span data-ttu-id="4290f-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span><span class="sxs-lookup"><span data-stu-id="4290f-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span></span> | <span data-ttu-id="4290f-120">Use para arquivos de áudio relacionados a notícias.</span><span class="sxs-lookup"><span data-stu-id="4290f-120">Use for audio files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="4290f-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span><span class="sxs-lookup"><span data-stu-id="4290f-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span></span> | <span data-ttu-id="4290f-122">Use para arquivos de áudio com o talk show Content.</span><span class="sxs-lookup"><span data-stu-id="4290f-122">Use for audio files with talk show content.</span></span>                                                                                                                                             |
| <span data-ttu-id="4290f-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span><span class="sxs-lookup"><span data-stu-id="4290f-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span></span> | <span data-ttu-id="4290f-124">Use para arquivos de vídeo relacionados a notícias.</span><span class="sxs-lookup"><span data-stu-id="4290f-124">Use for video files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="4290f-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span><span class="sxs-lookup"><span data-stu-id="4290f-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span></span> | <span data-ttu-id="4290f-126">Use para arquivos de vídeo que contenham apresentações baseadas na Web, filmes curtos, trailers de filmes e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4290f-126">Use for video files containing Web-based shows, short films, movie trailers, and so on.</span></span> <span data-ttu-id="4290f-127">Esse é o identificador geral para o entretenimento em vídeo que não se encaixa em outra categoria.</span><span class="sxs-lookup"><span data-stu-id="4290f-127">This is the general identifier for video entertainment that does not fit into another category.</span></span> |
| <span data-ttu-id="4290f-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span><span class="sxs-lookup"><span data-stu-id="4290f-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span></span> | <span data-ttu-id="4290f-129">Use para arquivos de áudio que contenham clipes de som de jogos.</span><span class="sxs-lookup"><span data-stu-id="4290f-129">Use for audio files containing sound clips from games.</span></span>                                                                                                                                  |
| <span data-ttu-id="4290f-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span><span class="sxs-lookup"><span data-stu-id="4290f-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span></span> | <span data-ttu-id="4290f-131">Use para arquivos de áudio que contenham músicas completas de faixas sonoras do jogo.</span><span class="sxs-lookup"><span data-stu-id="4290f-131">Use for audio files containing complete songs from game sound tracks.</span></span> <span data-ttu-id="4290f-132">Se apenas parte de uma música for codificada no arquivo, use o identificador para clipes de som do jogo.</span><span class="sxs-lookup"><span data-stu-id="4290f-132">If only part of a song is encoded in the file, use the identifier for game sound clips instead.</span></span>                   |
| <span data-ttu-id="4290f-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span><span class="sxs-lookup"><span data-stu-id="4290f-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span></span> | <span data-ttu-id="4290f-134">Use para arquivos de vídeo que contenham vídeos musicais.</span><span class="sxs-lookup"><span data-stu-id="4290f-134">Use for video files containing music videos.</span></span>                                                                                                                                            |
| <span data-ttu-id="4290f-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span><span class="sxs-lookup"><span data-stu-id="4290f-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span></span> | <span data-ttu-id="4290f-136">Use para arquivos de vídeo que contenham vídeo doméstico geral.</span><span class="sxs-lookup"><span data-stu-id="4290f-136">Use for video files containing general home video.</span></span>                                                                                                                                      |
| <span data-ttu-id="4290f-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span><span class="sxs-lookup"><span data-stu-id="4290f-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span></span> | <span data-ttu-id="4290f-138">Use para arquivos de vídeo que contenham filmes de recursos.</span><span class="sxs-lookup"><span data-stu-id="4290f-138">Use for video files containing feature films.</span></span>                                                                                                                                           |
| <span data-ttu-id="4290f-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span><span class="sxs-lookup"><span data-stu-id="4290f-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span></span> | <span data-ttu-id="4290f-140">Use para arquivos de vídeo que contenham programas de televisão.</span><span class="sxs-lookup"><span data-stu-id="4290f-140">Use for video files containing television shows.</span></span> <span data-ttu-id="4290f-141">Para apresentações baseadas na Web, use o identificador mais genérico.</span><span class="sxs-lookup"><span data-stu-id="4290f-141">For Web-based shows, use the more generic identifier.</span></span>                                                                                  |
| <span data-ttu-id="4290f-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span><span class="sxs-lookup"><span data-stu-id="4290f-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span></span> | <span data-ttu-id="4290f-143">Use para arquivos de vídeo que contenham vídeo corporativo.</span><span class="sxs-lookup"><span data-stu-id="4290f-143">Use for video files containing corporate video.</span></span> <span data-ttu-id="4290f-144">Por exemplo, reuniões registradas ou vídeos de treinamento.</span><span class="sxs-lookup"><span data-stu-id="4290f-144">For example, recorded meetings or training videos.</span></span>                                                                                      |
| <span data-ttu-id="4290f-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span><span class="sxs-lookup"><span data-stu-id="4290f-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span></span> | <span data-ttu-id="4290f-146">Use para arquivos de vídeo que contenham o vídeo Home feito de fotografias.</span><span class="sxs-lookup"><span data-stu-id="4290f-146">Use for video files containing home video made from photographs.</span></span>                                                                                                                        |



 

<span data-ttu-id="4290f-147">Ao especificar um identificador de classe secundário, o arquivo também deve conter um atributo de identificador de classe primário.</span><span class="sxs-lookup"><span data-stu-id="4290f-147">When specifying a secondary class identifier, the file should also contain a primary class identifier attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="4290f-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="4290f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4290f-149">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="4290f-149">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="4290f-150">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="4290f-150">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
</dt> </dl>

 

 




