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
# <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks

Determina se os níveis de confiança da política de restrição de software (SRP) são usados durante as ativações do ActivateAsActivator.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz do reg** .

Os valores de cadeia de caracteres de {N, N, não, não, não} indicam que o objeto de servidor é executado com o nível de confiança SRP do objeto de cliente, independentemente do nível de confiança do SRP com o qual foi configurado. Se esse valor de registro for definido como qualquer outro valor ou não existir, o nível de confiança do SRP configurado para o objeto de servidor será comparado com o nível de confiança do SRP do objeto de cliente e que o nível de confiança mais estrito é usado para executar o objeto de servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




