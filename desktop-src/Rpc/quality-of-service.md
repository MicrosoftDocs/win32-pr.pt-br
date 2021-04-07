---
title: Qualidade de serviço (RPC)
description: Os programas cliente podem usar a função RpcBindingSetAuthInfoEx em vez da função RpcBindingSetAuthInfo para criar uma associação autenticada.
ms.assetid: bc3d47ba-3c1b-4aba-8fe3-b4501a621931
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee93b1aa376c9d6f4e2b3eedab73c91471d42498
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824105"
---
# <a name="quality-of-service-rpc"></a>Qualidade de serviço (RPC)

Os programas cliente podem usar a função [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) em vez da função [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) para criar uma associação autenticada. Se isso for feito, eles passarão um ponteiro para uma estrutura de [**\_ \_ QoS de segurança RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) como o parâmetro final de **RpcBindingSetAuthInfoEx**. Essa estrutura contém informações sobre a qualidade do serviço. Os programas cliente também podem especificar o controle de identidade e selecionar o tipo de representação.

Use o membro **Capabilities** da estrutura [**de \_ \_ QoS de segurança RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) para definir quais partes do aplicativo cliente/servidor são autenticadas. Se \_ \_ \_ \_ o padrão de recursos de QoS RPC C for selecionado, a biblioteca de tempo de execução RPC autenticará o cliente ou o servidor de acordo com o padrão para o SSP. Por padrão, o SSP do protocolo Kerberos autentica o cliente e o servidor. O padrão para todos os outros SSPs que a Microsoft fornece é autenticar o cliente para o servidor, mas não para autenticar o servidor para o cliente.

Se o cliente e o servidor sempre devem se autenticar entre si, defina o membro de **recursos** da estrutura de [**\_ \_ QoS de segurança RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) para \_ \_ \_ autenticação mútua de recursos de QoS RPC C \_ \_ . Alguns provedores de segurança podem não dar suporte à autenticação mútua. Se \_ \_ \_ a autenticação mútua dos recursos de QoS RPC C \_ \_ for especificada para esses provedores de segurança, um erro será retornado quando uma chamada de procedimento remoto for feita. Ao usar o SSP do SCHANNEL, também é possível definir o membro de **recursos** para \_ os recursos de QoS RPC C \_ \_ \_ qualquer \_ autoridade. Essa constante especifica que o SSP deve validar a chamada de procedimento remoto mesmo se a autoridade de certificação que emitiu o certificado de autenticação do cliente não estiver no repositório de certificados raiz do SSP. O padrão é rejeitar o certificado se o SSP não reconhecer a autoridade de certificação. A autoridade de certificação é uma empresa ou organização independente, como a VeriSign, que emite certificados de autenticação.

Os aplicativos também podem definir o controle de identidade que a biblioteca de tempo de execução RPC usa. Os programas geralmente usam o [*rastreamento de identidade estático*](s-glos.md). Com o rastreamento estático, as credenciais do cliente são definidas quando ele chama a função [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) . Em seguida, a biblioteca de tempo de execução RPC usa essas credenciais para todas as chamadas RPC na associação, independentemente das alterações na identidade do thread de chamada ou do processo de chamada. Os aplicativos também podem selecionar o [*controle de identidade dinâmico*](d-glos.md). O controle de identidade dinâmico instrui a biblioteca de tempo de execução RPC a usar as credenciais do thread de chamada no momento de cada chamada, em vez do identificador de ligação. O controle de identidade padrão é estático.

Se a identidade do cliente não for alterada, o rastreamento de identidade estático poderá ter melhores características de desempenho e poderá salvar o tempo de execução de RPC a partir da verificação sempre que a identidade no thread de chamada for igual à identidade fornecida ao sistema de segurança. Se a identidade do thread de chamada puder mudar entre as chamadas e o servidor precisar reconhecer essas alterações, é melhor especificar o controle de identidade dinâmico — o tempo de execução de RPC de forma silenciosa e eficiente controla a identidade para você e, se a identidade for alterada, o gerenciará essa alteração em seu nome.

> [!Note]  
> Para chamadas **Ncalrpc** , o controle de identidade estático e dinâmico tem características de desempenho diferentes e, dependendo das circunstâncias, pode ser mais rápido.

 

Como parte da especificação de QOS, o programa cliente também pode definir o tipo de representação que um programa de servidor pode executar em seu nome. Para obter mais informações, consulte [representação do cliente](client-impersonation.md).

O campo número de versão da [**estrutura \_ \_ QoS de segurança RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) deve ser sempre definido como a \_ versão de QoS de segurança RPC C \_ \_ \_ .

 

 




