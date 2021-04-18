---
title: Recursos de arquivo ASF
description: Recursos de arquivo ASF
ms.assetid: 6e180f27-69ef-4fe0-b06c-b2ead7be8a05
keywords:
- SDK do Windows Media Format, recursos de arquivo ASF
- SDK do Windows Media Format, recursos
- ASF (Advanced Systems Format), recursos de arquivo
- ASF (formato de sistemas avançados), recursos de arquivo
- ASF (Advanced Systems Format), recursos
- ASF (formato de sistemas avançados), recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871d2986ad85716fe198b9a16e1a3772d1cca5f8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105780267"
---
# <a name="asf-file-features"></a><span data-ttu-id="3243d-109">Recursos de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="3243d-109">ASF File Features</span></span>

<span data-ttu-id="3243d-110">A principal finalidade do Windows Media Format SDK é fornecer suporte para encapsular dados de mídia digital em arquivos ASF (Advanced Systems Format) e entregar a mídia a um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="3243d-110">The primary purpose of the Windows Media Format SDK is to provide support for encapsulating digital media data in Advanced Systems Format (ASF) files and delivering the media to a client application.</span></span> <span data-ttu-id="3243d-111">Os cenários de entrega podem variar muito do aplicativo para o aplicativo, mas todos usam a estrutura do arquivo ASF entre a criação e a entrega.</span><span class="sxs-lookup"><span data-stu-id="3243d-111">Delivery scenarios can vary widely from application to application, but all use the ASF file structure between authoring and delivery.</span></span> <span data-ttu-id="3243d-112">Os arquivos ASF estão em conformidade com uma estrutura bem definida, mas bastante flexível.</span><span class="sxs-lookup"><span data-stu-id="3243d-112">ASF files conform to a well defined but very flexible structure.</span></span> <span data-ttu-id="3243d-113">Para obter mais informações sobre a estrutura do arquivo ASF, consulte [visão geral do formato ASF](overview-of-the-asf-format.md).</span><span class="sxs-lookup"><span data-stu-id="3243d-113">For more information about the ASF file structure, see [Overview of the ASF Format](overview-of-the-asf-format.md).</span></span>

<span data-ttu-id="3243d-114">Informações detalhadas sobre os dados em um arquivo ASF são fornecidas na especificação do ASF, que você pode baixar no [site da Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span><span class="sxs-lookup"><span data-stu-id="3243d-114">Detailed information about the data in an ASF file is provided in the ASF specification, which you can download from the [Microsoft Web site](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span></span>

<span data-ttu-id="3243d-115">O Windows Media Format SDK fornece suporte para os recursos da especificação do ASF principalmente por meio do perfil usado para criar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3243d-115">The Windows Media Format SDK provides support for the features of the ASF specification mostly through the profile that is used to create a file.</span></span> <span data-ttu-id="3243d-116">Para obter mais informações sobre perfis, consulte [perfis](profiles.md).</span><span class="sxs-lookup"><span data-stu-id="3243d-116">For more information about profiles, see [Profiles](profiles.md).</span></span>

<span data-ttu-id="3243d-117">Os recursos a seguir são discutidos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="3243d-117">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="3243d-118">Fluxos de áudio e vídeo</span><span class="sxs-lookup"><span data-stu-id="3243d-118">Audio and Video Streams</span></span>](audio-and-video-streams.md)
-   [<span data-ttu-id="3243d-119">Fluxos de imagem</span><span class="sxs-lookup"><span data-stu-id="3243d-119">Image Streams</span></span>](image-streams.md)
-   [<span data-ttu-id="3243d-120">Fluxos arbitrários</span><span class="sxs-lookup"><span data-stu-id="3243d-120">Arbitrary Streams</span></span>](arbitrary-streams.md)
-   [<span data-ttu-id="3243d-121">Comandos de script</span><span class="sxs-lookup"><span data-stu-id="3243d-121">Script Commands</span></span>](script-commands.md)
-   [<span data-ttu-id="3243d-122">Extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="3243d-122">Data Unit Extensions</span></span>](data-unit-extensions.md)
-   [<span data-ttu-id="3243d-123">Suporte ao código de tempo SMPTE</span><span class="sxs-lookup"><span data-stu-id="3243d-123">SMPTE Time Code Support</span></span>](smpte-time-code-support.md)
-   [<span data-ttu-id="3243d-124">Exclusão mútua</span><span class="sxs-lookup"><span data-stu-id="3243d-124">Mutual Exclusion</span></span>](mutual-exclusion.md)
-   [<span data-ttu-id="3243d-125">Priorização de fluxo</span><span class="sxs-lookup"><span data-stu-id="3243d-125">Stream Prioritization</span></span>](stream-prioritization.md)
-   [<span data-ttu-id="3243d-126">Compartilhamento de largura de banda</span><span class="sxs-lookup"><span data-stu-id="3243d-126">Bandwidth Sharing</span></span>](bandwidth-sharing.md)
-   [<span data-ttu-id="3243d-127">Índices</span><span class="sxs-lookup"><span data-stu-id="3243d-127">Indexes</span></span>](indexes.md)
-   [<span data-ttu-id="3243d-128">Marcadores</span><span class="sxs-lookup"><span data-stu-id="3243d-128">Markers</span></span>](markers.md)
-   [<span data-ttu-id="3243d-129">Resposta do leitor para recursos do ASF</span><span class="sxs-lookup"><span data-stu-id="3243d-129">Reader Response to ASF Features</span></span>](reader-response-to-asf-features.md)

## <a name="related-topics"></a><span data-ttu-id="3243d-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3243d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3243d-131">**Recursos**</span><span class="sxs-lookup"><span data-stu-id="3243d-131">**Features**</span></span>](features.md)
</dt> </dl>

 

 




