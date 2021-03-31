---
title: Definindo a segurança para aplicativos COM
description: Definindo a segurança para aplicativos COM
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823069"
---
# <a name="setting-security-for-com-applications"></a><span data-ttu-id="154c7-103">Definindo a segurança para aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="154c7-103">Setting Security for COM Applications</span></span>

<span data-ttu-id="154c7-104">Há várias maneiras pelas quais você pode ajudar a controlar a segurança para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="154c7-104">There are several ways you can help control security for your applications.</span></span> <span data-ttu-id="154c7-105">Você pode alterar as configurações de segurança padrão de um computador, que são usadas por todos os aplicativos no computador que não fornecem seus próprios valores de segurança.</span><span class="sxs-lookup"><span data-stu-id="154c7-105">You can change a computer's default security settings, which are used by all applications on the computer that do not supply their own security values.</span></span> <span data-ttu-id="154c7-106">Você pode definir a segurança para um processo específico, usando Dcomcnfg.exe ou ao chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="154c7-106">You can set security for a particular process, either by using Dcomcnfg.exe or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="154c7-107">Você também pode controlar de forma programática as configurações de segurança no nível de proxy da interface.</span><span class="sxs-lookup"><span data-stu-id="154c7-107">You can also programmatically control security settings at the interface proxy level.</span></span>

<span data-ttu-id="154c7-108">Os tópicos a seguir fornecem procedimentos que explicam como definir a segurança:</span><span class="sxs-lookup"><span data-stu-id="154c7-108">The following topics provide procedures that explain how to set security:</span></span>

-   [<span data-ttu-id="154c7-109">Modificando os padrões de segurança de um computador</span><span class="sxs-lookup"><span data-stu-id="154c7-109">Modifying the Security Defaults for a Computer</span></span>](modifying-the-security-defaults-for-a-computer.md)
-   [<span data-ttu-id="154c7-110">Definindo Process-Wide segurança</span><span class="sxs-lookup"><span data-stu-id="154c7-110">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
-   [<span data-ttu-id="154c7-111">Definindo a segurança no nível de proxy da interface</span><span class="sxs-lookup"><span data-stu-id="154c7-111">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a><span data-ttu-id="154c7-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="154c7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="154c7-113">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="154c7-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




