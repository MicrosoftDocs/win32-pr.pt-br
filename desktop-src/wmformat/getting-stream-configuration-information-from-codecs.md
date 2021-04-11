---
title: Obtendo informações de configuração de fluxo de codecs
description: Obtendo informações de configuração de fluxo de codecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- fluxos, configurações de codecs
- codecs, obtendo configurações de fluxo de
- fluxos, formatos de codec
- codecs, formatos
- fluxos, interface IWMCodecInfo
- IWMCodecInfo, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104365735"
---
# <a name="getting-stream-configuration-information-from-codecs"></a><span data-ttu-id="00eda-109">Obtendo informações de configuração de fluxo de codecs</span><span class="sxs-lookup"><span data-stu-id="00eda-109">Getting Stream Configuration Information from Codecs</span></span>

<span data-ttu-id="00eda-110">Para fluxos de áudio e vídeo que usam os codecs de áudio e vídeo do Windows Media, você deve obter os valores para as estruturas de configuração de fluxo do codec que deseja usar.</span><span class="sxs-lookup"><span data-stu-id="00eda-110">For audio and video streams that use the Windows Media Audio and Video codecs, you should get the values for the stream configuration structures from the codec you want to use.</span></span> <span data-ttu-id="00eda-111">Embora seja possível definir esses valores por conta própria, usar os codecs garante que os valores sejam precisos.</span><span class="sxs-lookup"><span data-stu-id="00eda-111">While it is possible to set these values yourself, using the codecs ensures that the values are accurate.</span></span> <span data-ttu-id="00eda-112">Você não deve alterar os valores nessas estruturas, a menos que a documentação recomende especificamente uma alteração específica.</span><span class="sxs-lookup"><span data-stu-id="00eda-112">You should not alter the values in these structures unless the documentation specifically recommends a particular change.</span></span>

<span data-ttu-id="00eda-113">As informações dos codecs vêm na forma de formatos de codec.</span><span class="sxs-lookup"><span data-stu-id="00eda-113">Information from the codecs comes in the form of codec formats.</span></span> <span data-ttu-id="00eda-114">Cada formato de codec é um formato de fluxo único com suporte pelo codec.</span><span class="sxs-lookup"><span data-stu-id="00eda-114">Each codec format is a single stream format supported by the codec.</span></span> <span data-ttu-id="00eda-115">Para obter mais informações sobre formatos de fluxo, consulte [formatos](formats.md).</span><span class="sxs-lookup"><span data-stu-id="00eda-115">For more information about stream formats, see [Formats](formats.md).</span></span>

<span data-ttu-id="00eda-116">Você pode solicitar informações dos codecs de mídia do Windows usando as interfaces [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)e [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) do objeto do Gerenciador de perfis.</span><span class="sxs-lookup"><span data-stu-id="00eda-116">You can request information from the Windows Media codecs using the [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2), and [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interfaces of the profile manager object.</span></span> <span data-ttu-id="00eda-117">Para obter a interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) de um objeto do Gerenciador de perfis, chame a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="00eda-117">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="00eda-118">Chame **QueryInterface** em **IWMProfileManager** para obter **IWMCodecInfo3**.</span><span class="sxs-lookup"><span data-stu-id="00eda-118">Call **QueryInterface** on **IWMProfileManager** to get **IWMCodecInfo3**.</span></span>

<span data-ttu-id="00eda-119">As seções a seguir descrevem como obter as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="00eda-119">The following sections describe how to get the information you need.</span></span>



| <span data-ttu-id="00eda-120">Seção</span><span class="sxs-lookup"><span data-stu-id="00eda-120">Section</span></span>                                                                                                | <span data-ttu-id="00eda-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="00eda-121">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00eda-122">Para enumerar todos os codecs de mídia do Windows instalados</span><span class="sxs-lookup"><span data-stu-id="00eda-122">To Enumerate All Installed Windows Media Codecs</span></span>](to-enumerate-all-installed-windows-media-codecs.md) | <span data-ttu-id="00eda-123">Descreve como usar os métodos das interfaces **IWMCodecInfo** e **IWMCodecInfo2** para recuperar o nome e o índice de codec de cada codec de mídia do Windows instalado.</span><span class="sxs-lookup"><span data-stu-id="00eda-123">Describes how to use the methods of the **IWMCodecInfo** and **IWMCodecInfo2** interfaces to retrieve the name and codec index of each Windows Media codec installed.</span></span> |
| [<span data-ttu-id="00eda-124">Para enumerar formatos de codec</span><span class="sxs-lookup"><span data-stu-id="00eda-124">To Enumerate Codec Formats</span></span>](to-enumerate-codec-formats.md)                                           | <span data-ttu-id="00eda-125">Descreve como obter objetos de configuração de fluxo de codecs para uso em seus perfis.</span><span class="sxs-lookup"><span data-stu-id="00eda-125">Describes how to get stream configuration objects from codecs for use in your profiles.</span></span>                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="00eda-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00eda-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00eda-127">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="00eda-127">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




