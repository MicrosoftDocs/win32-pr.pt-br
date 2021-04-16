---
title: LegacySecureReferences
description: Determina se invocações AddRef/Release são protegidas para aplicativos que não chamam CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- COM valor do registro LegacySecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105782628"
---
# <a name="legacysecurereferences"></a><span data-ttu-id="507d8-104">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="507d8-104">LegacySecureReferences</span></span>

<span data-ttu-id="507d8-105">Determina se as / invocações de **versão** AddRef são protegidas para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="507d8-105">Determines whether **AddRef**/**Release** invocations are secured for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="507d8-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="507d8-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a><span data-ttu-id="507d8-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="507d8-107">Remarks</span></span>

<span data-ttu-id="507d8-108">Este é um valor de **\_ sz do reg** .</span><span class="sxs-lookup"><span data-stu-id="507d8-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="507d8-109">Um valor de ' Y ' ou ' y ' indica que **AddRef** e **Release** são protegidos.</span><span class="sxs-lookup"><span data-stu-id="507d8-109">A value of 'Y' or 'y' indicate that **AddRef** and **Release** are secured.</span></span> <span data-ttu-id="507d8-110">Se esse valor de registro não estiver presente ou definido com um valor diferente de ' Y ' ou ' y ', **AddRef** e **Release** não serão protegidos.</span><span class="sxs-lookup"><span data-stu-id="507d8-110">If this registry value is not present or is set to a value other than 'Y' or 'y', **AddRef** and **Release** are not secured.</span></span> <span data-ttu-id="507d8-111">A habilitação de referências seguras reduz as chamadas remotas.</span><span class="sxs-lookup"><span data-stu-id="507d8-111">Enabling secure references slows remote calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="507d8-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="507d8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="507d8-113">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="507d8-113">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="507d8-114">Definindo a segurança de todo o processo</span><span class="sxs-lookup"><span data-stu-id="507d8-114">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




