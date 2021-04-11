---
description: Escolhendo um codec de vídeo
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Escolhendo um codec de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164216"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a><span data-ttu-id="40aa6-103">Escolhendo um codec de vídeo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="40aa6-103">Choosing a Video Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="40aa6-104">O codificador do Windows Media Video 9 dá suporte a três categorias de saída codificada: perfil principal, perfil avançado e imagem.</span><span class="sxs-lookup"><span data-stu-id="40aa6-104">The Windows Media Video 9 Encoder supports three categories of encoded output: Main Profile, Advanced Profile, and Image.</span></span> <span data-ttu-id="40aa6-105">A categoria de perfil principal fornece compactação de vídeo geral para conteúdo de vídeo complexo, como filmes ou vídeos de música.</span><span class="sxs-lookup"><span data-stu-id="40aa6-105">The Main Profile category provides general video compression for complex video content, such as movies or music videos.</span></span> <span data-ttu-id="40aa6-106">Os recursos do perfil principal fornecem uma ampla gama de configurações de codificação.</span><span class="sxs-lookup"><span data-stu-id="40aa6-106">The features of the Main Profile provide for a wide range of encoding settings.</span></span> <span data-ttu-id="40aa6-107">Você pode usar o perfil principal para criar vídeo com taxas de bits muito baixas para entrega em dispositivos portáteis ou, na outra extremidade do espectro, você pode usá-lo para criar vídeo de alta definição para cinema digital.</span><span class="sxs-lookup"><span data-stu-id="40aa6-107">You can use the Main Profile to create video with very low bit rates for delivery on handheld devices or, at the other end of the spectrum, you can use it to create high-definition video for digital cinema.</span></span>

<span data-ttu-id="40aa6-108">A ênfase dos algoritmos de codificação no perfil principal é o conteúdo de vídeo dinâmico, mas eles são adequados para outros conteúdos de vídeo também.</span><span class="sxs-lookup"><span data-stu-id="40aa6-108">The emphasis of the encoding algorithms in the Main Profile is on dynamic video content, but they are suitable for other video content as well.</span></span> <span data-ttu-id="40aa6-109">O perfil principal deve ser sua categoria padrão para conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="40aa6-109">The Main Profile should be your default category for video content.</span></span> <span data-ttu-id="40aa6-110">Para atender a necessidades específicas, você pode usar a categoria de perfil avançado, a categoria de imagem ou um codificador separado chamado de codificador de tela do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="40aa6-110">To meet specific needs, you can use the Advanced Profile category, the Image category, or a separate encoder called the Windows Media Video 9 Screen encoder.</span></span> <span data-ttu-id="40aa6-111">A tabela a seguir lista as quatro opções.</span><span class="sxs-lookup"><span data-stu-id="40aa6-111">The following table lists the four options.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="40aa6-112">Finalidade</span><span class="sxs-lookup"><span data-stu-id="40aa6-112">Purpose</span></span></th>
<th><span data-ttu-id="40aa6-113">Codec</span><span class="sxs-lookup"><span data-stu-id="40aa6-113">Codec</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40aa6-114">Codificação de vídeo de uso geral</span><span class="sxs-lookup"><span data-stu-id="40aa6-114">General-purpose video encoding</span></span></td>
<td><span data-ttu-id="40aa6-115"><a href="windowsmediavideo9encoder.md">Codificador do Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="40aa6-115"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="40aa6-116">Perfil Principal</span><span class="sxs-lookup"><span data-stu-id="40aa6-116">Main Profile</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40aa6-117">Codificando vídeo de alta definição ou vídeo que está de acordo com o padrão SMPTE do perfil avançado VC-1</span><span class="sxs-lookup"><span data-stu-id="40aa6-117">Encoding high definition video or video that conforms to the VC-1 Advanced Profile SMPTE standard</span></span></td>
<td><span data-ttu-id="40aa6-118"><a href="windowsmediavideo9encoder.md">Codificador do Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="40aa6-118"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="40aa6-119">Perfil avançado</span><span class="sxs-lookup"><span data-stu-id="40aa6-119">Advanced Profile</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40aa6-120">Convertendo imagens de bitmap em vídeo dinâmico</span><span class="sxs-lookup"><span data-stu-id="40aa6-120">Converting bitmapped images to dynamic video</span></span></td>
<td><span data-ttu-id="40aa6-121"><a href="windowsmediavideo9encoder.md">Codificador do Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="40aa6-121"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="40aa6-122">Imagem</span><span class="sxs-lookup"><span data-stu-id="40aa6-122">Image</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40aa6-123">Codificação de vídeo de aplicativo de computador (captura de tela) ou outro vídeo altamente estático</span><span class="sxs-lookup"><span data-stu-id="40aa6-123">Encoding computer-application video (screen capture) or other highly static video</span></span></td>
<td><span data-ttu-id="40aa6-124"><a href="windowsmediavideo9screenencoder.md"><strong>Codificador de tela do Windows Media Video 9</strong></a></span><span class="sxs-lookup"><span data-stu-id="40aa6-124"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9 Screen Encoder</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="40aa6-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40aa6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40aa6-126">Trabalhando com vídeo</span><span class="sxs-lookup"><span data-stu-id="40aa6-126">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



