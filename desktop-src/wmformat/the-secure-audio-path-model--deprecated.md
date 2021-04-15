---
title: O modelo de caminho de áudio seguro (preterido)
description: O modelo de caminho de áudio seguro (preterido)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- SDK do Windows Media Format, caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- SDK do Windows Media Format, caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- Caminho de áudio seguro da Microsoft (SAP), modelo
- Caminho de áudio seguro (SAP), modelo
- SAP (caminho de áudio seguro), modelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363895"
---
# <a name="the-secure-audio-path-model-deprecated"></a><span data-ttu-id="24aef-112">O modelo de caminho de áudio seguro (preterido)</span><span class="sxs-lookup"><span data-stu-id="24aef-112">The Secure Audio Path Model (deprecated)</span></span>

<span data-ttu-id="24aef-113">Esta página documenta um recurso que terá suporte com uma solução técnica diferente em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="24aef-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="24aef-114">O Microsoft Secure áudio Path (SAP) é um recurso do Microsoft Windows® me e do Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="24aef-114">Microsoft Secure Audio Path (SAP) is a feature of Microsoft Windows® Me and Microsoft Windows XP.</span></span> <span data-ttu-id="24aef-115">O requisito de que um arquivo de áudio seja reproduzido somente por meio de um caminho de áudio seguro é especificado na licença DRM e imposto pelos componentes do cliente DRM.</span><span class="sxs-lookup"><span data-stu-id="24aef-115">The requirement that an audio file be played only through a secure audio path is specified in the DRM license and enforced by the DRM client components.</span></span> <span data-ttu-id="24aef-116">Não há criptografia extra adicional para arquivos somente SAP quando eles são protegidos inicialmente.</span><span class="sxs-lookup"><span data-stu-id="24aef-116">There is no extra encryption added for SAP-only files when they are initially protected.</span></span> <span data-ttu-id="24aef-117">A criptografia SAP é adicionada automaticamente pelos componentes DRM no momento da reprodução, assim como o processo de autenticação para todos os componentes de software envolvidos na reprodução.</span><span class="sxs-lookup"><span data-stu-id="24aef-117">The SAP encryption is added automatically by the DRM components at playback time, as is the authentication process for all software components involved in playback.</span></span> <span data-ttu-id="24aef-118">Portanto, os funcionamentos do SAP são completamente transparentes para os aplicativos, e é por isso que não há nenhum método ou propriedade no SDK do Windows Media Format para habilitar ou desabilitar o SAP.</span><span class="sxs-lookup"><span data-stu-id="24aef-118">The workings of SAP are therefore completely transparent to applications, and that is why there is no method or property in the Windows Media Format SDK for enabling or disabling SAP.</span></span> <span data-ttu-id="24aef-119">Se desejar, ao criar um arquivo protegido, um proprietário de conteúdo poderá adicionar um atributo de cabeçalho personalizado chamado algo como "DRMHeader. SAPRequired" para instruir um servidor de licença a adicionar o requisito do SAP à licença.</span><span class="sxs-lookup"><span data-stu-id="24aef-119">If desired, when creating a protected file a content owner can add a custom header attribute called something like "DRMHeader.SAPRequired" in order to instruct a license server to add the SAP requirement to the license.</span></span> <span data-ttu-id="24aef-120">A implementação desse esquema é até o proprietário do conteúdo e o serviço de licença.</span><span class="sxs-lookup"><span data-stu-id="24aef-120">The implementation of such a scheme is up to the content owner and the license service.</span></span>

<span data-ttu-id="24aef-121">No modelo DRM atual, se o SAP não for aplicado, quando música digital protegida for reproduzida, o conteúdo criptografado passará para o componente cliente DRM.</span><span class="sxs-lookup"><span data-stu-id="24aef-121">In the current DRM model, if SAP is not applied, when protected digital music is played, the encrypted content passes to the DRM client component.</span></span> <span data-ttu-id="24aef-122">O cliente DRM verifica se o aplicativo e o componente DRM que estão incorporando o SDK do Windows Media Format são válidos.</span><span class="sxs-lookup"><span data-stu-id="24aef-122">The DRM client verifies that the application and the DRM component incorporating the Windows Media Format SDK are valid.</span></span> <span data-ttu-id="24aef-123">Se eles forem válidos, o cliente DRM descriptografará o conteúdo e o enviará para o aplicativo, que o enviará para os componentes de áudio de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="24aef-123">If they are valid, the DRM client decrypts the content and sends it to the application, which then sends it to the lower-level audio components.</span></span> <span data-ttu-id="24aef-124">Neste ponto, a música descriptografada está disponível para aplicativos de modo de usuário, plug-ins e drivers de modo kernel que podem interceptar os bits de áudio descriptografados.</span><span class="sxs-lookup"><span data-stu-id="24aef-124">At this point, the decrypted music is available to user mode applications and plug-ins and kernel mode drivers that can intercept the decrypted audio bits.</span></span>

<span data-ttu-id="24aef-125">Quando o requisito de caminho de áudio seguro é aplicado, o conteúdo não é descriptografado pelo aplicativo, mas é passado em um estado criptografado para componentes de nível inferior, todos os quais foram autenticados pela Microsoft como confiáveis.</span><span class="sxs-lookup"><span data-stu-id="24aef-125">When the Secure Audio Path requirement is applied, the content is not decrypted by the application, but rather is passed in an encrypted state to lower level components, all of which have been authenticated by Microsoft as trustworthy.</span></span> <span data-ttu-id="24aef-126">Um componente de áudio confiável é aquele que não disponibiliza o conteúdo de áudio para nenhum componente do sistema, exceto outros componentes confiáveis específicos.</span><span class="sxs-lookup"><span data-stu-id="24aef-126">A trusted audio component is one that does not make the audio content available to any system component except other specific trusted components.</span></span> <span data-ttu-id="24aef-127">Dessa forma, o conteúdo digital permanece protegido até o nível do driver.</span><span class="sxs-lookup"><span data-stu-id="24aef-127">In this way, the digital content remains protected all the way down to the driver level.</span></span>

<span data-ttu-id="24aef-128">O diagrama a seguir exibe o modelo atual em comparação com o modelo de caminho de áudio seguro.</span><span class="sxs-lookup"><span data-stu-id="24aef-128">The following diagram displays the current model in comparison to the Secure Audio Path model.</span></span>

![diagrama do modelo de caminho de áudio seguro](images/sap.png)

 

 




