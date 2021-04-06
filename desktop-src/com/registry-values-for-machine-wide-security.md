---
title: Valores de registro para segurança de System-Wide
description: Valores de registro para segurança de System-Wide
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916133"
---
# <a name="registry-values-for-system-wide-security"></a><span data-ttu-id="659d8-103">Valores de registro para segurança de System-Wide</span><span class="sxs-lookup"><span data-stu-id="659d8-103">Registry Values for System-Wide Security</span></span>

<span data-ttu-id="659d8-104">Não é recomendável que você altere as configurações de segurança de todo o sistema, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="659d8-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="659d8-105">Se você estiver alterando as configurações de segurança de todo o sistema para afetar as configurações de segurança de um determinado aplicativo COM, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico.</span><span class="sxs-lookup"><span data-stu-id="659d8-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="659d8-106">Para obter mais informações sobre como definir a segurança de todo o processo, consulte [setting Process-Wide Security](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="659d8-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="659d8-107">Determinados valores no registro são usados para determinar as configurações de segurança para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="659d8-107">Certain values in the registry are used to determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="659d8-108">Você pode usar Dcomcnfg.exe para modificar essas configurações de segurança padrão para um computador.</span><span class="sxs-lookup"><span data-stu-id="659d8-108">You can use Dcomcnfg.exe to modify these default security settings for a computer.</span></span> <span data-ttu-id="659d8-109">Para obter procedimentos passo a passo que descrevem como usar Dcomcnfg.exe para essa finalidade, consulte Definindo a [segurança de System-Wide usando DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="659d8-109">For step-by-step procedures that describe how to use Dcomcnfg.exe for this purpose, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="659d8-110">Outra maneira de alterar as configurações padrão de todo o sistema é manipular valores de registro diretamente.</span><span class="sxs-lookup"><span data-stu-id="659d8-110">Another way to change default system-wide settings is to manipulate registry values directly.</span></span> <span data-ttu-id="659d8-111">No entanto, somente administradores e o sistema têm acesso total à parte do registro que contém as configurações padrão de segurança de chamada do sistema.</span><span class="sxs-lookup"><span data-stu-id="659d8-111">However, only administrators and the system have full access to the portion of the registry that contains the default system-wide call-security settings.</span></span> <span data-ttu-id="659d8-112">Todos os outros usuários têm acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="659d8-112">All other users have read-access only.</span></span>

<span data-ttu-id="659d8-113">Os valores nomeados que afetam os padrões de segurança em todo o sistema são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="659d8-113">The named values that affect system-wide security defaults are as follows:</span></span>

-   [<span data-ttu-id="659d8-114">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="659d8-114">DefaultLaunchPermission</span></span>](defaultlaunchpermission.md)
-   [<span data-ttu-id="659d8-115">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="659d8-115">DefaultAccessPermission</span></span>](defaultaccesspermission.md)
-   [<span data-ttu-id="659d8-116">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="659d8-116">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
-   [<span data-ttu-id="659d8-117">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="659d8-117">LegacyImpersonationLevel</span></span>](legacyimpersonationlevel.md)
-   [<span data-ttu-id="659d8-118">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="659d8-118">LegacySecureReferences</span></span>](legacysecurereferences.md)
-   [<span data-ttu-id="659d8-119">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="659d8-119">SRPRunningObjectChecks</span></span>](srprunningobjectchecks.md)
-   [<span data-ttu-id="659d8-120">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="659d8-120">SRPActivateAsActivatorChecks</span></span>](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a><span data-ttu-id="659d8-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="659d8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="659d8-122">Definindo Process-Wide segurança</span><span class="sxs-lookup"><span data-stu-id="659d8-122">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




