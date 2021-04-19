---
description: Microsoft Media Foundation é a próxima geração de plataforma multimídia para Windows que permite que desenvolvedores, consumidores e provedores de conteúdo adotem a nova onda de conteúdo premium com robustez avançada, qualidade incomparável e interoperabilidade direta.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Sobre o Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782734"
---
# <a name="about-media-foundation"></a><span data-ttu-id="05c55-103">Sobre o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05c55-103">About Media Foundation</span></span>

<span data-ttu-id="05c55-104">Microsoft Media Foundation é a próxima geração de plataforma multimídia para Windows que permite que desenvolvedores, consumidores e provedores de conteúdo adotem a nova onda de conteúdo premium com robustez avançada, qualidade incomparável e interoperabilidade direta.</span><span class="sxs-lookup"><span data-stu-id="05c55-104">Microsoft Media Foundation is the next generation multimedia platform for Windows that enables developers, consumers, and content providers to embrace the new wave of premium content with enhanced robustness, unparalleled quality, and seamless interoperability.</span></span>

<span data-ttu-id="05c55-105">Media Foundation requer o Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="05c55-105">Media Foundation requires Windows Vista or later.</span></span> <span data-ttu-id="05c55-106">Ele usa o COM (modelo de objeto de componente) e requer C/C++.</span><span class="sxs-lookup"><span data-stu-id="05c55-106">It uses the component object model (COM) and requires C/C++.</span></span> <span data-ttu-id="05c55-107">A Microsoft não fornece uma API gerenciada para Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05c55-107">Microsoft does not provide a managed API for Media Foundation.</span></span>

<span data-ttu-id="05c55-108">As APIs de Media Foundation fazem parte do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="05c55-108">The Media Foundation APIs are part of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="05c55-109">Para desenvolver um aplicativo Media Foundation, instale a versão mais recente do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="05c55-109">To develop a Media Foundation application, install the latest version of the Windows SDK.</span></span>

## <a name="audio-and-video-quality"></a><span data-ttu-id="05c55-110">Qualidade de áudio e vídeo</span><span class="sxs-lookup"><span data-stu-id="05c55-110">Audio and Video Quality</span></span>

<span data-ttu-id="05c55-111">O Media Foundation foi projetado para atender aos desafios apresentados pelo conteúdo de alta definição.</span><span class="sxs-lookup"><span data-stu-id="05c55-111">Media Foundation has been designed to meet the challenges posed by high-definition content.</span></span> <span data-ttu-id="05c55-112">Os aprimoramentos de qualidade de áudio e vídeo feitos em toda a plataforma agora possibilitam a entrega de uma ótima experiência para o conteúdo de alta definição da próxima geração.</span><span class="sxs-lookup"><span data-stu-id="05c55-112">Audio and video quality enhancements made throughout the platform now make it possible to deliver a great experience for next generation high-definition content.</span></span>

-   <span data-ttu-id="05c55-113">A DXVA (DirectX Video Acceleration) 2,0 oferece aceleração de vídeo mais eficiente, em comparação com a DXVA 1,0, com decodificação de vídeo mais robusta e simplificada e uso estendido de hardware no processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="05c55-113">DirectX Video Acceleration (DXVA) 2.0 offers more efficient video acceleration, compared with DXVA 1.0, with more robust and streamlined video decoding and extended use of hardware in video processing.</span></span> <span data-ttu-id="05c55-114">Com o DXVA 2,0, o Windows pode lidar com alguns dos mais exigentes conteúdo de alta definição com alta qualidade e maior resiliência de problemas.</span><span class="sxs-lookup"><span data-stu-id="05c55-114">With DXVA 2.0, Windows can handle some of the most demanding high-definition content with high quality and improved glitch-resilience.</span></span>

