---
description: Trabalhando com tipos de mídia DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Trabalhando com tipos de mídia DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930117"
---
# <a name="working-with-dmo-media-types"></a><span data-ttu-id="12d76-103">Trabalhando com tipos de mídia DMO</span><span class="sxs-lookup"><span data-stu-id="12d76-103">Working with DMO Media Types</span></span>

<span data-ttu-id="12d76-104">Os tipos de mídia de entrada e saída usados pelo codec DMOs são definidos usando a estrutura [**do \_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="12d76-104">The input and output media types that are used by the codec DMOs are defined using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="12d76-105">Essa estrutura é idêntica ao [**tipo de \_ mídia \_ do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), que é definido no Windows Media Format SDK e no [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type), que é definido no Microsoft DirectShow®.</span><span class="sxs-lookup"><span data-stu-id="12d76-105">This structure is identical to both [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), which is defined in the Windows Media Format SDK, and [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), which is defined in Microsoft DirectShow®.</span></span> <span data-ttu-id="12d76-106">Dependendo do seu aplicativo, você pode usar variáveis definidas como qualquer um desses três tipos.</span><span class="sxs-lookup"><span data-stu-id="12d76-106">Depending upon your application, you may use variables defined as any one of these three types.</span></span> <span data-ttu-id="12d76-107">É seguro converter um ponteiro para uma das estruturas de tipo de mídia como outra.</span><span class="sxs-lookup"><span data-stu-id="12d76-107">It is safe to cast a pointer to one of the media type structures as another.</span></span> <span data-ttu-id="12d76-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="12d76-108">For example:</span></span>


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



<span data-ttu-id="12d76-109">Os tipos de formato usados pelos codecs geralmente são limitados aos descritos pelas estruturas **VIDEOINFOHEADER** e **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="12d76-109">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span> <span data-ttu-id="12d76-110">Para sua conveniência, constantes para esses tipos de formato são incluídas no arquivo de cabeçalho wmcodecconst. h.</span><span class="sxs-lookup"><span data-stu-id="12d76-110">For convenience, constants for these format types are included in the wmcodecconst.h header file.</span></span> <span data-ttu-id="12d76-111">Os nomes das constantes são WMCFORMAT \_ VIDEOINFO e WMCFORMAT \_ WaveFormatEx, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="12d76-111">The constant names are WMCFORMAT\_VideoInfo and WMCFORMAT\_WaveFormatEx respectively.</span></span> <span data-ttu-id="12d76-112">Os codecs de áudio podem funcionar com a estrutura **WAVEFORMATEXTENSIBLE** em algumas circunstâncias e devem ser usados em outros.</span><span class="sxs-lookup"><span data-stu-id="12d76-112">The audio codecs can work with the **WAVEFORMATEXTENSIBLE** structure in some circumstances, and must use it in others.</span></span> <span data-ttu-id="12d76-113">No entanto, o **\_ tipo de mídia DMO \_ . FormatType** é definido com o mesmo valor que é para **WAVEFORMATEX**.</span><span class="sxs-lookup"><span data-stu-id="12d76-113">However, **DMO\_MEDIA\_TYPE.formattype** is set to the same value as it is for **WAVEFORMATEX**.</span></span> <span data-ttu-id="12d76-114">Para obter mais informações sobre como usar o **WAVEFORMATEXTENSIBLE**, consulte [usando High-Definition áudio](usinghighdefinitionaudio.md).</span><span class="sxs-lookup"><span data-stu-id="12d76-114">For more information about using **WAVEFORMATEXTENSIBLE**, see [Using High-Definition Audio](usinghighdefinitionaudio.md).</span></span>

> [!Note]  
>    <span data-ttu-id="12d76-115">Você deve incluir a estrutura de tipo de formato usada como a saída do codificador em qualquer contêiner usado para armazenar os dados compactados.</span><span class="sxs-lookup"><span data-stu-id="12d76-115">You must include the format type structure used as the encoder output in whatever container you use to store the compressed data.</span></span> <span data-ttu-id="12d76-116">Os decodificadores exigem a estrutura de formato original para descompactar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="12d76-116">The decoders require the original format structure to decompress the content.</span></span> <span data-ttu-id="12d76-117">Além dos membros da estrutura, os tipos de áudio e vídeo do Windows Media compactados exigem informações de formato adicionais, que são acrescentadas à estrutura.</span><span class="sxs-lookup"><span data-stu-id="12d76-117">In addition to the members of the structure, compressed Windows Media Audio and Video types require additional format information, which is appended to the structure.</span></span> <span data-ttu-id="12d76-118">Para obter mais informações, consulte [trabalhando com áudio](workingwithaudio.md) e [trabalhando com vídeo](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="12d76-118">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="12d76-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12d76-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12d76-120">Trabalhando com codec DMOs</span><span class="sxs-lookup"><span data-stu-id="12d76-120">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
