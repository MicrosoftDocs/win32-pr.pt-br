---
title: SRPRunningObjectChecks
description: Determina se as tentativas de se conectar a objetos em execução são teladas para níveis de confiança SRP (política de restrição de software) compatíveis.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valor do Registro SRPRunningObjectChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c416b5f430540282873e37c5e74ef2cccc1c564f4a5b27842ba2a49e99cc8769
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129788"
---
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

Determina se as tentativas de se conectar a objetos em execução são teladas para níveis de confiança SRP (política de restrição de software) compatíveis.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG SZ.**

Valores de cadeia de caracteres {N, n, NO, Não, não} indicam que as tentativas de conexão com objetos em execução não são teladas para níveis de confiança SRP compatíveis. Se esse valor do Registro for definido como qualquer outro valor ou não existir, o objeto em execução não poderá ter um nível de confiança SRP menos rigoroso do que o objeto cliente. Por exemplo, o objeto em execução não poderá ter um nível de confiança Não permitido se o objeto cliente tiver um nível de confiança Irrestrito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




