---
title: Individualização de DRM
description: Individualização de DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- SDK do Windows Media Format, individualização de DRM
- DRM (gerenciamento de direitos digitais), individualização
- DRM (gerenciamento de direitos digitais), individualização
- individualização do DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291976"
---
# <a name="drm-individualization"></a><span data-ttu-id="8f154-107">Individualização de DRM</span><span class="sxs-lookup"><span data-stu-id="8f154-107">DRM Individualization</span></span>

<span data-ttu-id="8f154-108">Os proprietários de conteúdo protegido podem exigir que os usuários atualizem alguns dos componentes DRM (gerenciamento de direitos digitais) incluídos no Windows Media Format SDK antes de acessar seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8f154-108">Owners of protected content may require users to upgrade some of the digital rights management (DRM) components included in the Windows Media Format SDK before accessing their content.</span></span> <span data-ttu-id="8f154-109">Se um usuário aceitar a atualização, uma versão individualizada de um arquivo de segurança (única para seu computador) será baixada de um site da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8f154-109">If a user accepts the upgrade, an individualized version of a security file (one unique to their computer) will be downloaded from a Microsoft Web site.</span></span> <span data-ttu-id="8f154-110">Se o usuário recusar a atualização, não poderá acessar o conteúdo; no entanto, eles ainda poderão acessar conteúdo desprotegido e conteúdo protegido que não exija a atualização.</span><span class="sxs-lookup"><span data-stu-id="8f154-110">If the user declines the upgrade, they will not be able to access the content; however, they will still be able to access unprotected content and protected content that does not require the upgrade.</span></span> <span data-ttu-id="8f154-111">A execução de uma atualização de segurança ajuda a aumentar o nível de proteção oferecido pelo DRM.</span><span class="sxs-lookup"><span data-stu-id="8f154-111">Performing a security upgrade helps increase the level of protection offered by DRM.</span></span>

<span data-ttu-id="8f154-112">A individualização pode ser feita no momento da instalação ou quando um aplicativo encontra primeiro um arquivo ASF protegido que o exige.</span><span class="sxs-lookup"><span data-stu-id="8f154-112">Individualization can be done either at setup time or when an application first encounters a protected ASF file that requires it.</span></span> <span data-ttu-id="8f154-113">Como esse processo modifica os componentes do sistema de um usuário, o aplicativo deve notificar o usuário e obter seu consentimento informado antes de executar a atualização.</span><span class="sxs-lookup"><span data-stu-id="8f154-113">Because this process modifies a user's system components, the application must notify the user and obtain their informed consent before performing the upgrade.</span></span> <span data-ttu-id="8f154-114">O Microsoft Windows Media Player, por exemplo, mostra uma caixa de diálogo com o seguinte texto:</span><span class="sxs-lookup"><span data-stu-id="8f154-114">Microsoft Windows Media Player, for example, shows a dialog box with the following text:</span></span>

<span data-ttu-id="8f154-115">**Atualização de segurança necessária**</span><span class="sxs-lookup"><span data-stu-id="8f154-115">**Security Upgrade Required**</span></span>

<span data-ttu-id="8f154-116">**O proprietário do conteúdo protegido que você está tentando acessar requer primeiro a atualização de alguns dos componentes do Microsoft DRM (gerenciamento de direitos digitais) em seu computador.**</span><span class="sxs-lookup"><span data-stu-id="8f154-116">**The owner of the protected content you are trying to access requires you to first upgrade some of the Microsoft digital rights management (DRM) components on your computer.**</span></span>

<span data-ttu-id="8f154-117">**Clique em OK para atualizar seus componentes DRM.**</span><span class="sxs-lookup"><span data-stu-id="8f154-117">**Click OK to upgrade your DRM components.**</span></span>

<span data-ttu-id="8f154-118">**Ver**</span><span class="sxs-lookup"><span data-stu-id="8f154-118">**Details:**</span></span>

<span data-ttu-id="8f154-119">**Quando você clica em OK, um identificador exclusivo e um arquivo de segurança DRM são enviados a um serviço da Microsoft na Internet. O arquivo é substituído por uma versão personalizada que contém seu identificador exclusivo. Isso aumenta o nível de proteção fornecido pelo DRM.**</span><span class="sxs-lookup"><span data-stu-id="8f154-119">**When you click OK, a unique identifier and a DRM security file are sent to a Microsoft service on the Internet. The file is replaced with a customized version that contains your unique identifier. This increases the level of protection provided by DRM.**</span></span>

<span data-ttu-id="8f154-120">Qualquer aplicativo que dê suporte à individualização deve usar o mesmo texto ou uma palavra semelhante.</span><span class="sxs-lookup"><span data-stu-id="8f154-120">Any application that supports individualization should use the same or similar wording.</span></span> <span data-ttu-id="8f154-121">Para obter mais informações sobre a política de privacidade da Microsoft, consulte a seção [declaração de privacidade](privacy-statement.md) desta documentação.</span><span class="sxs-lookup"><span data-stu-id="8f154-121">For more information on Microsoft's Privacy Policy, see the [Privacy Statement](privacy-statement.md) section of this documentation.</span></span>

> [!Note]  
> <span data-ttu-id="8f154-122">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="8f154-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8f154-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f154-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f154-124">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="8f154-124">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="8f154-125">**Individualizando aplicativos DRM**</span><span class="sxs-lookup"><span data-stu-id="8f154-125">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> </dl>

 

 




