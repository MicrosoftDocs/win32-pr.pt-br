---
title: SRPRunningObjectChecks
description: Determina se as tentativas de conexão com objetos em execução são filtradas para os níveis de confiança da política de restrição de software (SRP) compatíveis.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- COM valor do registro SRPRunningObjectChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635545"
---
# <a name="srprunningobjectchecks"></a><span data-ttu-id="22eb9-104">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="22eb9-104">SRPRunningObjectChecks</span></span>

<span data-ttu-id="22eb9-105">Determina se as tentativas de conexão com objetos em execução são filtradas para os níveis de confiança da política de restrição de software (SRP) compatíveis.</span><span class="sxs-lookup"><span data-stu-id="22eb9-105">Determines whether attempts to connect to running objects are screened for compatible software restriction policy (SRP) trust levels.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="22eb9-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="22eb9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a><span data-ttu-id="22eb9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="22eb9-107">Remarks</span></span>

<span data-ttu-id="22eb9-108">Este é um valor de **\_ sz do reg** .</span><span class="sxs-lookup"><span data-stu-id="22eb9-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="22eb9-109">Os valores de cadeia de caracteres de {N, N, não, não, não} indicam que as tentativas de conexão com objetos em execução não são filtrados em níveis de confiança do SRP compatíveis.</span><span class="sxs-lookup"><span data-stu-id="22eb9-109">String values of {N, n, NO, No, no} indicate that attempts to connect to running objects are not screened for compatible SRP trust levels.</span></span> <span data-ttu-id="22eb9-110">Se esse valor de registro for definido como qualquer outro valor ou não existir, o objeto em execução não poderá ter um nível de confiança SRP menos estrito do que o objeto de cliente.</span><span class="sxs-lookup"><span data-stu-id="22eb9-110">If this registry value is set to any other value or does not exist, the running object cannot have a less stringent SRP trust level than the client object.</span></span> <span data-ttu-id="22eb9-111">Por exemplo, o objeto em execução não poderá ter um nível de confiança não permitido se o objeto de cliente tiver um nível de confiança irrestrito.</span><span class="sxs-lookup"><span data-stu-id="22eb9-111">For example, the running object cannot have a Disallowed trust level if the client object has an Unrestricted trust level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22eb9-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22eb9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22eb9-113">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="22eb9-113">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




