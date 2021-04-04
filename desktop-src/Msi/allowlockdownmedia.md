---
description: Definir o valor dessa política do sistema por máquina para &\# 0034; 1&\# 0034;, permite que usuários não administrativos instalem aplicativos gerenciados de fontes armazenadas em mídia, como um CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837682"
---
# <a name="allowlockdownmedia"></a><span data-ttu-id="2e60b-103">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="2e60b-103">AllowLockdownMedia</span></span>

<span data-ttu-id="2e60b-104">Definir o valor dessa [política de sistema](system-policy.md) por máquina como "1" permite que usuários não administrativos instalem [*aplicativos gerenciados*](m-gly.md) de fontes armazenadas em mídia, como um CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="2e60b-104">Setting the value of this per-machine [system policy](system-policy.md) to "1", enables nonadministrative users to install [*managed applications*](m-gly.md) from sources stored on media, such as a CD-ROM.</span></span> <span data-ttu-id="2e60b-105">Consulte [resiliência da origem](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="2e60b-105">See [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="2e60b-106">Por exemplo, se essa política estiver definida, um usuário não administrativo poderá usar uma fonte de mídia para instalar aplicativos atribuídos ou publicados ou aplicativos que estão sendo instalados para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="2e60b-106">For example, if this policy is set, a nonadministrative user may use a media source to install assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="2e60b-107">Definir essa política também permite que usuários não administrativos executem programas em privilégios LocalSystem durante uma instalação elevada.</span><span class="sxs-lookup"><span data-stu-id="2e60b-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="2e60b-108">O valor padrão dessa política é 1 somente em computadores que executam o Windows Vista e que não fazem parte de um domínio.</span><span class="sxs-lookup"><span data-stu-id="2e60b-108">The default value of this policy is 1 only on computers running Windows Vista and that are not joined to a domain.</span></span> <span data-ttu-id="2e60b-109">O padrão em outros computadores é que usuários não-administrativos não podem instalar aplicativos gerenciados de uma origem localizada na mídia.</span><span class="sxs-lookup"><span data-stu-id="2e60b-109">The default on other computers is that nonadministrative users cannot install managed applications from a source located on media.</span></span>

<span data-ttu-id="2e60b-110">Como essa política permite que os usuários que não são administradores instalem com privilégios que eles não têm, por padrão, antes de definir essa política, você deve considerar se ele fornece um nível apropriado de segurança para o usuário.</span><span class="sxs-lookup"><span data-stu-id="2e60b-110">Because this policy enables users that are not an administrator to install with privileges they do not have by default, before setting this policy you should consider whether it provides an appropriate level of security for your user.</span></span> <span data-ttu-id="2e60b-111">A configuração padrão é recomendada para garantir um ambiente seguro.</span><span class="sxs-lookup"><span data-stu-id="2e60b-111">The default setting is recommended to ensure a secure environment.</span></span>

<span data-ttu-id="2e60b-112">Para obter mais informações sobre como proteger instalações e usar certificados digitais, consulte [diretrizes para criar instalações seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md) e [baixar uma instalação da Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="2e60b-112">For more information about securing installations and using digital certificates see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="2e60b-113">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="2e60b-113">Registry Key</span></span>

<span data-ttu-id="2e60b-114">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="2e60b-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="2e60b-115">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="2e60b-115">Data Type</span></span>

<span data-ttu-id="2e60b-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2e60b-116">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="2e60b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e60b-117">Remarks</span></span>

<span data-ttu-id="2e60b-118">Definir essa política também permite que usuários não administrativos executem programas arbitrários em privilégios LocalSystem se tiverem um pacote Windows Installer que instala ou inicia esses programas.</span><span class="sxs-lookup"><span data-stu-id="2e60b-118">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e60b-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e60b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e60b-120">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="2e60b-120">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="2e60b-121">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="2e60b-121">AllowLockdownBrowse</span></span>](allowlockdownbrowse.md)
</dt> </dl>

 

 



