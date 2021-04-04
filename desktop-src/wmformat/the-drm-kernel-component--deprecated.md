---
title: O componente de kernel do DRM (preterido)
description: O componente de kernel do DRM (preterido)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- SDK do Windows Media Format, caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- SDK do Windows Media Format, caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- SDK do Windows Media Format, componente do kernel do DRM
- DRM (gerenciamento de direitos digitais), componente de kernel
- DRM (gerenciamento de direitos digitais), componente de kernel
- Caminho de áudio seguro da Microsoft (SAP), componente de kernel do DRM
- Caminho de áudio seguro (SAP), componente de kernel do DRM
- SAP (caminho de áudio seguro), componente de kernel do DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008580"
---
# <a name="the-drm-kernel-component-deprecated"></a><span data-ttu-id="60048-115">O componente de kernel do DRM (preterido)</span><span class="sxs-lookup"><span data-stu-id="60048-115">The DRM Kernel Component (deprecated)</span></span>

<span data-ttu-id="60048-116">Esta página documenta um recurso que terá suporte com uma solução técnica diferente em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="60048-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="60048-117">No modelo de caminho de áudio seguro da Microsoft (SAP), o componente de kernel do DRM fornece dois recursos básicos que protegem a integridade de músicas criptografadas.</span><span class="sxs-lookup"><span data-stu-id="60048-117">In the Microsoft Secure Audio Path (SAP) model, the DRM kernel component provides two basic features that protect the integrity of encrypted music.</span></span>

<span data-ttu-id="60048-118">Primeiro, o componente de cliente DRM e o componente de kernel DRM estão em comunicação quando um arquivo de música é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="60048-118">First, the DRM client component and the DRM kernel component are in communication when a music file is played.</span></span> <span data-ttu-id="60048-119">Essa comunicação entre os componentes impede que alguém viole o sinal criptografado ou insira informações falsas.</span><span class="sxs-lookup"><span data-stu-id="60048-119">This communication between components prevents anyone from tampering with the encrypted signal or from inserting false information.</span></span>

<span data-ttu-id="60048-120">Em segundo lugar, o componente do kernel do DRM não descriptografa o sinal de música até que todos os componentes restantes sejam autenticados.</span><span class="sxs-lookup"><span data-stu-id="60048-120">Second, the DRM kernel component does not decrypt the music signal until all remaining components are authenticated.</span></span> <span data-ttu-id="60048-121">Ou seja, antes de descriptografar o conteúdo e passá-lo para o próximo componente do sistema, o componente do kernel DRM verifica cada componente que permanece no caminho para a placa de som (cada componente que pode acessar o conteúdo) e verifica se esses componentes estão assinados com um certificado da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="60048-121">That is, before decrypting content and passing it to the next system component, the DRM kernel component checks each component that remains in the path to the sound card (each component that can access the content) and verifies that these components are signed with a certificate from Microsoft.</span></span> <span data-ttu-id="60048-122">Um componente não assinado pode indicar um componente suspeito ou um driver mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="60048-122">An unsigned component might indicate a suspicious component or a malicious driver.</span></span> <span data-ttu-id="60048-123">Assim, quando o componente de kernel DRM valida os componentes restantes, se algum componente falhar nesse teste, o sinal será interrompido e não poderá ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="60048-123">So, when the DRM kernel component validates remaining components, if any component fails this test, the signal is halted and cannot be played.</span></span> <span data-ttu-id="60048-124">Caso contrário, se todos os componentes passarem na validação, o componente do kernel DRM descriptografará a música e a passará para o próximo componente.</span><span class="sxs-lookup"><span data-stu-id="60048-124">Otherwise, if all components pass validation, the DRM kernel component decrypts the music and passes it to the next component.</span></span>

<span data-ttu-id="60048-125">A Microsoft assina digitalmente os drivers que passam os testes do WHQL (laboratório de qualidade de hardware) do Windows® para garantir que os usuários estejam usando os drivers de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="60048-125">Microsoft digitally signs drivers that pass the Windows® Hardware Quality Lab (WHQL) tests to assure users that they are using the highest-quality drivers.</span></span> <span data-ttu-id="60048-126">Essa prática é padrão e garante a autenticidade dos componentes, pois a assinatura não pode ser forjada, nem o código pode ser modificado sem destruir a assinatura.</span><span class="sxs-lookup"><span data-stu-id="60048-126">This practice is standard and guarantees the authenticity of components because the signature cannot be forged, nor can the code be modified without destroying the signature.</span></span> <span data-ttu-id="60048-127">Os drivers que são certificados para o caminho de áudio seguro devem proteger os dados de áudio que eles processam do acesso por componentes não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="60048-127">Drivers that are certified for Secure Audio Path must protect the audio data they process from access by untrusted components.</span></span> 

<span data-ttu-id="60048-128">Os drivers incluídos no Windows Millennium Edition e no Windows XP são atualizados para um caminho de áudio seguro e assinados.</span><span class="sxs-lookup"><span data-stu-id="60048-128">Drivers included with Windows Millennium Edition and Windows XP are updated for Secure Audio Path and signed.</span></span> <span data-ttu-id="60048-129">Os drivers que não estão assinados para uso com o Windows me ou o Windows XP não podem reproduzir música protegida.</span><span class="sxs-lookup"><span data-stu-id="60048-129">Drivers that are not signed for use with Windows Me or Windows XP cannot play protected music.</span></span> <span data-ttu-id="60048-130">Os fabricantes de driver podem reemitir versões atualizadas de seus drivers assinados pelo WHQL e publicá-las na Internet para que os consumidores baixem.</span><span class="sxs-lookup"><span data-stu-id="60048-130">Driver manufacturers can reissue updated versions of their drivers that are signed by WHQL, and publish them on the Internet for consumers to download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60048-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60048-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60048-132">**Caminho de áudio seguro da Microsoft**</span><span class="sxs-lookup"><span data-stu-id="60048-132">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




