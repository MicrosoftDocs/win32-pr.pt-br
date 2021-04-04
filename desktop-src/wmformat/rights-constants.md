---
title: Constantes de direitos
description: Constantes de direitos
ms.assetid: fb20dc57-25da-4613-a324-e081ba87df73
keywords:
- SDK do Windows Media Format, constantes
- DRM (gerenciamento de direitos digitais), constantes
- DRM (gerenciamento de direitos digitais), constantes
- APIs estendidas do cliente DRM, constantes
- APIs estendidas do cliente, constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1349da53b63b1b7df59c13e0e69f7fdbf47ee3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084113"
---
# <a name="rights-constants"></a><span data-ttu-id="65f2e-108">Constantes de direitos</span><span class="sxs-lookup"><span data-stu-id="65f2e-108">Rights Constants</span></span>

<span data-ttu-id="65f2e-109">As constantes listadas na tabela a seguir são usadas para identificar ações de DRM e para criar listas de ações.</span><span class="sxs-lookup"><span data-stu-id="65f2e-109">The constants listed in the following table are used to identify DRM actions and to build lists of actions.</span></span>



| <span data-ttu-id="65f2e-110">Constante</span><span class="sxs-lookup"><span data-stu-id="65f2e-110">Constant</span></span>                                        | <span data-ttu-id="65f2e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="65f2e-111">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f2e-112">marca de ação da g \_ wszWMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="65f2e-112">g\_wszWMDRM\_ACTIONLIST\_TAG</span></span>                    | <span data-ttu-id="65f2e-113">Define o nome do elemento XML para uma lista de ações.</span><span class="sxs-lookup"><span data-stu-id="65f2e-113">Defines the XML element name for an action list.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="65f2e-114">\_marca de \_ ação g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="65f2e-114">g\_wszWMDRM\_ACTION\_TAG</span></span>                        | <span data-ttu-id="65f2e-115">Define o nome do elemento XML para uma entrada em uma lista de ações.</span><span class="sxs-lookup"><span data-stu-id="65f2e-115">Defines the XML element name for an entry in an action list.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="65f2e-116">\_ \_ reprodução à direita g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="65f2e-116">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="65f2e-117">Define a cadeia de caracteres para o direito de reprodução de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="65f2e-117">Defines the string for the right to play content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="65f2e-118">\_ \_ copiar à direita do g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="65f2e-118">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="65f2e-119">Define a cadeia de caracteres para o direito de copiar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="65f2e-119">Defines the string for the right to copy content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="65f2e-120">\_gravação da playlist g wszWMDRM \_ Right \_ \_</span><span class="sxs-lookup"><span data-stu-id="65f2e-120">g\_wszWMDRM\_RIGHT\_PLAYLIST\_BURN</span></span>              | <span data-ttu-id="65f2e-121">Define a cadeia de caracteres para o direito de gravar o conteúdo no CD como parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="65f2e-121">Defines the string for the right to burn content to CD as part of a playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="65f2e-122">g \_ wszWMDRM \_ direita \_ criar \_ imagem em miniatura \_</span><span class="sxs-lookup"><span data-stu-id="65f2e-122">g\_wszWMDRM\_RIGHT\_CREATE\_THUMBNAIL\_IMAGE</span></span>    | <span data-ttu-id="65f2e-123">Define a cadeia de caracteres para o direito de criar uma imagem em miniatura do conteúdo do vídeo.</span><span class="sxs-lookup"><span data-stu-id="65f2e-123">Defines the string for the right to create a thumbnail image from video content.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="65f2e-124">\_ \_ \_ copiar \_ para o \_ CD do g wszWMDRM</span><span class="sxs-lookup"><span data-stu-id="65f2e-124">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="65f2e-125">Define a cadeia de caracteres para o direito de copiar o conteúdo para um CD.</span><span class="sxs-lookup"><span data-stu-id="65f2e-125">Defines the string for the right to copy content to a CD.</span></span> <span data-ttu-id="65f2e-126">As novas licenças não devem usar esse direito.</span><span class="sxs-lookup"><span data-stu-id="65f2e-126">New licenses should not use this right.</span></span> <span data-ttu-id="65f2e-127">Em vez disso, todos os direitos que concedem permissão para copiar conteúdo devem ser cobertos pelo direito de cópia e pelo direito de gravação de playlist.</span><span class="sxs-lookup"><span data-stu-id="65f2e-127">Instead, all rights granting permission to copy content should be covered by the copy right and the playlist burn right.</span></span>                                     |
| <span data-ttu-id="65f2e-128">\_ \_ copiar à direita do g wszWMDRM \_ para o \_ \_ \_ dispositivo SDMI</span><span class="sxs-lookup"><span data-stu-id="65f2e-128">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="65f2e-129">Define a cadeia de caracteres para o direito de copiar conteúdo para um dispositivo que esteja de acordo com o SDMI (Secure Digital Music Initiative).</span><span class="sxs-lookup"><span data-stu-id="65f2e-129">Defines the string for the right to copy content to a device that conforms to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="65f2e-130">As novas licenças não devem usar esse direito.</span><span class="sxs-lookup"><span data-stu-id="65f2e-130">New licenses should not use this right.</span></span> <span data-ttu-id="65f2e-131">Em vez disso, todos os direitos que concedem permissão para copiar conteúdo devem ser cobertos pelo direito de cópia.</span><span class="sxs-lookup"><span data-stu-id="65f2e-131">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="65f2e-132">\_ \_ copiar à direita do g wszWMDRM \_ para um \_ \_ \_ dispositivo não SDMI \_</span><span class="sxs-lookup"><span data-stu-id="65f2e-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="65f2e-133">Define a cadeia de caracteres para o direito de copiar para um dispositivo que não está de acordo com a SDMI (iniciativa de música digital) segura.</span><span class="sxs-lookup"><span data-stu-id="65f2e-133">Defines the string for the right to copy to a device that does not conform to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="65f2e-134">As novas licenças não devem usar esse direito.</span><span class="sxs-lookup"><span data-stu-id="65f2e-134">New licenses should not use this right.</span></span> <span data-ttu-id="65f2e-135">Em vez disso, todos os direitos que concedem permissão para copiar conteúdo devem ser cobertos pelo direito de cópia.</span><span class="sxs-lookup"><span data-stu-id="65f2e-135">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="65f2e-136">\_ \_ backup do g wszWMDRM direito \_</span><span class="sxs-lookup"><span data-stu-id="65f2e-136">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="65f2e-137">Define a cadeia de caracteres para o direito de fazer backup da licença.</span><span class="sxs-lookup"><span data-stu-id="65f2e-137">Defines the string for the right to backup the license.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="65f2e-138">g \_ wszWMDRM \_ de \_ colaboração à \_ direita</span><span class="sxs-lookup"><span data-stu-id="65f2e-138">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="65f2e-139">Define a cadeia de caracteres para o direito de reprodução de conteúdo em uma rede como parte de uma lista de reprodução compartilhada.</span><span class="sxs-lookup"><span data-stu-id="65f2e-139">Defines the string for the right to play content over a network as part of a shared playlist.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="65f2e-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65f2e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65f2e-141">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="65f2e-141">**Constants**</span></span>](constants.md)
</dt> </dl>

 

 




