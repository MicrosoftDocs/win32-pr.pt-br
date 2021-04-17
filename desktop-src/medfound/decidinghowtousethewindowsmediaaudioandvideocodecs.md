---
description: Usando os objetos codec e DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Usando os objetos codec e DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105761568"
---
# <a name="using-the-codec-and-dsp-objects"></a><span data-ttu-id="5f175-103">Usando os objetos codec e DSP</span><span class="sxs-lookup"><span data-stu-id="5f175-103">Using the Codec and DSP Objects</span></span>

<span data-ttu-id="5f175-104">Há várias maneiras de usar os codecs de áudio e vídeo do Windows Media e os DSPs para codificar, decodificar ou transformar seu conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="5f175-104">There are several ways to use the Windows Media Audio and Video codecs and DSPs to encode, decode, or transform your digital media content.</span></span> <span data-ttu-id="5f175-105">O codec de áudio e vídeo do Windows Media e a API do DSP destinam-se a usuários que precisam configurar objetos codec e DSP manualmente ou usá-los fora do contexto de um dos SDKs do Windows Media, como o SDK do Windows Media Format ou SDK do Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="5f175-105">The Windows Media Audio and Video Codec and DSP API is intended for those users who need to configure codec and DSP objects manually or use them outside of the context one of the Windows Media SDKs, such as the Windows Media Format SDK or Media Foundation SDK.</span></span>

<span data-ttu-id="5f175-106">Os criadores de conteúdo e os usuários finais podem usar uma variedade de ferramentas e aplicativos para codificar conteúdo em fluxos de vídeo de áudio do Windows ou Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5f175-106">Content creators and end users can use a variety of tools and applications to encode content in Windows Media Audio or Windows Media Video streams.</span></span> <span data-ttu-id="5f175-107">O codificador de mídia do Windows, por exemplo, foi projetado especificamente para facilitar o processo de codificação.</span><span class="sxs-lookup"><span data-stu-id="5f175-107">Windows Media Encoder, for example, is specifically designed to make the encoding process easy.</span></span> <span data-ttu-id="5f175-108">Da mesma forma, o Windows Media Player é especialmente projetado para funcionar bem com dados de mídia digital codificados nos formatos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="5f175-108">Likewise, Windows Media Player is specially designed to work well with digital media data that is encoded in Windows Media formats.</span></span> <span data-ttu-id="5f175-109">Para muitos aplicativos, usar o SDK do Windows Media Encoder ou o SDK do Windows Media Player é tudo o que é necessário.</span><span class="sxs-lookup"><span data-stu-id="5f175-109">For many applications, using the Windows Media Encoder SDK or the Windows Media Player SDK is all that is needed.</span></span> <span data-ttu-id="5f175-110">Em particular, essas duas tecnologias são boas para cenários que se assemelham à funcionalidade das ferramentas que automatizam.</span><span class="sxs-lookup"><span data-stu-id="5f175-110">In particular, these two technologies are good for scenarios that resemble the functionality of the tools they automate.</span></span>

<span data-ttu-id="5f175-111">Se você precisar de mais controle sobre o processo de codificação ou decodificação, mas ainda pretende usar o ASF (Advanced Systems Format) como um contêiner para seus dados de mídia, o SDK do Windows Media Format pode ser uma boa opção.</span><span class="sxs-lookup"><span data-stu-id="5f175-111">If you need greater control over the encoding or decoding process, but you still intend to use the Advanced Systems Format (ASF) as a container for your media data, the Windows Media Format SDK might be a good choice.</span></span> <span data-ttu-id="5f175-112">Os objetos do Windows Media Format SDK fornecem uma estrutura flexível para a criação de arquivos ASF e fornecem suporte interno para os codecs de vídeo e áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5f175-112">The objects of the Windows Media Format SDK provide a flexible framework for creating ASF files, and provide built-in support for the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="5f175-113">O SDK do Media Foundation, que é novo para o Windows Vista, simplifica bastante a codificação e a decodificação fornecendo um pipeline de mídia personalizável.</span><span class="sxs-lookup"><span data-stu-id="5f175-113">The Media Foundation SDK, which is new for Windows Vista, greatly simplifies encoding and decoding by providing a customizable media pipeline.</span></span> <span data-ttu-id="5f175-114">Você pode definir as propriedades de mídia de entrada e saída e o carregador de topologia de Media Foundation configurará os codecs e DSPs necessários para você.</span><span class="sxs-lookup"><span data-stu-id="5f175-114">You can set input and output media properties and the Media Foundation topology loader will configure the necessary codecs and DSPs for you.</span></span>

<span data-ttu-id="5f175-115">O principal motivo para usar os objetos de codec diretamente é usar os codecs de áudio e vídeo do Windows Media fora do contêiner do ASF.</span><span class="sxs-lookup"><span data-stu-id="5f175-115">The primary reason for using the codec objects directly is to use the Windows Media Audio and Video codecs outside of the ASF container.</span></span> <span data-ttu-id="5f175-116">O uso dos objetos codec e DSP também fornece um nível de controle que não está disponível usando qualquer uma das tecnologias mais abstratas.</span><span class="sxs-lookup"><span data-stu-id="5f175-116">Using the codec and DSP objects also provides a level of control that is unavailable using any of the more abstracted technologies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f175-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f175-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f175-118">Codificações de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="5f175-118">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



