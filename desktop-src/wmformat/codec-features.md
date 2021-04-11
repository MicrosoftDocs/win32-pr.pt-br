---
title: Recursos do codec
description: Recursos do codec
ms.assetid: e0bbdf75-2369-4080-ae8e-aabaa8401dcf
keywords:
- SDK do Windows Media Format, recursos do codec
- SDK do Windows Media Format, recursos
- codecs, recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3623bcb6f338fe11bef3089705801dc3ea047
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159805"
---
# <a name="codec-features"></a><span data-ttu-id="a40ff-106">Recursos do codec</span><span class="sxs-lookup"><span data-stu-id="a40ff-106">Codec Features</span></span>

<span data-ttu-id="a40ff-107">O Windows Media Format SDK é fornecido com vários codecs de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="a40ff-107">The Windows Media Format SDK is delivered with several audio and video codecs.</span></span> <span data-ttu-id="a40ff-108">Você pode usar os codecs fornecidos para compactar e descompactar conteúdo de acordo com uma variedade de necessidades.</span><span class="sxs-lookup"><span data-stu-id="a40ff-108">You can use the codecs provided to compress and decompress content to suit a variety of needs.</span></span> <span data-ttu-id="a40ff-109">O codec usado pelo gravador para compactar dados é especificado por informações de configuração de fluxo no perfil.</span><span class="sxs-lookup"><span data-stu-id="a40ff-109">The codec that is used by the writer to compress data is specified by stream configuration information in the profile.</span></span> <span data-ttu-id="a40ff-110">As informações do perfil são armazenadas no cabeçalho do arquivo criado pelo gravador.</span><span class="sxs-lookup"><span data-stu-id="a40ff-110">Information from the profile is then stored in the header of the file created by the writer.</span></span> <span data-ttu-id="a40ff-111">Em seguida, quando o arquivo é aberto pelo leitor ou leitor síncrono, as informações de perfil no cabeçalho identificam o codec necessário para descompactar os dados.</span><span class="sxs-lookup"><span data-stu-id="a40ff-111">Then, when the file is opened by the reader or synchronous reader, the profile information in the header identifies the codec needed to decompress the data.</span></span>

<span data-ttu-id="a40ff-112">Os recursos a seguir são discutidos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="a40ff-112">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="a40ff-113">Codecs com suporte</span><span class="sxs-lookup"><span data-stu-id="a40ff-113">Supported Codecs</span></span>](supported-codecs.md)
-   [<span data-ttu-id="a40ff-114">Codificação de taxa de bits constante (CBR)</span><span class="sxs-lookup"><span data-stu-id="a40ff-114">Constant Bit Rate (CBR) Encoding</span></span>](constant-bit-rate--cbr--encoding.md)
-   [<span data-ttu-id="a40ff-115">Codificação de taxa de bits variável (VBR)</span><span class="sxs-lookup"><span data-stu-id="a40ff-115">Variable Bit Rate (VBR) Encoding</span></span>](variable-bit-rate--vbr--encoding.md)
-   [<span data-ttu-id="a40ff-116">Codificação de duas passagens</span><span class="sxs-lookup"><span data-stu-id="a40ff-116">Two-Pass Encoding</span></span>](two-pass-encoding.md)
-   [<span data-ttu-id="a40ff-117">Suporte de áudio de alta resolução</span><span class="sxs-lookup"><span data-stu-id="a40ff-117">High-Resolution Audio Support</span></span>](high-resolution-audio-support.md)
-   [<span data-ttu-id="a40ff-118">Áudio de atraso baixo</span><span class="sxs-lookup"><span data-stu-id="a40ff-118">Low-Delay Audio</span></span>](low-delay-audio.md)
-   [<span data-ttu-id="a40ff-119">Saída de áudio S/PDIF</span><span class="sxs-lookup"><span data-stu-id="a40ff-119">S/PDIF Audio Output</span></span>](s-pdif-audio-output.md)
-   [<span data-ttu-id="a40ff-120">Imagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="a40ff-120">Video Image</span></span>](video-image.md)
-   [<span data-ttu-id="a40ff-121">Modelos de conformidade do dispositivo</span><span class="sxs-lookup"><span data-stu-id="a40ff-121">Device Conformance Templates</span></span>](device-conformance-templates.md)
-   [<span data-ttu-id="a40ff-122">Configurações de complexidade do vídeo</span><span class="sxs-lookup"><span data-stu-id="a40ff-122">Video Complexity Settings</span></span>](video-complexity-settings.md)
-   [<span data-ttu-id="a40ff-123">Interpolação de quadros</span><span class="sxs-lookup"><span data-stu-id="a40ff-123">Frame Interpolation</span></span>](frame-interpolation.md)

## <a name="related-topics"></a><span data-ttu-id="a40ff-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a40ff-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a40ff-125">**Recursos**</span><span class="sxs-lookup"><span data-stu-id="a40ff-125">**Features**</span></span>](features.md)
</dt> </dl>

 

 




