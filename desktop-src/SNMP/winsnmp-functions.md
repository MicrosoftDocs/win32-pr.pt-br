---
title: Funções WinSNMP
description: As funções usadas com o WinSNMP se enquadram nos seguintes agrupamentos funcionais. Segue uma lista alfabética.
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29169e8cf86b7f21ebbc40ced2ac37a46668c727183a9b2970eb368c7e81d85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142799"
---
# <a name="winsnmp-functions"></a>Funções WinSNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. em vez disso, use [Gerenciamento Remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

As funções usadas com o WinSNMP se enquadram nos seguintes agrupamentos funcionais. Segue uma lista alfabética.

-   [Funções de comunicação](#winsnmp-communications-functions)
-   [Funções de contexto e entidade](#winsnmp-entity-and-context-functions)
-   [Funções de banco de dados](#winsnmp-database-functions)
-   [Funções de PDU](#winsnmp-pdu-functions)
-   [Funções de utilitário](#winsnmp-utility-functions)
-   [Funções de associação de variáveis](#winsnmp-variable-binding-functions)
-   [Lista alfabética de funções WinSNMP](/windows)

## <a name="winsnmp-communications-functions"></a>Funções de comunicação de WinSNMP

As funções de comunicação WinSNMP fornecem uma interface entre o aplicativo de chamada WinSNMP e a implementação do Microsoft WinSNMP. A implementação manipula a comunicação entre o aplicativo e outras entidades de gerenciamento.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>SnmpCancelMsg</strong></a></td>
<td>Solicita que a implementação do Microsoft WinSNMP cancele tentativas de retransmissão e notificações de tempo limite para uma mensagem de solicitação SNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a></td>
<td>Informa a implementação de que um aplicativo está desconectando e não requer mais recursos alocados.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>SnmpCleanupEx</strong></a></td>
<td>Executa a limpeza quando não há chamadas bem-sucedidas pendentes para <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> ou <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> em um aplicativo WinSNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a></td>
<td>Habilita a implementação para desalocar recursos associados a uma sessão e para fechar mecanismos de comunicação.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a></td>
<td>Solicita que a implementação abra uma sessão WinSNMP e aloque recursos e mecanismos de comunicação. Ao desenvolver novos aplicativos WinSNMP, é recomendável chamar a função <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> para abrir uma sessão WinSNMP em vez de chamar a função <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>SnmpListen</strong></a></td>
<td>Registra ou cancela o registro de um aplicativo WinSNMP como um agente SNMP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a></td>
<td>Solicita que a implementação abra uma sessão WinSNMP e aloque recursos e mecanismos de comunicação. Ao desenvolver novos aplicativos WinSNMP, é recomendável chamar a função <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> para abrir uma sessão WinSNMP em vez de chamar a função <strong>SnmpOpen</strong> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a></td>
<td>Retorna mensagens SNMP e notificações e dados de interceptação pendentes.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a></td>
<td>Informa a implementação que o aplicativo precisa registrar ou cancelar o registro para interceptações e notificações.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a></td>
<td>Solicita que a implementação transmita uma unidade de dados de protocolo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a></td>
<td>Notifica a implementação para executar procedimentos de inicialização para o aplicativo. Um aplicativo deve chamar a função <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> com êxito antes de chamar qualquer outra função WinSNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a></td>
<td>Notifica a implementação do Microsoft WinSNMP de que o aplicativo WinSNMP exige os serviços da implementação. O <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> habilita o suporte para vários módulos de software independentes que usam o WinSNMP dentro do mesmo aplicativo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a></td>
<td>Notifica uma sessão WinSNMP de que uma mensagem SNMP ou evento assíncrono está disponível.
<blockquote>
[!Note]<br />
Essa função de retorno de chamada aplica-se somente a sessões abertas como resultado de uma chamada para a função <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="winsnmp-entity-and-context-functions"></a>Funções de contexto e entidade WinSNMP

A entidade WinSNMP e as funções de contexto permitem que um aplicativo WinSNMP especifique nomes amigáveis para entidades e contextos SNMP. A implementação do Microsoft WinSNMP traduz o nome para seus componentes SNMPv1 ou SNMPv2C usando o banco de dados da implementação.



| Função                                     | Descrição                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | Retorna uma cadeia de caracteres que identifica um contexto SNMP (um conjunto de recursos de objeto gerenciado).                                  |
| [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | Retorna uma cadeia de caracteres que identifica uma entidade de gerenciamento SNMP.                                                            |
| [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | Libera recursos alocados pela função [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) para um contexto SNMP.         |
| [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | Libera recursos alocados pela função [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) para uma entidade de gerenciamento SNMP. |
| [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | Altera a porta atribuída a uma entidade de destino SNMP.                                                               |
| [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | Retorna um identificador para informações de contexto SNMP que são específicas para a implementação.                                   |
| [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | Retorna um identificador para informações da entidade de gerenciamento SNMP que é específica para a implementação.                         |



 

## <a name="winsnmp-database-functions"></a>Funções de banco de dados WinSNMP

As funções de banco de dados WinSNMP fornecem um aplicativo WinSNMP com acesso às configurações atuais no armazenamento de informações administrativas da implementação do Microsoft WinSNMP. Essas funções permitem alterar o modo de retransmissão e o modo de tradução de contexto e entidade. As funções de banco de dados também fornecem ao aplicativo a capacidade de manipular os valores de tempo limite e de contagem de repetições.



| Função                                               | Descrição                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | Retorna a configuração atual do modo de retransmissão.                                               |
| [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | Retorna o valor da contagem de repetições, em unidades, para a retransmissão de solicitações de mensagens SNMP.             |
| [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | Retorna o valor de tempo limite, em centésimos de segundo, para a transmissão de solicitações de mensagens SNMP. |
| [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | Retorna a configuração atual do modo de tradução da entidade e do contexto.                               |
| [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | Recupera informações que identificam o fornecedor WinSNMP.                                             |
| [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | Altera o modo de retransmissão.                                                                      |
| [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | Altera o valor da contagem de repetições para a retransmissão de solicitações de mensagens SNMP.                        |
| [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | Altera o valor de tempo limite para a transmissão de solicitações de mensagens SNMP.                             |
| [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | Altera a entidade e o modo de tradução de contexto.                                                      |



 

## <a name="winsnmp-pdu-functions"></a>Funções de PDU de WinSNMP

As funções de PDU de WinSNMP permitem que aplicativos WinSNMP extraem e atualizem os elementos de dados (ou campos) de uma PDU. Isso inclui a PDUs retornada por uma chamada para a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) ou a função [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) . As funções PDU também constroem PDUs para uso nas funções [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .



| Função                                     | Descrição                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | Cria e Inicializa uma unidade de dados do protocolo SNMP.                                                                                                                               |
| [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | Duplica uma unidade de dados do protocolo SNMP.                                                                                                                                            |
| [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | Libera recursos associados a uma unidade de dados do protocolo SNMP criada pela função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) . |
| [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | Retorna elementos de dados selecionados de uma unidade de dados de protocolo SNMP especificada.                                                                                                          |
| [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | Atualiza os elementos de dados selecionados em uma unidade de dados de protocolo SNMP especificada.                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a>Funções do utilitário WinSNMP

As funções do utilitário WinSNMP permitem que um aplicativo WinSNMP gerencie objetos e mensagens SNMP na interface WinSNMP.



| Função                                         | Descrição                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | Decodifica uma mensagem SNMP codificada ou serializada em seus componentes constituintes.                                      |
| [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | Cria uma mensagem SNMP codificada.                                                                                    |
| [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | Sinaliza a implementação do Microsoft WinSNMP de que ela deve liberar a memória alocada para um descritor específico. |
| [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | Retorna o valor do código de último erro para a última operação SNMP.                                                      |
| [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | Compara dois identificadores de objeto SNMP.                                                                               |
| [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | Copia um identificador de objeto SNMP.                                                                                   |
| [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | Converte a representação binária interna de um identificador de objeto SNMP em seu formato de cadeia de caracteres numérica pontilhada.       |
| [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | Converte o formato de cadeia de caracteres numérica pontilhada de um identificador de objeto SNMP em sua representação binária interna.       |



 

## <a name="winsnmp-variable-binding-functions"></a>Funções de associação de variável WinSNMP

As funções de associação de variável WinSNMP permitem que aplicativos WinSNMP construam e manipulem listas de associação de variáveis e as incluam em PDUs.



| Função                                     | Descrição                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | Enumera as entradas de associação de variável em uma lista de associação de variável especificada.                                                                                                   |
| [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | Cria uma nova lista de associação de variáveis.                                                                                                                                            |
| [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | Remove uma entrada de associação de variável de uma lista de associação de variável.                                                                                                                  |
| [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | Copia uma lista de associação de variável.                                                                                                                                                 |
| [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | Libera recursos para uma lista de associação de variável alocada anteriormente pela função [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) ou [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . |
| [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | Recupera informações de uma entrada de associação de variável especificada.                                                                                                                  |
| [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | Altera as entradas de associação de variável em uma lista de associação de variável; acrescenta novas entradas de associação de variável a uma lista de associação de variável existente.                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a>Lista alfabética de funções WinSNMP

-   [**\_retorno de chamada snmpapi**](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
-   [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)
-   [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)
-   [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)
-   [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)
-   [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)
-   [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)
-   [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)
-   [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)
-   [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)
-   [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)
-   [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)
-   [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)
-   [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)
-   [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)
-   [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)
-   [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)
-   [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)
-   [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)
-   [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)
-   [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)
-   [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)
-   [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode)
-   [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)
-   [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)
-   [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)
-   [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)
-   [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)
-   [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten)
-   [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)
-   [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)
-   [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)
-   [**SnmpOpen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen)
-   [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)
-   [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)
-   [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)
-   [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)
-   [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)
-   [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)
-   [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)
-   [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)
-   [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)
-   [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)
-   [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)
-   [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)
-   [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)
-   [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

 

