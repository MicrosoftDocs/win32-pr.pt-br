---
title: RPC (Qualidade de Serviço)
description: Os programas cliente podem usar a função RpcBindingSetAuthInfoEx em vez da função RpcBindingSetAuthInfo para criar uma associação autenticada.
ms.assetid: bc3d47ba-3c1b-4aba-8fe3-b4501a621931
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d7c68386a5d7db4f59b620bc998d628faa2969671ef99b5c5fc2c65aadeb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927144"
---
# <a name="quality-of-service-rpc"></a>RPC (Qualidade de Serviço)

Os programas cliente podem usar a [**função RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) em vez da [**função RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) para criar uma associação autenticada. Se fizerem isso, passarão um ponteiro para uma estrutura [**\_ \_ QOS RPC SECURITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) como o parâmetro final **de RpcBindingSetAuthInfoEx.** Essa estrutura contém informações sobre a qualidade do serviço. Os programas cliente também podem especificar o rastreamento de identidade e selecionar o tipo de representação.

Use o **membro Funcionalidades** da estrutura [**\_ \_ QOS RPC SECURITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) para definir quais partes do aplicativo cliente/servidor são autenticadas. Se AS FUNCIONALIDADES de QOS de RPC PADRÃO forem selecionadas, a biblioteca em tempo de executar RPC autentica o cliente ou o servidor de acordo com o padrão \_ \_ para o \_ \_ SSP. Por padrão, o protocolo Kerberos SSP autentica o cliente e o servidor. O padrão para todos os outros SSPs que a Microsoft fornece é autenticar o cliente no servidor, mas não para autenticar o servidor no cliente.

Se o cliente e o servidor sempre devem  se autenticar entre si, deverão definir o membro Funcionalidades da estrutura [**\_ \_ QOS RPC SECURITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) como FUNCIONALIDADES MÚTUAS DE QOS do RPC \_ \_ \_ \_ \_ C. Alguns provedores de segurança podem não dar suporte à autenticação mútua. Se \_ AUTH MÚTUA DE FUNCIONALIDADES DE QOS do RPC C for especificada para esses provedores de segurança, um erro será retornado quando uma chamada de procedimento \_ \_ remoto for \_ \_ feita. Ao usar o SSP SCHANNEL, também é possível definir o membro **Funcionalidades** como RECURSOS QOS do RPC \_ QUALQUER \_ \_ \_ \_ AUTORIDADE. Essa constante especifica que o SSP deve validar a chamada de procedimento remoto mesmo se a autoridade de certificação que emitiu o certificado de autenticação do cliente não estiver no armazenamento de certificados raiz do SSP. O padrão é rejeitar o certificado se o SSP não reconhecer a autoridade de certificação. A autoridade de certificação é uma empresa ou organização independente, como a VeriSign, que emite certificados de autenticação.

Os aplicativos também podem definir o controle de identidade que a biblioteca em tempo de executar RPC usa. Os programas geralmente usam [*o controle de identidade estático*](s-glos.md). Com o acompanhamento estático, as credenciais do cliente são definidas quando ele chama a [**função RpcBindingSetAuthInfo.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) A biblioteca em tempo de executar RPC usa essas credenciais para todas as chamadas RPC na associação, independentemente das alterações na identidade do thread de chamada ou do processo de chamada. Os aplicativos também podem selecionar [*o controle de identidade dinâmico.*](d-glos.md) O controle de identidade dinâmico instrui a biblioteca de tempo de executar RPC a usar as credenciais do thread de chamada no momento de cada chamada, em vez do alça de associação. O rastreamento de identidade padrão é estático.

Se a identidade do cliente não for mudar, o acompanhamento de identidade estático poderá ter características de desempenho melhores e poderá economizar o tempo de execução RPC de verificar sempre se a identidade no thread de chamada é a mesma que a identidade dada ao sistema de segurança. Se a identidade do thread de chamada pode mudar entre chamadas e o servidor precisa reconhecer essas alterações, é melhor especificar o acompanhamento de identidade dinâmico– o tempo de run time RPC rastreia e acompanha com eficiência a identidade para você e, se a identidade mudar, gerenciará essa alteração em seu nome.

> [!Note]  
> Para **chamadas ncalrpc,** o acompanhamento de identidade estática e dinâmica tem características de desempenho diferentes e, dependendo das circunstâncias, qualquer uma pode ser mais rápida.

 

Como parte da especificação do QOS, o programa cliente também pode definir o tipo de representação que um programa de servidor pode executar em seu nome. Para obter mais informações, consulte [Representação de cliente](client-impersonation.md).

O campo número de versão da estrutura [**\_ \_ QOS RPC SECURITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) sempre deve ser definido como RPC \_ C SECURITY \_ \_ QOS \_ VERSION.

 

 




