---
title: Configurando o registro para alocações de porta e Associação seletiva
description: a partir do Windows 2000, um utilitário no Kit de recursos do Windows chamado Rpccfg.exe deve ser usado para definir associações. para obter mais informações, consulte o Windows Resource Kit para a versão apropriada do sistema operacional.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- Chamada de procedimento remoto RPC, tarefas, configurando o registro para alocações de porta e Associação seletiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8166e9cb4d6706e8eafb016fba309eb64a4c4910b5727bcf88c2e071a7077d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931243"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Configurando o registro para alocações de porta e Associação seletiva

a partir do Windows 2000, um utilitário no Kit de recursos do Windows chamado Rpccfg.exe deve ser usado para definir associações. para obter mais informações, consulte o Windows Resource Kit para a versão apropriada do sistema operacional.

para versões do windows anteriores ao Windows 2000, as chaves do registro na tabela a seguir especificam os padrões do sistema para a alocação de porta dinâmica e para a associação a NICs em computadores de hospedagem múltipla. Você deve primeiro criar essas chaves e, em seguida, especificar as configurações apropriadas.

O uso da função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) afeta essas configurações. Os desenvolvedores devem estar familiarizados com as configurações do registro explicadas nesta seção e a função **RpcServerUseProtseqEx** ao gerenciar as alocações de porta. Um exemplo com três aplicativos hipotéticos segue a tabela abaixo e ilustra como essas configurações e a função **RpcServerUseProtseqEx** interoperam.

Se uma chave estiver ausente ou se contiver um valor inválido, a configuração inteira será marcada como inválida e todas as ** \* RpcServerUseProtseq* _ chamadas acima de [*ncacn \_ IP \_ TCP* *](/windows/desktop/Midl/ncacn-ip-tcp) ou [**ncadg \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) falharão.

> [!Note]  
> As portas alocadas a um processo permanecem alocadas até que o processo seja desativado. Se todas as portas disponíveis estiverem em uso, a função retornará RPC \_ S para \_ fora \_ dos \_ recursos.

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Chave de porta</th>
<th>Tipo de dados</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><strong>REG_MULTI_SZ</strong></td>
<td>Especifica um conjunto de intervalos de portas IP que consistem em todas as portas disponíveis na Internet ou em todas as portas não disponíveis na Internet. Cada cadeia de caracteres representa uma única porta ou um conjunto inclusivo de portas (por exemplo, 1000-1050, 1984). Se alguma entrada estiver fora do intervalo de 0 a 65535, ou se qualquer cadeia de caracteres não puder ser interpretada, o tempo de execução de RPC tratará toda a configuração como inválida.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y ou N (não diferencia maiúsculas de minúsculas). Se Y, as portas listadas na chave portas serão todas as portas disponíveis para a Internet nesse computador. Se N, as portas listadas na chave portas serão todas aquelas portas que não estão disponíveis para a Internet.</td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y ou N (não diferencia maiúsculas de minúsculas). Especifica a política padrão do sistema. Se Y, os processos que usam o padrão serão atribuídos às portas do conjunto de portas disponíveis para a Internet, conforme definido acima. Se N, os processos que usam o padrão serão atribuídos às portas do conjunto de portas somente de intranet.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><strong>REG_MULTI_SZ</strong></td>
<td>Lista os nomes de dispositivos de todas as NICs nas quais associar por padrão (por exemplo, \Device\AMDPCN1). Se a chave não existir, o servidor será associado a todas as NICs. Se a chave existir, o servidor se associará às NICs especificadas na chave, a menos que o campo NICFlags seja definido como RPC_C_BIND_TO_ALL_NICS. Se a chave tiver um valor nulo ( &quot; &quot; ), a configuração será marcada como inválida e todas as chamadas para <strong>RpcServerUseProtseq *</strong> sobre <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> ou <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> falharão.</td>
</tr>
</tbody>
</table>



 

A tabela a seguir ilustra como três aplicativos de exemplo são afetados pelas configurações definidas na tabela anterior e como as configurações aplicadas usando a função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) também são afetadas.

Neste exemplo, três aplicativos hipotéticos são considerados:

-   Internetapp: esse aplicativo destina-se à exposição à Internet e especificou que o RPC \_ C \_ usa a porta da \_ Internet \_ no membro **EndpointFlags** da estrutura de [**\_ política RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passada para a função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .
-   LocalApp: este aplicativo não se destina à exposição à Internet e especificou \_ que o RPC C \_ usa a porta de \_ intranet \_ no membro **EndpointFlags** da estrutura de [**\_ política RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passada para a função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .
-   DefaultApp: esse aplicativo especifica zero no membro **EndpointFlags** da estrutura de [**\_ política RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passada para a função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .

A tabela a seguir explica o impacto que essas configurações têm com base nos valores especificados nas entradas de registro explicadas na tabela anterior. Para considerações de formatação, os códigos a seguir são atribuídos:

PIA = valor de chave PortsInternetAvailable

UIP = valor de chave UseInternetPorts

O valor da chave de portas, para fins deste exemplo, é 5000-5100 para cada entrada.



| Aplicativo | PIA | UIP | Resultado                                  |
|-------------|-----|-----|-----------------------------------------|
| Internetapp | Y   | Y   | Usa portas entre 5000 e 5100        |
| LocalApp    | Y   | Y   | Usa uma porta fora do intervalo de 5000-5100 |
| DefaultApp  | Y   | Y   | Usa portas entre 5000 e 5100        |
| Internetapp | Y   | N   | Usa portas entre 5000 e 5100        |
| LocalApp    | Y   | N   | Usa uma porta fora do intervalo de 5000-5100 |
| DefaultApp  | Y   | N   | Usa uma porta fora do intervalo de 5000-5100 |
| Internetapp | N   | Y   | Usa uma porta fora do intervalo de 5000-5100 |
| LocalApp    | N   | Y   | Usa portas entre 5000 e 5100        |
| DefaultApp  | N   | Y   | Usa uma porta fora do intervalo de 5000-5100 |
| Internetapp | N   | N   | Usa uma porta fora do intervalo de 5000-5100 |
| LocalApp    | N   | N   | Usa portas entre 5000 e 5100        |
| DefaultApp  | N   | N   | Usa portas entre 5000 e 5100        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_política RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
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

[**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 