---
title: Serviço SNMP
description: A implementação do Microsoft Windows do Simple Network Management Protocol (SNMP) é usada para configurar dispositivos remotos, monitorar o desempenho da rede, auditar o uso da rede e detectar falhas de rede ou acesso impróprio. Importante a API SNMP do Microsoft Windows só dá suporte a versões de protocolo até o SNMPv2C. Ele não oferece suporte a nenhuma versão posterior do protocolo.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP DO SNMP
- SNMP do SNMP, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008045"
---
# <a name="snmp-service"></a>Serviço SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

## <a name="purpose"></a>Finalidade

A implementação do Microsoft Windows do Simple Network Management Protocol (SNMP) é usada para configurar dispositivos remotos, monitorar o desempenho da rede, auditar o uso da rede e detectar falhas de rede ou acesso impróprio.

> [!IMPORTANT]
> A API SNMP do Microsoft Windows só dá suporte a versões de protocolo até o SNMPv2C. Ele não oferece suporte a nenhuma versão posterior do protocolo.

 

## <a name="where-applicable"></a>Quando aplicável

O SNMP usa uma arquitetura distribuída que consiste em aplicativos de gerenciamento e aplicativos de agente. O serviço SNMP implementa um agente SNMP. Para usar as informações fornecidas pelo serviço SNMP, você deve ter pelo menos um host que esteja executando um aplicativo de gerenciamento SNMP. Você pode usar software de gerenciamento SNMP de terceiros ou pode desenvolver seu próprio aplicativo de software de gerenciamento SNMP. As seguintes APIs estão disponíveis para essa finalidade:

-   API de gerenciamento SNMP, um conjunto de funções que podem ser usadas para desenvolver rapidamente sistemas de gerenciamento SNMP básicos
-   API WinSNMP, versão 2,0, um conjunto de funções para codificação, decodificação, envio e recebimento de mensagens SNMP

Além disso, a API do agente de extensão SNMP define a interface entre o serviço SNMP e as DLLs do agente de extensão SNMP de terceiros. As funções de API do utilitário SNMP podem ser usadas para simplificar o processamento de mensagens SNMP.

## <a name="developer-audience"></a>Público de desenvolvedores

As APIs listadas na seção anterior foram projetadas para uso por programadores C/C++. É necessário ter familiaridade com o SNMP e o SNMPv2C, bem como um conhecimento prático de conceitos de rede e de gerenciamento de rede.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter mais informações sobre o sistema operacional necessário para usar uma função específica, consulte a seção requisitos da página de referência para essa função.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                | Descrição                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novidades no SNMP](new-in-snmp.md)<br/>                                                            | Informações sobre atualizações do SNMP.<br/>                                                                                                      |
| [Protocolo SNMP](simple-network-management-protocol-snmp-.md)<br/> | Referência de API e informações para SNMP, incluindo a API de gerenciamento SNMP, a API do agente de extensão SNMP e as funções de API do utilitário SNMP.<br/> |
| [API WinSNMP](snmp-reference.md)<br/>                                                         | Informações e referência de API para a interface de programação de aplicativo do Microsoft Windows SNMP (API WinSNMP). <br/>                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protocolo DHCP](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Gerenciamento de rede](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[Serviço de Roteamento e Acesso Remoto](/windows/desktop/RRAS/portal)
</dt> </dl>

 

