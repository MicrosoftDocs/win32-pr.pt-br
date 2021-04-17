---
title: Reutilizando configurações de fluxo
description: Reutilizando configurações de fluxo
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- fluxos, reutilizando configurações
- perfis, reutilizando configurações de fluxo
- Reutilizando configurações de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af10fd026904ccef33aba28d28e0e6a4975d3fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105813004"
---
# <a name="reusing-stream-configurations"></a><span data-ttu-id="b6ec6-106">Reutilizando configurações de fluxo</span><span class="sxs-lookup"><span data-stu-id="b6ec6-106">Reusing Stream Configurations</span></span>

<span data-ttu-id="b6ec6-107">Geralmente, há ocasiões em que você deseja reutilizar um objeto de configuração de fluxo de um perfil existente.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-107">There are often times when you want to reuse a stream configuration object from an existing profile.</span></span> <span data-ttu-id="b6ec6-108">Você pode ter perfis antigos que precisam de atualização ou pode precisar de um fluxo idêntico a um em um perfil de sistema.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-108">You may have old profiles that need updating or you may need a stream identical to one in a system profile.</span></span> <span data-ttu-id="b6ec6-109">É mais fácil reutilizar configurações de fluxo do que criar novas, e muitas vezes você pode alterar algumas configurações em uma configuração para atender às suas necessidades em vez de criar uma totalmente nova.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-109">It is easier to reuse stream configurations than to create new ones, and you can often change a few settings in a configuration to meet your needs rather than creating an entirely new one.</span></span>

<span data-ttu-id="b6ec6-110">Lembre-se de que há limitações em como você pode alterar as configurações de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-110">Be aware that there are limitations to how you can change stream configurations.</span></span> <span data-ttu-id="b6ec6-111">Se você alterar as configurações de forma errada, seu perfil poderá não aceitar o objeto de configuração de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-111">If you change settings in the wrong way, your profile may not accept the stream configuration object.</span></span> <span data-ttu-id="b6ec6-112">As configurações de fluxo incorretas são frequentemente aceitas pelo perfil, mas fazem com que o objeto do gravador rejeite o perfil.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-112">Incorrect stream configurations are frequently accepted by the profile but cause the writer object to reject the profile.</span></span> <span data-ttu-id="b6ec6-113">Esteja atento às seguintes limitações e problemas ao usar e modificar as configurações de fluxo existentes.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-113">Be aware of the following limitations and issues when using and modifying existing stream configurations.</span></span>

-   <span data-ttu-id="b6ec6-114">Nunca altere o conteúdo de um arquivo. prx para alterar as configurações de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-114">Never alter the contents of a .prx file to change stream settings.</span></span> <span data-ttu-id="b6ec6-115">Quando os perfis são salvos em cadeias de caracteres XML e gravados em um arquivo. prx, eles podem ser lidos com qualquer editor de texto.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-115">When profiles are saved to XML strings and written to a .prx file they can be read with any text editor.</span></span> <span data-ttu-id="b6ec6-116">Examinar um perfil salvo pode ajudá-lo a entender como os perfis funcionam.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-116">Looking at a saved profile can help you understand how profiles work.</span></span> <span data-ttu-id="b6ec6-117">No entanto, você nunca deve alterar um arquivo. prx de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-117">However, you should never alter a .prx file in any way.</span></span> <span data-ttu-id="b6ec6-118">Mesmo alterações aparentemente triviais podem invalidar o perfil.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-118">Even seemingly trivial changes can invalidate the profile.</span></span>
-   <span data-ttu-id="b6ec6-119">Várias versões do codec de áudio do Windows Media usam as mesmas configurações de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-119">Several versions of the Windows Media Audio codec use the same stream configurations.</span></span> <span data-ttu-id="b6ec6-120">Se você tiver um objeto de configuração de fluxo configurado como subtipo WMMEDIASUBTYPE \_ WMAudioV2, WMMEDIASUBTYPE \_ WMAUDIOV7 ou WMMEDIASUBTYPE \_ WMAudioV8, o fluxo resultante será compactado com o codec de áudio do Windows Media mais recente.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-120">If you have a stream configuration object that is configured as subtype WMMEDIASUBTYPE\_WMAudioV2, WMMEDIASUBTYPE\_WMAudioV7, or WMMEDIASUBTYPE\_WMAudioV8, the resulting stream will be compressed with the latest Windows Media Audio codec.</span></span> <span data-ttu-id="b6ec6-121">No entanto, você deve avaliar suas necessidades antes de usar um codec de áudio existente.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-121">However, you should evaluate your needs before using an existing audio codec.</span></span> <span data-ttu-id="b6ec6-122">Muitos tipos de arquivos podem ser aprimorados Atualizando para a versão mais recente do codec do Windows Media Audio Professional ou o codec de áudio do Windows Media Lossless.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-122">Many types of files can be improved by upgrading to the latest version of the Windows Media Audio Professional codec, or the Windows Media Audio Lossless codec.</span></span>
-   <span data-ttu-id="b6ec6-123">Nunca altere o subtipo de um fluxo para atualizar para um novo codec.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-123">Never change the subtype of a stream to upgrade to a new codec.</span></span> <span data-ttu-id="b6ec6-124">Quando você usa os métodos de [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) para obter uma configuração de fluxo, o codec anexa alguns dados a ele que identifica o formato de fluxo de bits.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-124">When you use the methods of [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) to obtain a stream configuration, the codec attaches some data to it that identifies the bit stream format.</span></span> <span data-ttu-id="b6ec6-125">Se você alterar o subtipo de um objeto de configuração de fluxo existente, o subtipo não corresponderá aos dados do codec.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-125">If you change the subtype of an existing stream configuration object, the subtype will not match the codec data.</span></span> <span data-ttu-id="b6ec6-126">Um perfil com essa configuração de fluxo não será aceito pelo objeto do gravador.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-126">A profile with such a stream configuration will not be accepted by the writer object.</span></span>
-   <span data-ttu-id="b6ec6-127">Não altere as configurações de configurações de fluxo de áudio compactado.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-127">Do not alter the settings of compressed audio stream configurations.</span></span> <span data-ttu-id="b6ec6-128">Se as configurações de um fluxo de áudio não atenderem às suas necessidades, obtenha uma nova configuração de fluxo do codec usando os métodos de **IWMCodecInfo3**.</span><span class="sxs-lookup"><span data-stu-id="b6ec6-128">If the settings of an audio stream do not suit your needs, obtain a new stream configuration from the codec using the methods of **IWMCodecInfo3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6ec6-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6ec6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6ec6-130">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="b6ec6-130">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="b6ec6-131">**Obtendo informações de configuração de fluxo de codecs**</span><span class="sxs-lookup"><span data-stu-id="b6ec6-131">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




