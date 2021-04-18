---
description: Definir o valor dessa política do sistema por máquina para &\# 0034; 1&\# 0034; impede que usuários não administrativos usem uma caixa de diálogo de procura para localizar fontes de aplicativos gerenciados armazenados em mídia, como CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752047"
---
# <a name="disablebrowse"></a><span data-ttu-id="d468b-103">DisableBrowse</span><span class="sxs-lookup"><span data-stu-id="d468b-103">DisableBrowse</span></span>

<span data-ttu-id="d468b-104">Definir o valor dessa [política de sistema](system-policy.md) por máquina como "1" impede que usuários não administrativos usem uma caixa de [diálogo de procura](browse-dialog.md) para localizar fontes de [*aplicativos gerenciados*](m-gly.md) armazenados em mídia, como CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d468b-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" prevents nonadministrative users from using a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md) stored on media, such as CD-ROM.</span></span> <span data-ttu-id="d468b-105">A caixa de combinação "usar recurso de:" para entrada direta está bloqueada e o "procurar..." o botão está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d468b-105">The "Use feature from:" combo box for direct input is locked and the "Browse..." button is disabled.</span></span> <span data-ttu-id="d468b-106">Para obter mais detalhes sobre a navegação de origem, consulte [resiliência de origem](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="d468b-106">For more details on source browsing, see [source resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="d468b-107">DisableBrowse substitui AllowLockdownBrowse e impede a navegação mesmo se AllowLockdownBrowse estiver definido.</span><span class="sxs-lookup"><span data-stu-id="d468b-107">DisableBrowse overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="d468b-108">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="d468b-108">Registry Key</span></span>

<span data-ttu-id="d468b-109">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="d468b-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="d468b-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d468b-110">Data Type</span></span>

<span data-ttu-id="d468b-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d468b-111">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="d468b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d468b-112">Remarks</span></span>

<span data-ttu-id="d468b-113">Em alguns casos com DisableBrowse definido, um usuário não administrativo ainda pode ser capaz de instalar aplicativos gerenciados de fontes na mídia rotulada corretamente.</span><span class="sxs-lookup"><span data-stu-id="d468b-113">In some cases with DisableBrowse set, a nonadministrative user may still be capable of installing managed applications from sources on correctly labeled media.</span></span> <span data-ttu-id="d468b-114">Definir a política DisableBrowse apenas desabilita a capacidade de navegar para fontes.</span><span class="sxs-lookup"><span data-stu-id="d468b-114">Setting the DisableBrowse policy only disables the capability to browse to sources.</span></span> <span data-ttu-id="d468b-115">Ele pode ser usado para impedir que um usuário não-administrativo navegue para uma nova fonte durante uma instalação, reinstalação ou reparo de instalações por demanda.</span><span class="sxs-lookup"><span data-stu-id="d468b-115">It can be used to prevent a nonadministrative user from browsing to a new source during an install-on-demand installation, reinstallation, or repair.</span></span> <span data-ttu-id="d468b-116">Se [AllowLockdownMedia](allowlockdownmedia.md) for definido, o usuário não administrativo ainda poderá instalar um aplicativo gerenciado a partir de uma mídia rotulada corretamente.</span><span class="sxs-lookup"><span data-stu-id="d468b-116">If [AllowLockdownMedia](allowlockdownmedia.md) is set, the nonadministrative user could still install a managed application from correctly labeled media.</span></span>

<span data-ttu-id="d468b-117">DisableBrowse impede que o usuário não administrativo navegue para um novo local de mídia ou qualquer outro local de origem.</span><span class="sxs-lookup"><span data-stu-id="d468b-117">DisableBrowse prevents the nonadministrative user from browsing to a new media location or any other source location.</span></span> <span data-ttu-id="d468b-118">Para obter detalhes de como proteger as fontes de mídia de aplicativos gerenciados, consulte [resiliência de origem](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="d468b-118">For details of how to secure media sources of managed applications see [Source Resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="d468b-119">Para obter informações sobre a interação dessa política com as fontes de instalação, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="d468b-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

 

 



