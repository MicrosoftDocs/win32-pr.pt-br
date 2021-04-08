---
description: Definir o valor dessa política do sistema por máquina para &\# 0034; 1&\# 0034; permite que usuários não administrativos usem uma caixa de diálogo de navegação para localizar fontes de aplicativos gerenciados.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828079"
---
# <a name="allowlockdownbrowse"></a><span data-ttu-id="c6a73-103">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="c6a73-103">AllowLockdownBrowse</span></span>

<span data-ttu-id="c6a73-104">Definir o valor dessa [política do sistema](system-policy.md) por máquina como "1" permite que usuários não administrativos usem uma caixa de [diálogo de procura](browse-dialog.md) para localizar fontes de [*aplicativos gerenciados*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c6a73-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" enables nonadministrative users to use a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md).</span></span> <span data-ttu-id="c6a73-105">As fontes podem incluir mídia, como CD-ROM, URLs e locais de rede.</span><span class="sxs-lookup"><span data-stu-id="c6a73-105">Sources may include media, such as CD-ROM, URLs, and network locations.</span></span> <span data-ttu-id="c6a73-106">Para obter mais informações, consulte [resiliência de origem](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="c6a73-106">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="c6a73-107">O padrão em Windows Installer é que usuários não administrativos não podem procurar novas fontes de aplicativos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="c6a73-107">The default on Windows Installer is that nonadministrative users cannot browse for new sources of managed applications.</span></span> <span data-ttu-id="c6a73-108">As únicas fontes disponíveis são aquelas que já estão registradas na lista de origem do produto.</span><span class="sxs-lookup"><span data-stu-id="c6a73-108">The only sources available are those that are already registered in the source list of the product.</span></span> <span data-ttu-id="c6a73-109">Se essa política estiver definida, um usuário não administrativo poderá procurar novas fontes de aplicativos atribuídos ou publicados ou aplicativos que estão sendo instalados para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="c6a73-109">If this policy is set, a nonadministrative user may browse for new sources of assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="c6a73-110">A definição de AllowLockdownBrowse também permite que usuários não administrativos executem programas em privilégios LocalSystem durante uma instalação elevada.</span><span class="sxs-lookup"><span data-stu-id="c6a73-110">Setting AllowLockdownBrowse also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="c6a73-111">A configuração padrão é recomendada para garantir um ambiente seguro.</span><span class="sxs-lookup"><span data-stu-id="c6a73-111">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="c6a73-112">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="c6a73-112">Registry Key</span></span>

<span data-ttu-id="c6a73-113">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="c6a73-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="c6a73-114">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="c6a73-114">Data Type</span></span>

<span data-ttu-id="c6a73-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c6a73-115">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a73-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6a73-116">Remarks</span></span>

<span data-ttu-id="c6a73-117">Definir essa política também permite que usuários não administrativos executem programas arbitrários em privilégios LocalSystem se tiverem um pacote Windows Installer que instala ou inicia esses programas.</span><span class="sxs-lookup"><span data-stu-id="c6a73-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

<span data-ttu-id="c6a73-118">[DisableBrowse](disablebrowse.md) substitui AllowLockdownBrowse e impede a navegação mesmo se AllowLockdownBrowse estiver definido.</span><span class="sxs-lookup"><span data-stu-id="c6a73-118">[DisableBrowse](disablebrowse.md) overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

<span data-ttu-id="c6a73-119">Para obter informações sobre a interação dessa política com as fontes de instalação, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="c6a73-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6a73-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6a73-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6a73-121">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="c6a73-121">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="c6a73-122">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="c6a73-122">AllowLockdownMedia</span></span>](allowlockdownmedia.md)
</dt> </dl>

 

 



