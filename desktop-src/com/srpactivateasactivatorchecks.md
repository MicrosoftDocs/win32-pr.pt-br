---
title: SRPActivateAsActivatorChecks
description: Determina se os níveis de confiança da política de restrição de software (SRP) são usados durante as ativações do ActivateAsActivator.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- COM valor do registro SRPActivateAsActivatorChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635546"
---
# <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="9a17a-104">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="9a17a-104">SRPActivateAsActivatorChecks</span></span>

<span data-ttu-id="9a17a-105">Determina se os níveis de confiança da política de restrição de software (SRP) são usados durante as ativações do ActivateAsActivator.</span><span class="sxs-lookup"><span data-stu-id="9a17a-105">Determines whether software restriction policy (SRP) trust levels are used during ActivateAsActivator activations.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="9a17a-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="9a17a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a><span data-ttu-id="9a17a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a17a-107">Remarks</span></span>

<span data-ttu-id="9a17a-108">Este é um valor de **\_ sz do reg** .</span><span class="sxs-lookup"><span data-stu-id="9a17a-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="9a17a-109">Os valores de cadeia de caracteres de {N, N, não, não, não} indicam que o objeto de servidor é executado com o nível de confiança SRP do objeto de cliente, independentemente do nível de confiança do SRP com o qual foi configurado.</span><span class="sxs-lookup"><span data-stu-id="9a17a-109">String values of {N, n, NO, No, no} indicate that the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which it was configured.</span></span> <span data-ttu-id="9a17a-110">Se esse valor de registro for definido como qualquer outro valor ou não existir, o nível de confiança do SRP configurado para o objeto de servidor será comparado com o nível de confiança do SRP do objeto de cliente e que o nível de confiança mais estrito é usado para executar o objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="9a17a-110">If this registry value is set to any other value or does not exist, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and that the more stringent trust level is used to run the server object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a17a-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a17a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a17a-112">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="9a17a-112">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




