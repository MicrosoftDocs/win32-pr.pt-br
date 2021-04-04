---
title: Individualizando aplicativos DRM
description: Individualizando aplicativos DRM
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- SDK do Windows Media Format, individualizando aplicativos DRM
- Windows Media Format SDK, individualização de aplicativos
- ASF (Advanced Systems Format), individualizando aplicativos DRM
- ASF (formato de sistemas avançados), individualizando aplicativos DRM
- Formato de sistema avançado (ASF), individualização de aplicativo
- ASF (formato de sistemas avançados), individualização de aplicativos
- DRM (gerenciamento de direitos digitais), individualizando aplicativos
- DRM (gerenciamento de direitos digitais), individualizando aplicativos
- DRM (gerenciamento de direitos digitais), individualização de aplicativos
- DRM (gerenciamento de direitos digitais), individualização de aplicativos
- individualização do aplicativo
- individualizando aplicativos DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103917060"
---
# <a name="individualizing-drm-applications"></a><span data-ttu-id="655ad-115">Individualizando aplicativos DRM</span><span class="sxs-lookup"><span data-stu-id="655ad-115">Individualizing DRM Applications</span></span>

<span data-ttu-id="655ad-116">Para aumentar a segurança, o componente DRM dos aplicativos pode ser *individualizado*.</span><span class="sxs-lookup"><span data-stu-id="655ad-116">To increase security, the DRM component of applications can be *individualized*.</span></span> <span data-ttu-id="655ad-117">Um aplicativo individual é aquele que recebeu uma atualização para seus componentes DRM que o diferencia de todas as outras cópias do mesmo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="655ad-117">An individualized application is one that has received an upgrade to its DRM components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="655ad-118">Os proprietários de conteúdo podem exigir que seus arquivos protegidos sejam reproduzidos somente em um aplicativo que tenha sido individualizado.</span><span class="sxs-lookup"><span data-stu-id="655ad-118">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

<span data-ttu-id="655ad-119">O processo de individualização é iniciado quando o aplicativo entra em contato com o serviço de individualização da Microsoft, que instala uma atualização de segurança no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="655ad-119">The individualization process starts when the application contacts the Microsoft Individualization Service, which then installs a security upgrade on the user's computer.</span></span> <span data-ttu-id="655ad-120">Como o serviço de individualização manipula informações do usuário, você deve exibir a política de privacidade da Microsoft ou fornecer um link para essa página no site da Microsoft: <https://privacy.microsoft.com/privacystatement> .</span><span class="sxs-lookup"><span data-stu-id="655ad-120">Because the Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft Web site: <https://privacy.microsoft.com/privacystatement>.</span></span>

<span data-ttu-id="655ad-121">A individualização pode ser realizada de maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="655ad-121">Individualization can be accomplished in different ways.</span></span> <span data-ttu-id="655ad-122">Por exemplo, a individualização pode ocorrer quando um usuário reproduz um arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="655ad-122">For example, individualization can take place when a user plays a protected file.</span></span> <span data-ttu-id="655ad-123">A solicitação de licença é enviada para o [*serviço de licença do Windows Media*](wmformat-glossary.md), que inspeciona o certificado do aplicativo que está solicitando a [*licença*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="655ad-123">The license request is sent to the [*Windows Media License Service*](wmformat-glossary.md), which inspects the certificate of the application requesting the [*license*](wmformat-glossary.md).</span></span> <span data-ttu-id="655ad-124">Se o componente DRM do aplicativo não tiver sido individualizado, o serviço de licença do Windows Media se recusará a emitir a licença, pois é a política do serviço de licença do Windows Media para emitir licenças somente para jogadores individualizados.</span><span class="sxs-lookup"><span data-stu-id="655ad-124">If the DRM component of the application has not been individualized, Windows Media License Service refuses to issue the license, because it is the policy of Windows Media License Service to issue licenses only to individualized players.</span></span> <span data-ttu-id="655ad-125">Em seguida, o aplicativo pode notificar o usuário de que o aplicativo deve ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="655ad-125">The application can then notify the user that the application must be upgraded.</span></span> <span data-ttu-id="655ad-126">Se o usuário concordar, uma atualização de segurança será fornecida para individualizar o componente DRM do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="655ad-126">If the user agrees, a security upgrade is provided to individualize the DRM component of the application.</span></span>

<span data-ttu-id="655ad-127">Para uma melhor experiência do usuário, você pode iniciar o processo de individualização como uma etapa de atualização de segurança durante a instalação; em seguida, o usuário não é interrompido para obter uma atualização de segurança ao tentar reproduzir um arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="655ad-127">For a better user experience, you can initiate the individualization process as a security upgrade step during setup; then the user is not interrupted to get a security upgrade while trying to play a protected file.</span></span> <span data-ttu-id="655ad-128">Você também pode incentivar a individualização de forma ativa adicionando um comando de menu de **atualização de segurança** ou um botão ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="655ad-128">You can also actively encourage individualization by adding a **Security Upgrade** menu command or button to the application.</span></span>

> [!Note]  
> <span data-ttu-id="655ad-129">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="655ad-129">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="655ad-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="655ad-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="655ad-131">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="655ad-131">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="655ad-132">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="655ad-132">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




