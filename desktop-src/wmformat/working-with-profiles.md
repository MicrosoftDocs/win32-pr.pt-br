---
title: Trabalhando com perfis
description: Trabalhando com perfis
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- SDK do Windows Media Format, perfis
- SDK do Windows Media Format, interface IWMCodecInfo3
- perfis, sobre
- perfis, Windows Media Format SDK
- perfis, IWMCodecInfo3
- IWMCodecInfo3, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664bbafd6c628588aa3b45b0a62a216db7bd7749
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365565"
---
# <a name="working-with-profiles"></a><span data-ttu-id="297c2-109">Trabalhando com perfis</span><span class="sxs-lookup"><span data-stu-id="297c2-109">Working with Profiles</span></span>

<span data-ttu-id="297c2-110">Esta seção descreve como criar, criar e modificar perfis.</span><span class="sxs-lookup"><span data-stu-id="297c2-110">This section describes how to design, create, and modify profiles.</span></span> <span data-ttu-id="297c2-111">Cada perfil descreve os fluxos que criarão um arquivo e suas relações entre si.</span><span class="sxs-lookup"><span data-stu-id="297c2-111">Each profile describes the streams that will make up a file and their relationships with each other.</span></span> <span data-ttu-id="297c2-112">Um objeto de perfil contém informações de configuração de fluxo para cada fluxo, informações de exclusão mútua para fluxos que não podem ser entregues simultaneamente, informações de compartilhamento de largura de banda e informações de priorização de fluxo.</span><span class="sxs-lookup"><span data-stu-id="297c2-112">A profile object contains stream configuration information for each stream, mutual exclusion information for streams that cannot be delivered simultaneously, bandwidth sharing information, and stream prioritization information.</span></span>

<span data-ttu-id="297c2-113">A principal finalidade dos perfis é fornecer informações de configuração de fluxo para o objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="297c2-113">The main purpose of profiles is to provide stream configuration information to the writer object.</span></span> <span data-ttu-id="297c2-114">O gravador usa as informações em um perfil para coordenar com os codecs o processo de compactação de entradas.</span><span class="sxs-lookup"><span data-stu-id="297c2-114">The writer uses the information in a profile to coordinate with the codecs the process of compressing inputs.</span></span> <span data-ttu-id="297c2-115">Ao configurar um fluxo de mídia compactado, você especifica o codec usado para compactar os dados e as configurações que o codec usa.</span><span class="sxs-lookup"><span data-stu-id="297c2-115">When you configure a compressed media stream, you specify the codec used to compress the data and the settings the codec uses.</span></span> <span data-ttu-id="297c2-116">Você também pode criar perfis para fluxos não compactados.</span><span class="sxs-lookup"><span data-stu-id="297c2-116">You can also create profiles for uncompressed streams.</span></span> <span data-ttu-id="297c2-117">Há suporte para vários tipos de fluxo não compactados.</span><span class="sxs-lookup"><span data-stu-id="297c2-117">Several uncompressed stream types are supported.</span></span> <span data-ttu-id="297c2-118">Embora não exijam um codec, esses tipos têm seus próprios requisitos para a configuração de fluxo.</span><span class="sxs-lookup"><span data-stu-id="297c2-118">Even though they do not require a codec, these types have their own requirements for stream configuration.</span></span> <span data-ttu-id="297c2-119">Para obter mais informações, consulte [Configurando fluxos](configuring-streams.md) e [usando fluxos de áudio e vídeo não compactados](using-uncompressed-audio-and-video-streams.md).</span><span class="sxs-lookup"><span data-stu-id="297c2-119">For more information, see [Configuring Streams](configuring-streams.md) and [Using Uncompressed Audio and Video Streams](using-uncompressed-audio-and-video-streams.md).</span></span>

