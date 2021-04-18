---
title: Funções SNMP
description: Este tópico descreve três agrupamentos de funções SNMP e lista as funções que são incluídas em cada grupo
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- SNMP de funções SNMP
- Funções SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f4cc98ce84fbb66f8beb59a6bf995dc4315159
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454279"
---
# <a name="snmp-functions"></a>Funções SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

Este tópico descreve três agrupamentos de funções SNMP e lista as funções que são incluídas em cada grupo:

-   [Funções de API do agente de extensão SNMP](#snmp-extension-agent-api-functions)
-   [Funções da API de gerenciamento SNMP](#snmp-management-api-functions)
-   [Funções de API do utilitário SNMP](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>Funções de API do agente de extensão SNMP

As funções do agente de extensão SNMP definem a interface entre o serviço SNMP e as DLLs de agente de extensão SNMP de terceiros. A tabela a seguir lista as funções que os aplicativos podem usar para resolver associações de variáveis especificadas por PDUs (unidades de dados de protocolo SNMP) de entrada.

| Função de API do agente de extensão SNMP                    | Descrição                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**SnmpExtensionClose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Solicita que o agente de extensão SNMP desaloque recursos e Finalize operações.                                    |
| [**SnmpExtensionInit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Inicializa a DLL do agente de extensão SNMP.                                                                                |
| [**SnmpExtensionInitEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Identifica todas as subárvores de MIB (base de informações de gerenciamento) adicionais às quais o agente de extensão SNMP dá suporte.             |
| [**SnmpExtensionMonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Fornece o agente de extensão SNMP com informações sobre os contadores internos e os parâmetros do serviço.            |
| [**SnmpExtensionQuery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Resolve as solicitações SNMP que contêm variáveis em uma ou mais das subárvores MIB registradas do agente de extensão SNMP. |
| [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Processa solicitações SNMP que especificam variáveis em uma ou mais subárvores MIB registradas por agentes de extensão SNMP. |
| [**SnmpExtensionTrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Recupera informações que o serviço requer para gerar interceptações para o agente de extensão SNMP.                          |



 

## <a name="snmp-management-api-functions"></a>Funções da API de gerenciamento SNMP

As funções de gerenciamento de SNMP definem a interface entre os aplicativos de Gerenciador SNMP de terceiros e a DLL (biblioteca de vínculo dinâmico) Mgmtapi.dll de função de gerenciamento. A DLL funciona em conjunto com o serviço de interceptação SNMP (Snmptrap.exe) e pode interagir com um ou mais aplicativos de Gerenciador SNMP de terceiros. A tabela a seguir lista as funções de gerenciamento que os aplicativos do Gerenciador de terceiros usam para executar operações do Gerenciador SNMP.

| Função da API de gerenciamento SNMP                   | Descrição                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpMgrClose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Fecha os soquetes de comunicação e as estruturas de dados associados à sessão especificada.                                                                                                  |
| [**SnmpMgrCtl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Define um parâmetro operacional associado a uma sessão SNMP.                                                                                                                                   |
| [**SnmpMgrGetTrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Retorna dados de interceptação pendentes que o chamador não recebeu se a recepção de interceptação estiver habilitada.                                                                                                           |
| [**SnmpMgrGetTrapEx**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Retorna dados de interceptação pendentes que o chamador não recebeu se a recepção de interceptação estiver habilitada. Também retorna o endereço da origem de transporte e a interceptação da comunidade associada à interceptação. |
| [**SnmpMgrOidToStr**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Converte uma estrutura de identificador de objeto interno em sua representação de cadeia de caracteres.                                                                                                                         |
| [**SnmpMgrOpen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Inicializa os soquetes de comunicação e as estruturas de dados necessários para estabelecer a comunicação com o agente SNMP.                                                                               |
| [**SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Solicita que a operação especificada seja executada pelo agente especificado.                                                                                                                             |
| [**SnmpMgrStrToOid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Converte o formato de cadeia de caracteres de um identificador de objeto em sua estrutura de identificador de objeto interno.                                                                                                        |
| [**SnmpMgrTrapListen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Registra a capacidade de um aplicativo Gerenciador SNMP de receber Interceptações SNMP do serviço de interceptação SNMP.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>Funções de API do utilitário SNMP

As funções do utilitário SNMP fornecem recursos úteis durante o desenvolvimento de aplicativos SNMP, incluindo a simplificação da manipulação de estruturas de dados SNMP. A tabela a seguir lista as funções do utilitário SNMP.

| Função da API do utilitário SNMP                                  | Descrição                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpSvcGetUptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Recupera a hora, em centiseconds, para a qual o serviço SNMP está em execução.                                                                                  |
| [**SnmpSvcSetLogLevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Ajusta o nível de detalhe da saída de depuração do serviço SNMP e dos agentes de extensão SNMP.                                                              |
| [**SnmpSvcSetLogType**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Ajusta o destino para a saída de depuração do serviço SNMP e de agentes de extensão SNMP.                                                                 |
| [**SnmpUtilAsnAnyCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Copia uma estrutura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) de origem para uma estrutura de **AsnAny** de destino.                                                                      |
| [**SnmpUtilAsnAnyFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Libera a memória que foi alocada para uma estrutura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) especificada.                                                                        |
| [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Define o nível de informações de depuração a serem recebidas do serviço SNMP ou de uma chamada para [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint).                       |
| [**SnmpUtilIdsToA**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Converte um OID (identificador de objeto) em uma cadeia de caracteres terminada em nulo.                                                                                                   |
| [**SnmpUtilMemAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Aloca memória dinâmica a partir do heap de processo.                                                                                                                    |
| [**SnmpUtilMemFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Libera o objeto de memória especificado.                                                                                                                                 |
| [**SnmpUtilMemReAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Altera o tamanho do objeto de memória especificado.                                                                                                                   |
| [**SnmpUtilOctetsCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Compara duas cadeias de caracteres de octeto.                                                                                                                                        |
| [**SnmpUtilOctetsCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Copia uma estrutura [**AsnOctetString**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) de origem para uma estrutura de **AsnOctetString** de destino.                                              |
| [**SnmpUtilOctetsFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Libera a memória que foi alocada para a cadeia de caracteres de octeto especificada.                                                                                                |
| [**SnmpUtilOctetsNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Executa uma comparação de duas cadeias de caracteres de octeto para o número especificado de subidentificadores.                                                                              |
| [**SnmpUtilOidAppend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Acrescenta um identificador de objeto de origem, contido em uma estrutura [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) , a um identificador de objeto de destino.          |
| [**SnmpUtilOidCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Compara dois identificadores de objeto contidos em estruturas [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) .                                           |
| [**SnmpUtilOidCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Copia uma estrutura [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) de origem para uma estrutura de **AsnObjectIdentifier** de destino.                               |
| [**SnmpUtilOidFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Libera a memória que foi alocada para o identificador de objeto especificado.                                                                                           |
| [**SnmpUtilOidNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Compara dois identificadores de objeto contidos em estruturas [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) para o número especificado de subidentificadores. |
| [**SnmpUtilOidToA**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Converte um OID (identificador de objeto) em uma cadeia de caracteres terminada em nulo.                                                                                                   |
| [**SnmpUtilPrintAsnAny**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Imprime um valor contido em uma estrutura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) para fins de depuração e desenvolvimento.                                              |
| [**SnmpUtilPrintOid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Formata o identificador de objeto (OID) especificado e imprime o resultado para o dispositivo de saída padrão.                                                                 |
| [**SnmpUtilVarBindCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Copia uma estrutura [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) de origem para uma estrutura de **SnmpVarBind** de destino.                                                       |
| [**SnmpUtilVarBindListCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Copia uma estrutura [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) de origem para uma estrutura de **SnmpVarBindList** de destino.                                           |
| [**SnmpUtilVarBindFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Libera a memória que foi alocada para a estrutura [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) especificada.                                                            |
| [**SnmpUtilVarBindListFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Libera a memória que foi alocada para a estrutura [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) especificada.                                                    |



 

 

 