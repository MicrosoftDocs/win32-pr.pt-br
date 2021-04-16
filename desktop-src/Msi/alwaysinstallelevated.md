---
description: Instale um pacote de Windows Installer com privilégios elevados (sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505802"
---
# <a name="alwaysinstallelevated"></a><span data-ttu-id="81268-103">AlwaysInstallElevated</span><span class="sxs-lookup"><span data-stu-id="81268-103">AlwaysInstallElevated</span></span>

<span data-ttu-id="81268-104">Você pode usar a política AlwaysInstallElevated para instalar um pacote de Windows Installer com privilégios elevados (sistema).</span><span class="sxs-lookup"><span data-stu-id="81268-104">You can use the AlwaysInstallElevated policy to install a Windows Installer package with elevated (system) privileges.</span></span>

<span data-ttu-id="81268-105">\* \* Aviso: \* \*</span><span class="sxs-lookup"><span data-stu-id="81268-105">\*\*Warning:  \*\*</span></span>

<span data-ttu-id="81268-106">Essa opção é equivalente a conceder direitos administrativos completos, o que pode representar um grande risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="81268-106">This option is equivalent to granting full administrative rights, which can pose a massive security risk.</span></span> <span data-ttu-id="81268-107">A Microsoft não incentiva fortemente o uso dessa configuração.</span><span class="sxs-lookup"><span data-stu-id="81268-107">Microsoft strongly discourages the use of this setting.</span></span>

<span data-ttu-id="81268-108">Para instalar um pacote com privilégios elevados (sistema), defina o valor de AlwaysInstallElevated como "1" em ambas as seguintes chaves do registro:</span><span class="sxs-lookup"><span data-stu-id="81268-108">To install a package with elevated (system) privileges, set the AlwaysInstallElevated value to "1" under both of the following registry keys:</span></span>

<span data-ttu-id="81268-109">**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="81268-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="81268-110">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="81268-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="81268-111">Se o valor de AlwaysInstallElevated não estiver definido como "1" em ambas as chaves de registro anteriores, o instalador usará privilégios elevados para instalar aplicativos gerenciados e usará o nível de privilégio do usuário atual para aplicativos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="81268-111">If the AlwaysInstallElevated value is not set to "1" under both of the preceding registry keys, the installer uses elevated privileges to install managed applications and uses the current user's privilege level for unmanaged applications.</span></span>

<span data-ttu-id="81268-112">Como essa política permite que os usuários instalem aplicativos que exigem acesso a diretórios e chaves do registro para os quais o usuário pode não ter permissão para exibir ou alterar, você deve considerar se ele fornece um nível apropriado de segurança aos usuários.</span><span class="sxs-lookup"><span data-stu-id="81268-112">Because this policy permits users to install applications that require access to directories and registry keys for which the user may not have permission to view or change, you should consider whether it provides your users with an appropriate level of security.</span></span> <span data-ttu-id="81268-113">Definir essa política direciona Windows Installer para usar permissões do sistema ao instalar o aplicativo no sistema.</span><span class="sxs-lookup"><span data-stu-id="81268-113">Setting this policy directs Windows Installer to use system permissions when it installs the application on the system.</span></span> <span data-ttu-id="81268-114">Se essa política não estiver definida, os aplicativos não distribuídos pelo administrador serão instalados usando os privilégios do usuário e somente os aplicativos gerenciados terão privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="81268-114">If this policy is not set, applications not distributed by the administrator are installed using the user's privileges and only managed applications get elevated privileges.</span></span>

<span data-ttu-id="81268-115">Observe que, depois que a política por máquina para AlwaysInstallElevated estiver habilitada, qualquer usuário poderá definir sua configuração por usuário.</span><span class="sxs-lookup"><span data-stu-id="81268-115">Note that once the per-machine policy for AlwaysInstallElevated is enabled, any user can set their per-user setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="81268-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="81268-116">Remarks</span></span>

<span data-ttu-id="81268-117">Para obter informações sobre a interação dessa política com as fontes de instalação, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="81268-117">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="81268-118">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="81268-118">Data Type</span></span>

<span data-ttu-id="81268-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="81268-119">**REG\_DWORD**</span></span>

 

 



