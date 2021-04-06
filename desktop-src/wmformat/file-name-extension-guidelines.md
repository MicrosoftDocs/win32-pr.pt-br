---
title: Diretrizes de extensão de nome de arquivo
description: Diretrizes de extensão de nome de arquivo
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- SDK do Windows Media Format, extensões de nome de arquivo
- ASF (Advanced Systems Format), extensões de nome de arquivo
- ASF (formato de sistemas avançados), extensões de nome de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916226"
---
# <a name="file-name-extension-guidelines"></a><span data-ttu-id="20fe5-106">Diretrizes de extensão de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="20fe5-106">File Name Extension Guidelines</span></span>

<span data-ttu-id="20fe5-107">Uma extensão de nome de arquivo fornece um fornecedor de software independente com informações sobre os requisitos de renderização de um aplicativo que usa essa extensão específica.</span><span class="sxs-lookup"><span data-stu-id="20fe5-107">A file name extension provides an independent software vendor with information about the rendering requirements of an application that uses that particular extension.</span></span>

<span data-ttu-id="20fe5-108">A extensão de nome de arquivo que você deve usar para um arquivo criado por um aplicativo baseado no Windows Media Format SDK é determinada pelo tipo de conteúdo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="20fe5-108">The file name extension you must use for a file created by an application based on the Windows Media Format SDK is determined by the type of content in the file.</span></span> <span data-ttu-id="20fe5-109">Use a lógica a seguir para determinar a extensão de nome de arquivo que você deve usar.</span><span class="sxs-lookup"><span data-stu-id="20fe5-109">Use the following logic to determine the file name extension you must use.</span></span>

<span data-ttu-id="20fe5-110">Se o arquivo contiver fluxos codificados com codecs de terceiros ou quaisquer dados descompactados sem suporte (incluindo dados arbitrários), o arquivo deverá usar a extensão. ASF.</span><span class="sxs-lookup"><span data-stu-id="20fe5-110">If the file contains any streams encoded with third-party codecs or any unsupported uncompressed data (including arbitrary data), the file must use the .asf extension.</span></span>

<span data-ttu-id="20fe5-111">Se o arquivo não contiver fluxos sem suporte e contiver um ou mais fluxos de vídeo descompactados ou codificados com qualquer codec de vídeo do Windows Media, o arquivo deverá usar a extensão. wmv.</span><span class="sxs-lookup"><span data-stu-id="20fe5-111">If the file contains no unsupported streams and contains one or more video streams either uncompressed or encoded with any Windows Media video codec, the file must use the .wmv extension.</span></span> <span data-ttu-id="20fe5-112">Esses arquivos também podem incluir fluxos de áudio PCM, fluxos de áudio codificados com qualquer codec de áudio do Windows Media, fluxos de script e fluxos da Web.</span><span class="sxs-lookup"><span data-stu-id="20fe5-112">These files may also include PCM audio streams, audio streams encoded with any Windows Media audio codec, script streams, and Web streams.</span></span>

<span data-ttu-id="20fe5-113">Se o arquivo não contiver fluxos sem suporte e fluxos de vídeo com suporte e contiver um ou mais fluxos de áudio não compactados PCM ou codificados com qualquer codec de áudio do Windows Media, o arquivo deverá usar a extensão. WMA.</span><span class="sxs-lookup"><span data-stu-id="20fe5-113">If the file contains no unsupported streams and no supported video streams, and contains one or more audio streams either uncompressed PCM or encoded with any Windows Media audio codec, the file must use the .wma extension.</span></span> <span data-ttu-id="20fe5-114">Esses arquivos também podem conter fluxos de script e fluxos da Web.</span><span class="sxs-lookup"><span data-stu-id="20fe5-114">These files may also contain script streams, and Web streams.</span></span>

<span data-ttu-id="20fe5-115">Se o arquivo contiver apenas fluxos que não sejam áudio nem vídeo, ele deverá usar a extensão. ASF.</span><span class="sxs-lookup"><span data-stu-id="20fe5-115">If the file contains only streams that are neither audio nor video, it must use the .asf extension.</span></span>

<span data-ttu-id="20fe5-116">Os tipos de vídeo descompactados com suporte incluem RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU e YVU9.</span><span class="sxs-lookup"><span data-stu-id="20fe5-116">Supported uncompressed video types include RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU, and YVU9.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20fe5-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20fe5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20fe5-118">**Considerações sobre o projeto**</span><span class="sxs-lookup"><span data-stu-id="20fe5-118">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




