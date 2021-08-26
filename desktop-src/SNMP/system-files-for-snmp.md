---
title: Arquivos do sistema para SNMP
description: A tabela a seguir descreve os arquivos de entidade de serviço relacionados ao serviço SNMP.
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 139b83a2d2117af693bcd7ae624ff18d7a18ab5618c9a9597c1e142f62aba07d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886046"
---
# <a name="system-files-for-snmp"></a>Arquivos do sistema para SNMP

A tabela a seguir descreve os arquivos de entidade de serviço relacionados ao serviço SNMP.



| Nome de arquivo     | Descrição                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | DLL do agente de extensão que implementa o MIB DHCP definido pela Microsoft. Instalado somente em servidores DHCP.                                                                                                                                 |
| EVNTAGNT.DLL | DLL SNMP que converte logs de eventos em interceptações SNMP; também conhecido como o tradutor de eventos SNMP.                                                                                                                                       |
| HOSTMIB.DLL  | DLL do agente de extensão que implementa o MIB de Recursos de Host.                                                                                                                                                                         |
| LMMIB2.DLL   | DLL do agente de extensão que implementa o LAN Manager MIB-II.                                                                                                                                                                             |
| MGMTAPI.DLL  | Biblioteca de API de Gerenciamento microsoft SNMP. Essa API permite que os aplicativos do gerenciador SNMP "escutem" as solicitações do gerenciador SNMP e enviem solicitações para e recebam respostas de agentes SNMP.                                                |
| Mib. Bin      | Informações do MIB compiladas usadas pelo MGMTAPI.DLL.                                                                                                                                                                                       |
| SNMP.EXE     | Serviço SNMP. Esse é o agente mestre que recebe solicitações SNMP e as entrega à DLL do agente de extensão apropriada.                                                                                                        |
| SNMPAPI.DLL  | DLL de utilitários SNMP usada por DLLs do agente de extensão SNMP e aplicativos de gerente. Essa DLL contém uma estrutura para desenvolver DLLs do agente de extensão.                                                                                   |
| SNMPSNAP.DLL | Aplicativo de configuração SNMP que é um componente de snap-in Console de Gerenciamento Microsoft (MMC). O snap-in adiciona várias páginas à folha Propriedades do Serviço SNMP. Para obter mais informações, consulte a ajuda online para o serviço SNMP. |
| SNMPTRAP.EXE | Serviço de interceptar SNMP. Recebe interceptações SNMP e encaminha-as para aplicativos do gerenciador SNMP.                                                                                                                                              |
| WINSMIB.DLL  | DLL do agente de extensão que implementa o WINS MIB definido pela Microsoft. Instalado somente em servidores WINS.                                                                                                                                 |
| WSNMP32.DLL  | Biblioteca de API do Microsoft [WinSNMP.](winsnmp-api.md) Essa API permite que os aplicativos do gerenciador SNMP "escutem" as solicitações do gerenciador SNMP e enviem solicitações para e recebam respostas de agentes SNMP.                                     |



 

Para obter informações adicionais, consulte A MIB (Base de Informações de Gerenciamento [SNMP).](the-snmp-management-information-base-mib-.md) (Você também pode consultar o Windows 2000 Resource Kit.)

 

 




