---
title: Funções SNMP
description: Este tópico descreve três agrupações de funções SNMP e lista as funções incluídas em cada grupo
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- SNMP Functions SNMP
- Funções SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42028e4045d4d0dfeb183dc29a3dc85e7220ed3d5bccf39a3cc9871215188153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143009"
---
# <a name="snmp-functions"></a>Funções SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, [Windows gerenciamento remoto,](/windows/desktop/WinRM/portal)que é a implementação da Microsoft do WS-Man.\]

Este tópico descreve três agrupações de funções SNMP e lista as funções incluídas em cada grupo:

-   [Funções de API do Agente de Extensão SNMP](#snmp-extension-agent-api-functions)
-   [Funções de API de Gerenciamento SNMP](#snmp-management-api-functions)
-   [Funções de API do Utilitário SNMP](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>Funções de API do Agente de Extensão SNMP

As funções do agente de extensão SNMP definem a interface entre o serviço SNMP e as DLLs do agente de extensão SNMP de terceiros. A tabela a seguir lista funções que os aplicativos podem usar para resolver as vinculações variáveis especificadas por PDUs (unidades de dados de protocolo SNMP) de entrada.

| Função de API do Agente de Extensão SNMP                    | Descrição                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**SnmpExtensionClose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Solicita que o agente de extensão SNMP desalocar recursos e encerrar operações.                                    |
| [**Snmpextensioninit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Inicializa a DLL do agente de extensão SNMP.                                                                                |
| [**SnmpExtensionInitEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Identifica as subárvores MIB (base de informações de gerenciamento) adicionais compatíveis com o agente de extensão SNMP.             |
| [**SnmpExtensionMonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Fornece ao agente de extensão SNMP informações sobre os contadores e parâmetros internos do serviço.            |
| [**Snmpextensionquery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Resolve solicitações SNMP que contêm variáveis em uma ou mais subárvores MIB registradas do agente de extensão SNMP. |
| [**Snmpextensionqueryex**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Processa solicitações SNMP que especificam variáveis em uma ou mais subárvores MIB registradas por agentes de extensão SNMP. |
| [**Snmpextensiontrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Recupera informações que o serviço requer para gerar interceptações para o agente de extensão SNMP.                          |



 

## <a name="snmp-management-api-functions"></a>Funções de API de Gerenciamento SNMP

As funções de gerenciamento SNMP definem a interface entre aplicativos de gerenciador SNMP de terceiros e a biblioteca de vínculo dinâmico (DLL) da função de gerenciamento Mgmtapi.dll. A DLL funciona em conjunto com o serviço de interceptação SNMP (Snmptrap.exe) e pode interagir com um ou mais aplicativos de gerenciador SNMP de terceiros. A tabela a seguir lista as funções de gerenciamento que os aplicativos de gerente de terceiros usam para executar operações do gerenciador SNMP.

| Função de API de Gerenciamento SNMP                   | Descrição                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpMgrClose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Fecha os soquetes de comunicação e as estruturas de dados associadas à sessão especificada.                                                                                                  |
| [**SnmpMgrCtl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Define um parâmetro operacional associado a uma sessão SNMP.                                                                                                                                   |
| [**SnmpMgrGetTrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Retorna dados de interceptação pendentes que o chamador não recebeu se a recepção de interceptação estiver habilitada.                                                                                                           |
| [**SnmpMgrGetTrapEx**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Retorna dados de interceptação pendentes que o chamador não recebeu se a recepção de interceptação estiver habilitada. Também retorna o endereço da origem do transporte e a intercepta da comunidade associada à intercepta. |
| [**SnmpMgrOidToStr**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Converte uma estrutura de identificador de objeto interno em sua representação de cadeia de caracteres.                                                                                                                         |
| [**SnmpMgrOpen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Inicializa soquetes de comunicação e estruturas de dados necessárias para estabelecer a comunicação com o agente SNMP.                                                                               |
| [**SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Solicita que a operação especificada seja executada pelo agente especificado.                                                                                                                             |
| [**SnmpMgrStrToOid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Converte o formato de cadeia de caracteres de um identificador de objeto em sua estrutura de identificador de objeto interna.                                                                                                        |
| [**SnmpMgrTrapListen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Registra a capacidade de um aplicativo gerenciador SNMP receber interceptações SNMP do Serviço de Interceptação SNMP.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>Funções de API do Utilitário SNMP

As funções do utilitário SNMP fornecem funcionalidades úteis durante o desenvolvimento de aplicativos SNMP, incluindo a simplificação da manipulação de estruturas de dados SNMP. A tabela a seguir lista as funções do utilitário SNMP.

| Função de API do Utilitário SNMP                                  | Descrição                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpSvcGetUptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Recupera o tempo, em centiseconds, para o qual o serviço SNMP está em execução.                                                                                  |
| [**SnmpSvcSetLogLevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Ajusta o nível de detalhes da saída de depuração do serviço SNMP e dos agentes de extensão SNMP.                                                              |
| [**SnmpSvcSetLogType**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Ajusta o destino da saída de depuração do serviço SNMP e dos agentes de extensão SNMP.                                                                 |
| [**SnmpUtilAsnAnyCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Copia uma estrutura [**AsnAny de origem**](/windows/desktop/api/Snmp/ns-snmp-asnany) para uma **estrutura AsnAny de** destino.                                                                      |
| [**SnmpUtilAsnAnyFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Libera a memória que foi alocada para uma estrutura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) especificada.                                                                        |
| [**Snmputildbgprint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Define o nível de informações de depuração a serem recebidas do serviço SNMP ou de uma chamada para [**SnmpUtilDbgPrint.**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)                       |
| [**Snmputilidstoa**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Converte um OID (identificador de objeto) em uma cadeia de caracteres terminada em nulo.                                                                                                   |
| [**SnmpUtilMemAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Aloca memória dinâmica do heap do processo.                                                                                                                    |
| [**SnmpUtilMemFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Libera o objeto de memória especificado.                                                                                                                                 |
| [**SnmpUtilMemReAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Altera o tamanho do objeto de memória especificado.                                                                                                                   |
| [**SnmpUtilOctetsCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Compara duas cadeias de caracteres de octeto.                                                                                                                                        |
| [**SnmpUtilOctetsCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Copia uma estrutura [**AsnOctetString de**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) origem para uma **estrutura AsnOctetString de** destino.                                              |
| [**SnmpUtilOctetsFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Libera a memória que foi alocada para a cadeia de caracteres de octeto especificada.                                                                                                |
| [**SnmpUtilOctetsNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Executa uma comparação de duas cadeias de caracteres de octeto com o número especificado de subidentificadores.                                                                              |
| [**SnmpUtilOidAppend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Anexa um identificador de objeto de origem, contido em uma [**estrutura AsnObjectIdentifier,**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) a um identificador de objeto de destino.          |
| [**SnmpUtilOidCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Compara dois identificadores de objeto contidos em [**estruturas AsnObjectIdentifier.**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier)                                           |
| [**SnmpUtilOidCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Copia uma estrutura [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) de origem para uma **estrutura AsnObjectIdentifier de** destino.                               |
| [**SnmpUtilOidFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Libera a memória que foi alocada para o identificador de objeto especificado.                                                                                           |
| [**SnmpUtilOidNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Compara dois identificadores de objeto contidos em [**estruturas AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) com o número especificado de subidentificadores. |
| [**SnmpUtilOidToA**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Converte um OID (identificador de objeto) em uma cadeia de caracteres terminada em nulo.                                                                                                   |
| [**SnmpUtilPrintAsnAny**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Imprime um valor contido em uma estrutura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) para fins de depuração e desenvolvimento.                                              |
| [**SnmpUtilPrintOid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Formata o identificador de objeto (OID) especificado e imprime o resultado para o dispositivo de saída padrão.                                                                 |
| [**SnmpUtilVarBindCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Copia uma estrutura [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) de origem para uma estrutura de **SnmpVarBind** de destino.                                                       |
| [**SnmpUtilVarBindListCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Copia uma estrutura [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) de origem para uma estrutura de **SnmpVarBindList** de destino.                                           |
| [**SnmpUtilVarBindFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Libera a memória que foi alocada para a estrutura [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) especificada.                                                            |
| [**SnmpUtilVarBindListFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Libera a memória que foi alocada para a estrutura [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) especificada.                                                    |



 

 

 