-   <span data-ttu-id="05c55-115">As informações de espaço de cores são preservadas em todo o pipeline de vídeo.</span><span class="sxs-lookup"><span data-stu-id="05c55-115">Color-space information is preserved throughout the video pipeline.</span></span> <span data-ttu-id="05c55-116">Os usuários podem desfrutar do conteúdo de vídeo com fidelidade total.</span><span class="sxs-lookup"><span data-stu-id="05c55-116">Users can enjoy video content with full fidelity.</span></span> <span data-ttu-id="05c55-117">As informações de cor e as imagens entrelaçadas agora são passadas para o hardware para composições de passagem única.</span><span class="sxs-lookup"><span data-stu-id="05c55-117">Color information and interlaced images are now passed to hardware for single-pass compositions.</span></span> <span data-ttu-id="05c55-118">Preservar as informações de espaço de cores também reduz as conversões desnecessárias de espaço de cores, o que libera mais ciclos para processar conteúdo HD exigente.</span><span class="sxs-lookup"><span data-stu-id="05c55-118">Preserving color-space information also reduces unnecessary color space conversions, which frees more cycles to process demanding HD content.</span></span>
-   <span data-ttu-id="05c55-119">O EVR (processador de vídeo avançado) oferece melhor suporte a tempo, processamento de vídeo aprimorado e maior resiliência de problemas.</span><span class="sxs-lookup"><span data-stu-id="05c55-119">The enhanced video renderer (EVR) offers better timing support, enhanced video processing, and improved glitch-resilience.</span></span> <span data-ttu-id="05c55-120">O suporte à reprodução de tela inteira foi aprimorado e a divisão de vídeo no modo de janela foi minimizada.</span><span class="sxs-lookup"><span data-stu-id="05c55-120">Full-screen playback support has been enhanced, and video tearing in windowed mode has been minimized.</span></span>
-   <span data-ttu-id="05c55-121">O Media Foundation usa o serviço do Agendador de classes de multimídia (MMCSS), um novo serviço do sistema no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="05c55-121">Media Foundation uses the Multimedia Class Scheduler Service (MMCSS), a new system service in Windows Vista.</span></span> <span data-ttu-id="05c55-122">O MMCSS permite que os aplicativos multimídia garantam que seu processamento de tempo-diferenciado recebe acesso priorizado aos recursos da CPU.</span><span class="sxs-lookup"><span data-stu-id="05c55-122">MMCSS enables multimedia applications to ensure that their time-sensitive processing receives prioritized access to CPU resources.</span></span>

## <a name="content-access"></a><span data-ttu-id="05c55-123">Acesso ao conteúdo</span><span class="sxs-lookup"><span data-stu-id="05c55-123">Content Access</span></span>

<span data-ttu-id="05c55-124">À medida que o entretenimento digital passa para a era de alta definição e o conteúdo se torna mais portátil e onipresente, a proteção de conteúdo se tornará parte integrante dos produtos de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="05c55-124">As digital entertainment moves into the high-definition era and content becomes more portable and ubiquitous, content protection will become an integral part of digital media products.</span></span> <span data-ttu-id="05c55-125">A extensibilidade do Media Foundation garante que ele possa dar suporte a essas tendências.</span><span class="sxs-lookup"><span data-stu-id="05c55-125">The extensibility of Media Foundation ensures that it can support these trends.</span></span>

<span data-ttu-id="05c55-126">Além disso, Media Foundation extensibilidade permite que diferentes sistemas de proteção de conteúdo operem juntos.</span><span class="sxs-lookup"><span data-stu-id="05c55-126">In addition, Media Foundation extensibility enables different content protection systems to operate together.</span></span>

## <a name="about-media-foundation"></a><span data-ttu-id="05c55-127">Sobre o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05c55-127">About Media Foundation</span></span>

<span data-ttu-id="05c55-128">Esta seção contém informações gerais sobre as APIs de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05c55-128">This section contains general information about the Media Foundation APIs.</span></span> <span data-ttu-id="05c55-129">Informações detalhadas de programação podem ser encontradas no [Guia de programação de Media Foundation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="05c55-129">Detailed programming information can be found in the [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>



| <span data-ttu-id="05c55-130">Seção</span><span class="sxs-lookup"><span data-stu-id="05c55-130">Section</span></span>                                                                              | <span data-ttu-id="05c55-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="05c55-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="05c55-132">O que há de novo para Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05c55-132">What's New for Media Foundation</span></span>](whats-new-for-media-foundation.md)                | <span data-ttu-id="05c55-133">Descreve os novos recursos do Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05c55-133">Describes new features in Media Foundation.</span></span>                               |
| [<span data-ttu-id="05c55-134">Cabeçalhos e bibliotecas do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05c55-134">Media Foundation Headers and Libraries</span></span>](media-foundation-headers-and-libraries.md) | <span data-ttu-id="05c55-135">Lista os arquivos de cabeçalho e biblioteca que definem as APIs de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05c55-135">Lists the header and library files that define the Media Foundation APIs.</span></span> |
| [<span data-ttu-id="05c55-136">Ferramentas de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05c55-136">Media Foundation Tools</span></span>](media-foundation-tools.md)                                 | <span data-ttu-id="05c55-137">Descreve as ferramentas de desenvolvimento que estão disponíveis para Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05c55-137">Describes the development tools that are available for Media Foundation.</span></span>  |



 

<span data-ttu-id="05c55-138">O Media Foundation não está incluído nas edições N e KN do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="05c55-138">Media Foundation is not included with the N and KN editions of Windows 8.</span></span> <span data-ttu-id="05c55-139">Para obter mais informações, consulte [Microsoft Windows Media Feature Pack para versões N e kN de todas as edições do Windows 8](https://support.microsoft.com/kb/2703761).</span><span class="sxs-lookup"><span data-stu-id="05c55-139">For more information, see [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05c55-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05c55-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05c55-141">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05c55-141">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