<span data-ttu-id="297c2-120">As informações de configuração de fluxo para um fluxo usando um dos codecs de mídia do Windows devem ser obtidas do codec usando os métodos da interface [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) .</span><span class="sxs-lookup"><span data-stu-id="297c2-120">Stream configuration information for a stream using one of the Windows Media codecs must be obtained from the codec by using the methods of the [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interface.</span></span> <span data-ttu-id="297c2-121">O procedimento para usar formatos de fluxo é diferente para codecs de vídeo do que para codecs de áudio, mas em ambos os casos, você deve começar obtendo o formato do codec.</span><span class="sxs-lookup"><span data-stu-id="297c2-121">The procedure for using stream formats is different for video codecs than it is for audio codecs, but in both cases you must begin by obtaining the format from the codec.</span></span> <span data-ttu-id="297c2-122">Você nunca deve tentar configurar manualmente um fluxo usando um dos codecs de mídia do Windows, porque pequenos erros no perfil podem ter um efeito profundo no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="297c2-122">You should never try to manually configure a stream using one of the Windows Media codecs, because small errors in the profile can have a profound effect on the ASF file.</span></span>

<span data-ttu-id="297c2-123">As etapas básicas na criação e/ou modificação de perfis são:</span><span class="sxs-lookup"><span data-stu-id="297c2-123">The basic steps in creating and/or modifying profiles are:</span></span>

1.  <span data-ttu-id="297c2-124">Crie um perfil vazio ou carregue um perfil existente para editar.</span><span class="sxs-lookup"><span data-stu-id="297c2-124">Create an empty profile, or load an existing profile to edit.</span></span>
2.  <span data-ttu-id="297c2-125">Configure cada um dos fluxos, se necessário, com base nos dados de perfil com suporte recuperados do codec que serão usados para codificar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="297c2-125">Configure each of the streams, if required, based on supported profile data retrieved from the codec that will be used to encode the stream.</span></span>
3.  <span data-ttu-id="297c2-126">Configure a exclusão mútua, se necessário.</span><span class="sxs-lookup"><span data-stu-id="297c2-126">Configure mutual exclusion, if needed.</span></span>
4.  <span data-ttu-id="297c2-127">Configure o compartilhamento de largura de banda, se necessário.</span><span class="sxs-lookup"><span data-stu-id="297c2-127">Configure bandwidth sharing, if needed.</span></span>
5.  <span data-ttu-id="297c2-128">Defina a prioridade dos fluxos no arquivo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="297c2-128">Set the priority of the streams in the file, if required.</span></span>

<span data-ttu-id="297c2-129">As seções a seguir explicam o processo de criação e edição de perfis.</span><span class="sxs-lookup"><span data-stu-id="297c2-129">The following sections explain the process of creating and editing profiles.</span></span>



| <span data-ttu-id="297c2-130">Seção</span><span class="sxs-lookup"><span data-stu-id="297c2-130">Section</span></span>                                                        | <span data-ttu-id="297c2-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="297c2-131">Description</span></span>                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="297c2-132">Criando perfis</span><span class="sxs-lookup"><span data-stu-id="297c2-132">Designing Profiles</span></span>](designing-profiles.md)                   | <span data-ttu-id="297c2-133">Descreve como criar um perfil.</span><span class="sxs-lookup"><span data-stu-id="297c2-133">Describes how to design a profile.</span></span>                                                                 |
| [<span data-ttu-id="297c2-134">Criando perfis</span><span class="sxs-lookup"><span data-stu-id="297c2-134">Creating Profiles</span></span>](creating-profiles.md)                     | <span data-ttu-id="297c2-135">Descreve como criar um perfil vazio.</span><span class="sxs-lookup"><span data-stu-id="297c2-135">Describes how to create an empty profile.</span></span>                                                          |
| [<span data-ttu-id="297c2-136">Configurando fluxos</span><span class="sxs-lookup"><span data-stu-id="297c2-136">Configuring Streams</span></span>](configuring-streams.md)                 | <span data-ttu-id="297c2-137">Descreve como configurar fluxos e incluí-los em um perfil.</span><span class="sxs-lookup"><span data-stu-id="297c2-137">Describes how to configure streams and include them in a profile.</span></span>                                  |
| [<span data-ttu-id="297c2-138">Usando a exclusão mútua</span><span class="sxs-lookup"><span data-stu-id="297c2-138">Using Mutual Exclusion</span></span>](using-mutual-exclusion.md)           | <span data-ttu-id="297c2-139">Descreve como criar objetos de exclusão mútua e incluí-los em um perfil.</span><span class="sxs-lookup"><span data-stu-id="297c2-139">Describes how to create mutual exclusion objects and include them in a profile.</span></span>                    |
| [<span data-ttu-id="297c2-140">Usando o compartilhamento de largura de banda</span><span class="sxs-lookup"><span data-stu-id="297c2-140">Using Bandwidth Sharing</span></span>](using-bandwidth-sharing.md)         | <span data-ttu-id="297c2-141">Descreve como usar o compartilhamento de largura de banda em um perfil.</span><span class="sxs-lookup"><span data-stu-id="297c2-141">Describes how to use bandwidth sharing in a profile.</span></span>                                               |
| [<span data-ttu-id="297c2-142">Usando a priorização de fluxo</span><span class="sxs-lookup"><span data-stu-id="297c2-142">Using Stream Prioritization</span></span>](using-stream-prioritization.md) | <span data-ttu-id="297c2-143">Descreve como usar a priorização de fluxo em um perfil.</span><span class="sxs-lookup"><span data-stu-id="297c2-143">Describes how to use stream prioritization in a profile.</span></span>                                           |
| [<span data-ttu-id="297c2-144">Salvando perfis</span><span class="sxs-lookup"><span data-stu-id="297c2-144">Saving Profiles</span></span>](saving-profiles.md)                         | <span data-ttu-id="297c2-145">Descreve como salvar seus perfis personalizados em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="297c2-145">Describes how to save your custom profiles to a file.</span></span>                                              |
| [<span data-ttu-id="297c2-146">Usando perfis de sistema</span><span class="sxs-lookup"><span data-stu-id="297c2-146">Using System Profiles</span></span>](using-system-profiles.md)             | <span data-ttu-id="297c2-147">Descreve como trabalhar com perfis de sistema para economizar tempo e esforço na criação de perfis.</span><span class="sxs-lookup"><span data-stu-id="297c2-147">Describes how to work with system profiles to save time and effort in creating profiles.</span></span>           |
| [<span data-ttu-id="297c2-148">Gerenciamento do tamanho do pacote</span><span class="sxs-lookup"><span data-stu-id="297c2-148">Managing Packet Size</span></span>](managing-packet-size.md)               | <span data-ttu-id="297c2-149">Discute como controlar o tamanho dos pacotes nos fluxos de dados de arquivos feitos usando seu perfil.</span><span class="sxs-lookup"><span data-stu-id="297c2-149">Discusses how to control the size of packets in the data streams of files made using your profile.</span></span> |



 

<span data-ttu-id="297c2-150">**Observação** Os usuários de versões anteriores do Windows Media Format SDK podem estar acostumados a usar perfis de sistema sem modificação para criar seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="297c2-150">**Note** Users of previous versions of the Windows Media Format SDK may be accustomed to using system profiles without modification to create their files.</span></span> <span data-ttu-id="297c2-151">O SDK do Windows Media Format 9 Series ou posterior não inclui nenhum novo perfil de sistema que use os codecs do Windows Media 9 Series ou posteriores.</span><span class="sxs-lookup"><span data-stu-id="297c2-151">The Windows Media Format 9 Series SDK or later does not include any new system profiles that use the Windows Media 9 Series or later codecs.</span></span> <span data-ttu-id="297c2-152">Isso ocorre devido ao número crescente de perfis que seriam necessários para abordar os vários recursos agora oferecidos pelos codecs.</span><span class="sxs-lookup"><span data-stu-id="297c2-152">This is because of the increasing number of profiles that would be needed to cover the various features now offered by the codecs.</span></span> <span data-ttu-id="297c2-153">Você ainda pode usar os perfis de sistema da versão 8 como um local inicial para seus perfis.</span><span class="sxs-lookup"><span data-stu-id="297c2-153">You can still use the version 8 system profiles as a starting place for your profiles.</span></span> <span data-ttu-id="297c2-154">Para obter mais informações, consulte [usando perfis de sistema](using-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="297c2-154">For more information see [Using System Profiles](using-system-profiles.md).</span></span> <span data-ttu-id="297c2-155">Para obter informações sobre o novo mecanismo de direcionamento de perfis para dispositivos de entrega específicos, consulte [trabalhando com modelos de conformidade do dispositivo](working-with-device-conformance-templates.md).</span><span class="sxs-lookup"><span data-stu-id="297c2-155">For information about the new mechanism for targeting profiles to specific delivery devices, see [Working with Device Conformance Templates](working-with-device-conformance-templates.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="297c2-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="297c2-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="297c2-157">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="297c2-157">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="297c2-158">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="297c2-158">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




