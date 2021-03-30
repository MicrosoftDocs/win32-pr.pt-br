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
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

Determina se as tentativas de conexão com objetos em execução são filtradas para os níveis de confiança da política de restrição de software (SRP) compatíveis.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz do reg** .

Os valores de cadeia de caracteres de {N, N, não, não, não} indicam que as tentativas de conexão com objetos em execução não são filtrados em níveis de confiança do SRP compatíveis. Se esse valor de registro for definido como qualquer outro valor ou não existir, o objeto em execução não poderá ter um nível de confiança SRP menos estrito do que o objeto de cliente. Por exemplo, o objeto em execução não poderá ter um nível de confiança não permitido se o objeto de cliente tiver um nível de confiança irrestrito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




