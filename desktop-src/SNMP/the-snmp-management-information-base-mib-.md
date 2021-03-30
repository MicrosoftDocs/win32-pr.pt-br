---
title: A MIB (base de informações de gerenciamento) SNMP
description: Uma MIB (base de informações de gerenciamento) descreve um conjunto de objetos gerenciados. Um aplicativo de console de gerenciamento SNMP pode manipular os objetos em um computador específico se o serviço SNMP tiver uma DLL de agente de extensão que dá suporte à MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635344"
---
# <a name="the-snmp-management-information-base-mib"></a>A MIB (base de informações de gerenciamento) SNMP

Uma MIB (base de informações de gerenciamento) descreve um conjunto de objetos gerenciados. Um aplicativo de console de gerenciamento SNMP pode manipular os objetos em um computador específico se o serviço SNMP tiver uma DLL de agente de extensão que dá suporte à MIB.

Cada objeto gerenciado em uma MIB tem um identificador exclusivo. O identificador inclui o tipo do objeto (como contador, Cadeia de caracteres, medidor ou endereço), o nível de acesso do objeto (como leitura ou leitura/gravação), restrições de tamanho e informações de intervalo.

A tabela a seguir contém uma lista parcial das MIBs que acompanham o sistema. Eles são instalados com o serviço SNMP no diretório% systemroot% \\ System32. Para obter uma lista completa de MIBs, consulte o Windows Resource Kit.



| MIB         | Description                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCP. MIB    | MIB definida pela Microsoft que contém tipos de objeto para monitorar o tráfego de rede entre hosts remotos e servidores DHCP                        |
| HOSTMIB. MIB | Contém tipos de objeto para monitorar e gerenciar recursos de host                                                                                 |
| LMMIB2. MIB  | Abrange serviços de estação de trabalho e servidor                                                                                                           |
| MIB \_ II. MIB | Contém a MIB-II (base de informações de gerenciamento), que fornece uma arquitetura e um sistema simples e viável para o gerenciamento de Internets baseadas em TCP/IP |
| WINS. MIB    | MIB definida pela Microsoft para o serviço de cadastramento na Internet do Windows (WINS)                                                                               |



 

**Windows NT:** Normalmente, você pode copiar uma MIB do agente de extensão SNMP que dá suporte à MIB específica. Alguns MIBs adicionais estão disponíveis com o Windows NT 4,0 Resource Kit.

As DLLs do agente de extensão para MIB-II, LAN Manager MIB-II e os recursos de host MIB são instalados com o serviço SNMP. As DLLs do agente de extensão para os outros MIBs são instaladas quando seus respectivos serviços são instalados. No momento da inicialização do serviço, o serviço SNMP carrega todas as DLLs do agente de extensão listadas no registro.

Os usuários podem adicionar outras DLLs de agente de extensão que implementam MIBs adicionais. Para fazer isso, eles devem adicionar uma entrada de registro para a nova DLL no serviço SNMP. Eles também devem registrar a nova MIB com o aplicativo de console de gerenciamento SNMP. Para obter mais informações, consulte a documentação incluída no seu aplicativo de console de gerenciamento.

Para obter mais informações, consulte [MIB Name Tree](mib-name-tree.md).

 

 




