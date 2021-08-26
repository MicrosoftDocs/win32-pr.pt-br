---
title: Serviço SNMP
description: A implementação Windows Microsoft do protocolo SNMP é usada para configurar dispositivos remotos, monitorar o desempenho de rede, auditar o uso da rede e detectar falhas de rede ou acesso inadequado. Importante A API Windows SNMP da Microsoft dá suporte apenas a versões de protocolo até SNMPv2C. Ele não dá suporte a nenhuma versão posterior do protocolo.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dfb56450edbb6d5f18daa635e30e08e5914eb48fefb28013a66276dbc9a0a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886386"
---
# <a name="snmp-service"></a>Serviço SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, [Windows gerenciamento remoto,](/windows/desktop/WinRM/portal)que é a implementação da Microsoft do WS-Man.\]

## <a name="purpose"></a>Finalidade

A implementação Windows Microsoft do protocolo SNMP é usada para configurar dispositivos remotos, monitorar o desempenho de rede, auditar o uso da rede e detectar falhas de rede ou acesso inadequado.

> [!IMPORTANT]
> A API Windows SNMP da Microsoft dá suporte apenas a versões de protocolo até SNMPv2C. Ele não dá suporte a nenhuma versão posterior do protocolo.

 

## <a name="where-applicable"></a>Quando aplicável

O SNMP usa uma arquitetura distribuída que consiste em aplicativos de gerenciamento e aplicativos de agente. O serviço SNMP implementa um agente SNMP. Para usar as informações fornecidas pelo serviço SNMP, você deve ter pelo menos um host que está executando um aplicativo de gerenciamento SNMP. Você pode usar software de gerenciamento SNMP de terceiros ou pode desenvolver seu próprio aplicativo de software de gerenciamento SNMP. As seguintes APIs estão disponíveis para esta finalidade:

-   SNMP API de Gerenciamento, um conjunto de funções que podem ser usadas para desenvolver rapidamente sistemas de gerenciamento SNMP básicos
-   API winSNMP, versão 2.0, um conjunto de funções para codificação, decodificação, envio e recebimento de mensagens SNMP

Além disso, a API do Agente de Extensão SNMP define a interface entre o serviço SNMP e as DLLs do agente de extensão SNMP de terceiros. As funções da API do Utilitário SNMP podem ser usadas para simplificar o processamento de mensagens SNMP.

## <a name="developer-audience"></a>Público de desenvolvedores

As APIs listadas na seção anterior foram projetadas para uso por programadores C/C++. É necessária familiaridade com SNMP e SNMPv2C, bem como um conhecimento prático dos conceitos de gerenciamento de rede e rede.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter mais informações sobre o sistema operacional necessário para usar uma função específica, consulte a seção Requisitos da página de referência para essa função.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                | Descrição                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novo no SNMP](new-in-snmp.md)<br/>                                                            | Informações sobre atualizações para SNMP.<br/>                                                                                                      |
| [Protocolo SNMP](simple-network-management-protocol-snmp-.md)<br/> | Informações e referência de API para SNMP, incluindo as funções SNMP API de Gerenciamento, API do Agente de Extensão SNMP e API do Utilitário SNMP.<br/> |
| [WinSNMP API](snmp-reference.md)<br/>                                                         | Informações e referência de API para a Api winSNMP (Interface de Programação de Aplicativos) do Microsoft Windows SNMP. <br/>                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protocolo DHCP](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Gerenciamento de Rede](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[Serviço de Roteamento e Acesso Remoto](/windows/desktop/RRAS/portal)
</dt> </dl>

 

