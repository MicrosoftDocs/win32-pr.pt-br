---
title: Usando Transport-Level segurança no cliente
description: O cliente especifica como o servidor representa o cliente quando o cliente estabelece a associação de cadeia de caracteres.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando segurança em nível de transporte no cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917600"
---
# <a name="using-transport-level-security-on-the-client"></a>Usando Transport-Level segurança no cliente

O cliente especifica como o servidor representa o cliente quando o cliente estabelece a associação de cadeia de caracteres. Essas informações de QOS são fornecidas como uma opção de ponto de extremidade na associação de cadeia de caracteres. O cliente pode especificar o nível de representação, controle dinâmico ou estático e o sinalizador somente efetiva.

**Para fornecer informações de qualidade de serviço para o servidor**

1.  O cliente chama [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) para criar as cadeias de componentes, incluindo as opções de ponto de extremidade, no contexto de ligação de cadeia de caracteres correto.
2.  O cliente chama [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obter um novo identificador de ligação e aplicar as informações de qualidade de serviço para o cliente.
3.  O cliente faz chamadas de procedimento remoto usando a alça.

O Microsoft RPC dá suporte a recursos de segurança do Windows somente em [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) e [**Ncalrpc**](/windows/desktop/Midl/ncalrpc). As opções de segurança para outros transportes são ignoradas.

O cliente pode associar os seguintes parâmetros de segurança à associação para o transporte nomeado pipe [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) ou [**Ncalrpc**](/windows/desktop/Midl/ncalrpc):

-   Identificação, representação ou anônima. Especifica o tipo de segurança usado. O padrão é representação.
-   Dinâmico ou estático. Determina se as informações de segurança associadas a um thread são uma cópia das informações de segurança criadas no momento em que a chamada de procedimento remoto é feita (estática) ou um ponteiro para as informações de segurança (dinâmico).

    As informações de segurança estática não são alteradas. A configuração dinâmica reflete as configurações de segurança atuais, incluindo as alterações feitas depois que a chamada de procedimento remoto é feita. Para [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), o padrão para conexões de pipe nomeado remoto é estático, para conexões de pipe nomeado local, o padrão é dinâmico.

-   **True** ou **false**. Especifica o valor do sinalizador somente efetivo. Um valor **true** indica que somente os privilégios de token definidos como on no momento da chamada entram em vigor. Um valor **false** indica que todos os privilégios estão disponíveis e que o aplicativo pode modificá-los.

Qualquer combinação dessas configurações pode ser atribuída à associação, conforme mostrado no exemplo a seguir:

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

As configurações de parâmetro de segurança padrão variam de acordo com o protocolo de transporte.

Para obter informações adicionais sobre a sintaxe das opções de ponto de extremidade, consulte [ponto de extremidade](/windows/desktop/Midl/endpoint).

 

 