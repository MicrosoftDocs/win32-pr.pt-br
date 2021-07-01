---
title: API de mestre de imagem
description: API de mestre de imagem
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fabf41d1c82420709b39bb5db03c2ac3e851d2
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119671"
---
# <a name="image-mastering-api"></a><span data-ttu-id="a0f50-103">API de mestre de imagem</span><span class="sxs-lookup"><span data-stu-id="a0f50-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="a0f50-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="a0f50-104">Purpose</span></span>

<span data-ttu-id="a0f50-105">A API de mestre de imagem do Microsoft Windows permite que os aplicativos testem e gravem imagens em mídia de armazenamento óptico de CD, DVD e Blu-Ray.</span><span class="sxs-lookup"><span data-stu-id="a0f50-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="a0f50-106">Outra mídia semelhante a um disco que deite imagens da mesma maneira também pode usar essa API.</span><span class="sxs-lookup"><span data-stu-id="a0f50-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a0f50-107">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="a0f50-107">Developer audience</span></span>

<span data-ttu-id="a0f50-108">O IMAPi foi criado para desenvolvedores de C/C++ e Visual Basic e aqueles que escrevem scripts usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="a0f50-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="a0f50-109">O conhecimento de tecnologias de CD, DVD e Blu-Ray e sistemas de arquivos é recomendado.</span><span class="sxs-lookup"><span data-stu-id="a0f50-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="a0f50-110">Os desenvolvedores podem se beneficiar de uma familiaridade com a revisão mais recente do comando de multimídia (MMC) em [ftp://ftp.T10.org/T10/Drafts/MMC6](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="a0f50-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a0f50-111">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="a0f50-111">Run-time requirements</span></span>

<span data-ttu-id="a0f50-112">Há suporte nativo para o IMAPi 2,0 a partir do Windows Vista e do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a0f50-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a0f50-113">A habilitação da funcionalidade IMAPi 2,0 para o Windows XP e o Windows Server 2003 requer a instalação do pacote de atualização do [KB932716](https://support.microsoft.com/kb/932716) .</span><span class="sxs-lookup"><span data-stu-id="a0f50-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="a0f50-114">Se esse pacote não estiver instalado, o Windows XP ainda oferecerá suporte nativo ao [imapi 1,0](imapiv1.md).</span><span class="sxs-lookup"><span data-stu-id="a0f50-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="a0f50-115">O Windows Feature Pack para armazenamento está disponível para o público por meio do [centro de download da Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span><span class="sxs-lookup"><span data-stu-id="a0f50-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="a0f50-116">Informações adicionais sobre alterações de API específicas podem ser encontradas na seção [o que há de novo](what-s-new.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f50-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="a0f50-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a0f50-117">In this section</span></span>



| <span data-ttu-id="a0f50-118">Tópico</span><span class="sxs-lookup"><span data-stu-id="a0f50-118">Topic</span></span>                                             | <span data-ttu-id="a0f50-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0f50-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0f50-120">Novidades</span><span class="sxs-lookup"><span data-stu-id="a0f50-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="a0f50-121">Informações detalhando cada versão significativa da API de mestre de imagem.</span><span class="sxs-lookup"><span data-stu-id="a0f50-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="a0f50-122">Sobre o IMAPi</span><span class="sxs-lookup"><span data-stu-id="a0f50-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="a0f50-123">Informações gerais sobre a API de mestre de imagem.</span><span class="sxs-lookup"><span data-stu-id="a0f50-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="a0f50-124">Usando o IMAPi</span><span class="sxs-lookup"><span data-stu-id="a0f50-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="a0f50-125">Tópicos relacionados a tarefas que demonstram como usar a API de mestre de imagem.</span><span class="sxs-lookup"><span data-stu-id="a0f50-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="a0f50-126">Referência de IMAPi</span><span class="sxs-lookup"><span data-stu-id="a0f50-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="a0f50-127">Descrições detalhadas de interfaces IMAPi e outros elementos de programação.</span><span class="sxs-lookup"><span data-stu-id="a0f50-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="a0f50-128">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="a0f50-128">Additional resources</span></span>

<span data-ttu-id="a0f50-129">Mais informações sobre o IMAPi e outros assuntos relacionados podem ser encontradas nos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="a0f50-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



| <span data-ttu-id="a0f50-130">Tópico</span><span class="sxs-lookup"><span data-stu-id="a0f50-130">Topic</span></span>                                                                                                 | <span data-ttu-id="a0f50-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0f50-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0f50-132">Blog de armazenamento óptico da Microsoft</span><span class="sxs-lookup"><span data-stu-id="a0f50-132">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="a0f50-133">Realça os tópicos que se concentram na implementação da API de mestre de imagem em cenários de desenvolvimento do mundo real.</span><span class="sxs-lookup"><span data-stu-id="a0f50-133">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a0f50-134">Fórum de discussão sobre plataforma ótica</span><span class="sxs-lookup"><span data-stu-id="a0f50-134">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="a0f50-135">Discuta CDROM.SYS, IMAPIv2 e problemas do sistema de arquivos dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="a0f50-135">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="a0f50-136">Este fórum se concentra em tópicos de nível de sistema e destina-se a desenvolvedores de aplicativos em vez de endusers.</span><span class="sxs-lookup"><span data-stu-id="a0f50-136">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="a0f50-137">Comitê Técnico T10</span><span class="sxs-lookup"><span data-stu-id="a0f50-137">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="a0f50-138">Um comitê técnico do Comitê Internacional de padrões de tecnologia da informação (INCITS, pronunciado "insights").</span><span class="sxs-lookup"><span data-stu-id="a0f50-138">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="a0f50-139">O INCITS é reconhecido pelo e opera em regras que são aprovadas pelo American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a0f50-139">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="a0f50-140">Essas regras foram projetadas para garantir que os padrões voluntários sejam desenvolvidos pelo consenso de grupos do setor.</span><span class="sxs-lookup"><span data-stu-id="a0f50-140">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="a0f50-141">OSTA (Associação de tecnologia de armazenamento óptico)</span><span class="sxs-lookup"><span data-stu-id="a0f50-141">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="a0f50-142">Trabalha para moldar o futuro do setor por meio de reuniões regulares de aplicativos de armazenamento óptico comercial (COSA), compatibilidade com DVD, marketing, MPV (MusicPhotoVideo), comitês UDF e um novo comitê de laser azul adhoc.</span><span class="sxs-lookup"><span data-stu-id="a0f50-142">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="a0f50-143">Empresas interessadas em todo o mundo são convidadas para participar da organização e participar de seus comitês e programas.</span><span class="sxs-lookup"><span data-stu-id="a0f50-143">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 

