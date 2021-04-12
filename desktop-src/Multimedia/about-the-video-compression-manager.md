---
title: Sobre o Gerenciador de compactação de vídeo
description: Sobre o Gerenciador de compactação de vídeo
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Multimídia do Windows, Gerenciador de compactação de vídeo (VCM)
- multimídia, Gerenciador de compactação de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454022"
---
# <a name="about-the-video-compression-manager"></a><span data-ttu-id="67758-105">Sobre o Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="67758-105">About the Video Compression Manager</span></span>

<span data-ttu-id="67758-106">Normalmente, os compactadores instaláveis operam com dados de imagem de vídeo armazenados em arquivos AVI (áudio-vídeo intercalado).</span><span class="sxs-lookup"><span data-stu-id="67758-106">Typically, installable compressors operate with video-image data stored in audio-video interleaved (AVI) files.</span></span> <span data-ttu-id="67758-107">Esta visão geral explica as técnicas de programação usadas para acessar os compactadores instaláveis por meio do VCM e aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="67758-107">This overview explains the programming techniques used to access installable compressors through VCM and covers the following topics:</span></span>

-   <span data-ttu-id="67758-108">VCM e a arquitetura de vídeo para Windows</span><span class="sxs-lookup"><span data-stu-id="67758-108">VCM and the Video for Windows architecture</span></span>
-   <span data-ttu-id="67758-109">Compactando e descompactando dados de imagem do seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="67758-109">Compressing and decompressing image data from your application</span></span>
-   <span data-ttu-id="67758-110">Usando renderizadores VCM para desenhar dados de seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="67758-110">Using VCM renderers to draw data from your application</span></span>
-   <span data-ttu-id="67758-111">Funções e estruturas do VCM</span><span class="sxs-lookup"><span data-stu-id="67758-111">VCM functions and structures</span></span>

<span data-ttu-id="67758-112">Antes de ler esta visão geral, você deve estar familiarizado com os serviços gráficos do Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="67758-112">Before you read this overview, you should be familiar with the Microsoft Win32 graphic services.</span></span> <span data-ttu-id="67758-113">Em particular, bitmaps e estruturas relacionadas a bitmaps, como [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) e [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), são usados extensivamente pelo VCM.</span><span class="sxs-lookup"><span data-stu-id="67758-113">In particular, bitmaps and bitmap-related structures, such as [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) and [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), are used extensively by VCM.</span></span> <span data-ttu-id="67758-114">Para obter informações adicionais sobre as estruturas **BITMAPINFO** e **BITMAPINFOHEADER** , consulte [bitmaps](/previous-versions//ms532349(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67758-114">For additional information about the **BITMAPINFO** and **BITMAPINFOHEADER** structures, see [Bitmaps](/previous-versions//ms532349(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="67758-115">O Gerenciador de compactação de áudio (ACM) fornece suporte de nível de sistema para drivers de compactação e descompactação de áudio.</span><span class="sxs-lookup"><span data-stu-id="67758-115">The audio compression manager (ACM) provides system-level support for audio compression and decompression drivers.</span></span> <span data-ttu-id="67758-116">Para obter uma descrição dos serviços de compactação de áudio, consulte [Gerenciador de compactação de áudio](audio-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="67758-116">For a description of the audio compression services, see [Audio Compression Manager](audio-compression-manager.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="67758-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67758-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67758-118">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="67758-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 