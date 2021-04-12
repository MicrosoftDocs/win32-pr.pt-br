---
title: Modificando os padrões de segurança de um computador
description: Modificando os padrões de segurança de um computador
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363641"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a><span data-ttu-id="53614-103">Modificando os padrões de segurança de um computador</span><span class="sxs-lookup"><span data-stu-id="53614-103">Modifying the Security Defaults for a Computer</span></span>

<span data-ttu-id="53614-104">Não é recomendável que você altere as configurações de segurança de todo o sistema, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="53614-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="53614-105">Se você estiver alterando as configurações de segurança de todo o sistema para afetar as configurações de segurança de um determinado aplicativo COM, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico.</span><span class="sxs-lookup"><span data-stu-id="53614-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="53614-106">Para obter mais informações sobre como definir a segurança de todo o processo, consulte [setting Process-Wide Security](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="53614-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="53614-107">Determinados valores no registro determinam as configurações de segurança para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="53614-107">Certain values in the registry determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="53614-108">Você pode modificar essas configurações usando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="53614-108">You can modify these settings using Dcomcnfg.exe.</span></span>

<span data-ttu-id="53614-109">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="53614-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="53614-110">Valores de registro para segurança de System-Wide</span><span class="sxs-lookup"><span data-stu-id="53614-110">Registry Values for System-Wide Security</span></span>](registry-values-for-machine-wide-security.md)
-   [<span data-ttu-id="53614-111">Definindo System-Wide segurança usando DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="53614-111">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="53614-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53614-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53614-113">Definindo a segurança de todo o processo</span><span class="sxs-lookup"><span data-stu-id="53614-113">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> <dt>

[<span data-ttu-id="53614-114">Definindo a segurança para aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="53614-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




