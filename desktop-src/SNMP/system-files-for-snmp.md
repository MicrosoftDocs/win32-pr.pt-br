---
title: Arquivos do sistema para SNMP
description: A tabela a seguir descreve os arquivos principais relacionados ao serviço SNMP.
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb917276fd807835fea703ec27cc66a0d493766d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453560"
---
# <a name="system-files-for-snmp"></a>Arquivos do sistema para SNMP

A tabela a seguir descreve os arquivos principais relacionados ao serviço SNMP.



| Nome de arquivo     | Descrição                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | DLL do agente de extensão que implementa a MIB do DHCP definida pela Microsoft. Instalado somente em servidores DHCP.                                                                                                                                 |
| EVNTAGNT.DLL | DLL SNMP que converte logs de eventos em interceptações SNMP; também conhecido como o tradutor de eventos SNMP.                                                                                                                                       |
| HOSTMIB.DLL  | DLL do agente de extensão que implementa a MIB de recursos de host.                                                                                                                                                                         |
| LMMIB2.DLL   | DLL do agente de extensão que implementa o LAN Manager MIB-II.                                                                                                                                                                             |
| MGMTAPI.DLL  | Biblioteca de API de gerenciamento SNMP da Microsoft. Essa API permite que os aplicativos do Gerenciador SNMP "Escutem" para solicitações do Gerenciador SNMP e enviem solicitações para e recebam respostas de agentes SNMP.                                                |
| MIB. COMPARTIMENTO      | Informações de MIB compiladas usadas pelo MGMTAPI.DLL.                                                                                                                                                                                       |
| SNMP.EXE     | Serviço SNMP. Esse é o agente mestre que recebe solicitações SNMP e as entrega à DLL apropriada do agente de extensão.                                                                                                        |
| SNMPAPI.DLL  | DLL de utilitários SNMP usada pelos aplicativos Gerenciador e DLLs do agente de extensão SNMP. Essa DLL contém uma estrutura para o desenvolvimento de DLLs do agente de extensão.                                                                                   |
| SNMPSNAP.DLL | Aplicativo de configuração SNMP que é um componente de snap-in do MMC (console de gerenciamento Microsoft). O snap-in adiciona várias páginas à folha de propriedades do serviço SNMP. Para obter mais informações, consulte a ajuda online para o serviço SNMP. |
| SNMPTRAP.EXE | Serviço de interceptação SNMP. Recebe interceptações SNMP e as encaminha para os aplicativos do Gerenciador SNMP.                                                                                                                                              |
| WINSMIB.DLL  | DLL do agente de extensão que implementa a MIB do WINS definida pela Microsoft. Instalado somente em servidores WINS.                                                                                                                                 |
| WSNMP32.DLL  | Biblioteca de API do Microsoft [WinSNMP](winsnmp-api.md) . Essa API permite que os aplicativos do Gerenciador SNMP "Escutem" para solicitações do Gerenciador SNMP e enviem solicitações para e recebam respostas de agentes SNMP.                                     |



 

Para obter informações adicionais, consulte [a MIB (base de informações de gerenciamento) SNMP](the-snmp-management-information-base-mib-.md). (Você também pode consultar o Windows 2000 Resource Kit).

 

 




