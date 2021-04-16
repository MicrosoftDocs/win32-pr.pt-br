---
description: Recursos do VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Recursos do VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757687"
---
# <a name="features-of-the-vmr"></a><span data-ttu-id="97f83-103">Recursos do VMR</span><span class="sxs-lookup"><span data-stu-id="97f83-103">Features of the VMR</span></span>

<span data-ttu-id="97f83-104">O processador de mixagem de vídeo 7 (VMR-7) oferece suporte aos seguintes novos recursos:</span><span class="sxs-lookup"><span data-stu-id="97f83-104">The Video Mixing Renderer 7 (VMR-7) supports the following new features:</span></span>

-   <span data-ttu-id="97f83-105">Mistura real de vários fluxos de vídeo, usando os recursos de mesclagem alfa de dispositivos de hardware do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="97f83-105">Real mixing of multiple video streams, using the alpha-blending capabilities of Direct3D hardware devices.</span></span>
-   <span data-ttu-id="97f83-106">A capacidade de conectar seu próprio componente de composição para implementar efeitos e transições entre vários fluxos de vídeo entrando no VMR.</span><span class="sxs-lookup"><span data-stu-id="97f83-106">The ability to plug in your own compositing component to implement effects and transitions between multiple video streams entering the VMR.</span></span>
-   <span data-ttu-id="97f83-107">Renderização true sem janela.</span><span class="sxs-lookup"><span data-stu-id="97f83-107">True windowless rendering.</span></span> <span data-ttu-id="97f83-108">Não é mais necessário tornar a janela de reprodução de vídeo um filho da janela do aplicativo para conter reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="97f83-108">It is no longer necessary to make the video playback window a child of the application's window in order to contain video playback.</span></span> <span data-ttu-id="97f83-109">O novo modo de renderização sem janela do VMR permite que os aplicativos hospedem facilmente a reprodução de vídeo em qualquer janela sem a necessidade de encaminhar mensagens de janela para o renderizador para processamento específico do processador.</span><span class="sxs-lookup"><span data-stu-id="97f83-109">The VMR's new windowless rendering mode allows applications to easily host video playback within any window without having to forward window messages to the renderer for renderer-specific processing.</span></span>
-   <span data-ttu-id="97f83-110">Um novo modo de reprodução de renderização em que os aplicativos podem fornecer seu próprio componente de alocador para obter acesso à imagem de vídeo decodificada antes de ser exibido na tela.</span><span class="sxs-lookup"><span data-stu-id="97f83-110">A new renderless playback mode where applications can supply their own allocator component to get access to the decoded video image prior to it being displayed on the screen.</span></span>
-   <span data-ttu-id="97f83-111">Suporte aprimorado para PCs equipados com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="97f83-111">Improved support for PCs equipped with multiple monitors.</span></span>
-   <span data-ttu-id="97f83-112">Suporte para a nova arquitetura de aceleração de vídeo DirectX da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="97f83-112">Support for Microsoft's new DirectX Video Acceleration architecture.</span></span>
-   <span data-ttu-id="97f83-113">Suporte para reprodução de vídeo de alta qualidade simultaneamente em várias janelas.</span><span class="sxs-lookup"><span data-stu-id="97f83-113">Support for high-quality video playback concurrently on multiple windows.</span></span>
-   <span data-ttu-id="97f83-114">Suporte para o modo exclusivo do DirectDraw</span><span class="sxs-lookup"><span data-stu-id="97f83-114">Support for DirectDraw Exclusive Mode</span></span>
-   <span data-ttu-id="97f83-115">100% de compatibilidade com versões anteriores com aplicativos existentes.</span><span class="sxs-lookup"><span data-stu-id="97f83-115">100% backward-compatibility with existing applications.</span></span>
-   <span data-ttu-id="97f83-116">Suporte para revisão de quadros e uma maneira confiável de capturar a imagem atual que está sendo exibida.</span><span class="sxs-lookup"><span data-stu-id="97f83-116">Support for frame stepping and a reliable way to capture the current image being displayed.</span></span>
-   <span data-ttu-id="97f83-117">A capacidade dos aplicativos de misturar facilmente seus próprios dados estáticos de imagem (como logotipos de canal ou componentes de interface do usuário) com o vídeo de uma maneira sem cintilação suave.</span><span class="sxs-lookup"><span data-stu-id="97f83-117">The ability for applications to easily alpha-blend their own static image data (such as channel logos or UI components) with the video in a smooth flicker-free way.</span></span>

<span data-ttu-id="97f83-118">O VMR-9 dá suporte a todos os recursos listados acima, além de:</span><span class="sxs-lookup"><span data-stu-id="97f83-118">The VMR-9 supports all the features listed above, plus:</span></span>

-   <span data-ttu-id="97f83-119">A capacidade de processar dados de vídeo diretamente com APIs do Direct3D, como sombreadores de pixel.</span><span class="sxs-lookup"><span data-stu-id="97f83-119">The ability to process video data directly with Direct3D APIs such as pixel shaders.</span></span>
-   <span data-ttu-id="97f83-120">Suporte aprimorado para conteúdo de vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="97f83-120">Improved support for interlaced video content.</span></span>
-   <span data-ttu-id="97f83-121">Suporte em qualquer plataforma compatível com o DirectX.</span><span class="sxs-lookup"><span data-stu-id="97f83-121">Support on any platform supported by DirectX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97f83-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97f83-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97f83-123">Sobre o processamento de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="97f83-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



