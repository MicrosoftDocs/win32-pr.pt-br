---
title: Configurando o Registro para alocações de porta e associação seletiva
description: A partir do Windows 2000, um utilitário no kit de recursos Windows chamado Rpccfg.exe deve ser usado para definir as vinculações. Para obter mais informações, consulte o Windows Resource Kit para obter a versão apropriada do sistema operacional.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, configurando o Registro para alocações de porta e associação seletiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b220e0e3415b7906c847c0f1196fbc815521dee0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465473"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Configurando o Registro para alocações de porta e associação seletiva

A partir do Windows 2000, um utilitário no kit de recursos Windows chamado Rpccfg.exe deve ser usado para definir as vinculações. Para obter mais informações, consulte o Windows Resource Kit para obter a versão apropriada do sistema operacional.

Para versões do Windows anteriores ao Windows 2000, as chaves do Registro na tabela a seguir especificam os padrões do sistema para alocação de porta dinâmica e para associação a NICs em computadores multihomed. Você deve primeiro criar essas chaves e, em seguida, especificar as configurações apropriadas.

O uso [**da função RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) afeta essas configurações. Os desenvolvedores devem estar familiarizados com as configurações do Registro explicadas nesta seção e com a função **RpcServerUseProtseqEx** ao gerenciar alocações de porta. Um exemplo com três aplicativos hipotéticos segue a tabela abaixo e ilustra como essas configurações e a função **RpcServerUseProtseqEx** interoperam.

Se uma chave estiver ausente ou se contiver um valor inválido, toda a configuração será marcada como inválida e todas as **RpcServerUseProtseq \** _ chamadas sobre [_ *ncacn \_ ip \_ tcp* *](/windows/desktop/Midl/ncacn-ip-tcp) ou [**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp) falharão.

> [!Note]  
> As portas alocadas a um processo permanecem alocadas até que o processo seja desalocado. Se todas as portas disponíveis estão em uso, a função retorna RPC \_ S \_ OUT OF \_ \_ RESOURCES.

 




| Chave de porta | Tipo de dados | Descrição | 
|----------|-----------|-------------|
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               Ports</code></pre> | <strong>REG_MULTI_SZ</strong> | Especifica um conjunto de intervalos de portas IP que consistem em todas as portas disponíveis da Internet ou todas as portas não disponíveis na Internet. Cada cadeia de caracteres representa uma única porta ou um conjunto inclusivo de portas (por exemplo, 1000-1050, 1984). Se qualquer entrada estiver fora do intervalo de 0 a 65535 ou se nenhuma cadeia de caracteres não puder ser interpretada, o tempo de execução RPC tratará toda a configuração como inválida. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               PortsInternetAvailable</code></pre> | <strong>REG_SZ</strong> | Y ou N (não sensíveis a minúsculas). Se Y, as portas listadas na chave Portas serão todas as portas disponíveis para a Internet nesse computador. Se N, as portas listadas na chave Portas serão todas as portas que não estão disponíveis para a Internet. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               UseInternetPorts</code></pre> | <strong>REG_SZ</strong> | Y ou N (não sensíveis a minúsculas). Especifica a política padrão do sistema. Se Y, os processos que usam o padrão receberão portas do conjunto de portas disponíveis para a Internet, conforme definido acima. Se N, os processos que usam o padrão receberão portas do conjunto de portas somente da intranet. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   System      CurrentControlSet         Services            Rpc               Linkage                  Bind</code></pre> | <strong>REG_MULTI_SZ</strong> | Lista os nomes de dispositivo de todas as NICs nas quais se vincular por padrão (por exemplo, \Device\AMDPCN1). Se a chave não existir, o servidor se vinculará a todas as NICs. Se a chave existir, o servidor se vinculará às NICs especificadas na chave, a menos que o campo NICFlags esteja definido como RPC_C_BIND_TO_ALL_NICS. Se a chave tiver um valor nulo (""), a configuração será marcada como inválida <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong></strong></a> e todas as chamadas para <strong>RpcServerUseProtseq*</strong> em ncacn_ip_tcp ou <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> falharão. | 




 

A tabela a seguir ilustra como três aplicativos de exemplo são afetados pelas configurações definidas na tabela anterior e como as configurações aplicadas usando a [**função RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) também são afetadas.

Neste exemplo, três aplicativos hipotéticos são considerados:

-   InternetApp: este aplicativo destina-se à exposição à Internet e especificou RPC C USE INTERNET PORT no membro EndpointFlags da estrutura RPC POLICY passada para a \_ \_ função \_ \_ [**RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) 
-   LocalApp: este aplicativo não se destina à exposição à Internet e especificou RPC C USE INTRANET PORT no membro EndpointFlags da estrutura RPC POLICY passada para a \_ \_ função \_ \_ [**RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) 
-   DefaultApp: esse aplicativo especifica zero no membro **EndpointFlags** da estrutura [**RPC \_ POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passada para a [**função RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)

A tabela a seguir explica o impacto que essas configurações têm com base nos valores especificados nas entradas do Registro explicadas na tabela anterior. Para considerações de formatação, os seguintes códigos são atribuídos:

PIA = PortsInternetAvailable Key value

UIP = Valor de Chave UseInternetPorts

O valor da chave Portas, para este exemplo, é 5000-5100 para cada entrada.



| Aplicativo | PIA | UIP | Resultado                                  |
|-------------|-----|-----|-----------------------------------------|
| InternetApp | S   | S   | Usa portas entre 5000 e 5100        |
| LocalApp    | S   | S   | Usa uma porta fora do intervalo 5000-5100 |
| DefaultApp  | S   | S   | Usa portas entre 5000 e 5100        |
| InternetApp | S   | N   | Usa portas entre 5000 e 5100        |
| LocalApp    | S   | N   | Usa uma porta fora do intervalo 5000-5100 |
| DefaultApp  | S   | N   | Usa uma porta fora do intervalo 5000-5100 |
| InternetApp | N   | S   | Usa uma porta fora do intervalo 5000-5100 |
| LocalApp    | N   | S   | Usa portas entre 5000 e 5100        |
| DefaultApp  | N   | S   | Usa uma porta fora do intervalo 5000-5100 |
| InternetApp | N   | N   | Usa uma porta fora do intervalo 5000-5100 |
| LocalApp    | N   | N   | Usa portas entre 5000 e 5100        |
| DefaultApp  | N   | N   | Usa portas entre 5000 e 5100        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**RPC \_ POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[**RpcServerUseProtseqIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[**\_TCP IP \_ ncacn**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**\_UDP IP \_ ncadg**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 
