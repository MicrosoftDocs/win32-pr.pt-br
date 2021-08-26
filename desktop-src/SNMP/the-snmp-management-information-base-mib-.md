---
title: A base de informações de gerenciamento SNMP (MIB)
description: Uma MIB (Base de Informações de Gerenciamento) descreve um conjunto de objetos gerenciados. Um aplicativo de console de gerenciamento SNMP poderá manipular os objetos em um computador específico se o serviço SNMP tiver uma DLL do agente de extensão que dá suporte ao MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf3fac2e24b79da3ea7277010da5a3f96e3664416809bc440097f4ec0b1384e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127596"
---
# <a name="the-snmp-management-information-base-mib"></a>A base de informações de gerenciamento SNMP (MIB)

Uma MIB (Base de Informações de Gerenciamento) descreve um conjunto de objetos gerenciados. Um aplicativo de console de gerenciamento SNMP poderá manipular os objetos em um computador específico se o serviço SNMP tiver uma DLL do agente de extensão que dá suporte ao MIB.

Cada objeto gerenciado em um MIB tem um identificador exclusivo. O identificador inclui o tipo do objeto (como contador, cadeia de caracteres, medidor ou endereço), o nível de acesso do objeto (como leitura ou leitura/gravação), restrições de tamanho e informações de intervalo.

A tabela a seguir contém uma lista parcial dos MIBs que acompanham o sistema. Eles são instalados com o serviço SNMP no diretório %systemroot% \\ system32. Para uma listagem completa de MIBs, consulte o Windows Resource Kit.



| MIB         | Descrição                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Dhcp. Mib    | MIB definido pela Microsoft que contém tipos de objeto para monitorar o tráfego de rede entre hosts remotos e servidores DHCP                        |
| HOSTMIB. Mib | Contém tipos de objeto para monitorar e gerenciar recursos de host                                                                                 |
| LMMIB2. Mib  | Abrange serviços de estação de trabalho e servidor                                                                                                           |
| MIB \_ II.MIB | Contém a MIB-II (Base de Informações de Gerenciamento), que fornece uma arquitetura e um sistema simples e viável para gerenciar internets baseadas em TCP/IP |
| Ganha. Mib    | MIB definido pela Microsoft para o WINS (Serviço Windows Nome da Internet)                                                                               |



 

**Windows NT:** Normalmente, você pode copiar um MIB do agente de extensão SNMP que dá suporte ao MIB específico. Alguns MIBs adicionais estão disponíveis com o kit de recursos Windows NT 4.0.

As DLLs do agente de extensão para MIB-II, LAN Manager MIB-II e os Recursos do Host MIB são instaladas com o serviço SNMP. As DLLs do agente de extensão para os outros MIBs são instaladas quando seus respectivos serviços são instalados. No momento da inicialização do serviço, o serviço SNMP carrega todas as DLLs do agente de extensão listadas no Registro.

Os usuários podem adicionar outras DLLs do agente de extensão que implementam MIBs adicionais. Para fazer isso, eles devem adicionar uma entrada do Registro para a nova DLL no serviço SNMP. Eles também devem registrar o novo MIB com o aplicativo de console de gerenciamento SNMP. Para obter mais informações, consulte a documentação incluída com seu aplicativo de console de gerenciamento.

Para obter mais informações, consulte [Árvore de Nomes MIB](mib-name-tree.md).

 

 




