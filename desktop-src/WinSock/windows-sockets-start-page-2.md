---
description: O Windows Sockets 2 (Winsock) permite que os programadores criem aplicativos avançados de Internet, intranet e outros com capacidade de rede para transmitir dados de aplicativos pela conexão, independentemente do protocolo de rede que está sendo usado.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091001"
---
# <a name="windows-sockets-2"></a>Windows Sockets 2

## <a name="purpose"></a>Finalidade

O Windows Sockets 2 (Winsock) permite que os programadores criem aplicativos avançados de Internet, intranet e outros com capacidade de rede para transmitir dados de aplicativos pela conexão, independentemente do protocolo de rede que está sendo usado. Com o Winsock, os programadores recebem acesso a recursos de rede avançados do Microsoft® Windows®, como multicast e QoS (qualidade de serviço).

O Winsock segue o modelo de arquitetura do sistema aberto do Windows (WOSA); Ele define uma SPI (interface de provedor de serviços) padrão entre a API (interface de programação de aplicativo), com suas funções exportadas e as pilhas de protocolo. Ele usa o paradigma de soquetes que foi mais popular pela Berkeley Software Distribution (BSD) UNIX. Ele foi adaptado posteriormente para Windows no Windows Sockets 1,1, com o qual os aplicativos do Windows Sockets 2 são compatíveis com versões anteriores. Programação do Winsock centrada anteriormente em volta do TCP/IP. Algumas práticas de programação que funcionaram com TCP/IP não funcionam com todos os protocolos. Como resultado, a API do Windows Sockets 2 adiciona funções onde for necessário para lidar com vários protocolos.

## <a name="developer-audience"></a>Público de desenvolvedores

O Windows Sockets 2 foi projetado para ser usado por programadores C/C++. É necessário ter familiaridade com a rede do Windows.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O Windows Sockets 2 pode ser usado em todas as plataformas Windows. Quando determinadas implementações ou recursos de restrições de plataforma do Windows Sockets 2 existem, eles são claramente indicados na documentação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novidades para Windows Sockets](what-s-new-for-windows-sockets-2.md)<br/>                 | Informações sobre os novos recursos do Windows Sockets.<br/>                                                                                                                                                                                                                                 |
| [Suporte ao protocolo de rede Winsock no Windows](network-protocol-support-in-windows.md)<br/> | Informações sobre o suporte de protocolo de rede para Windows Sockets em diferentes versões do Windows.<br/>                                                                                                                                                                                    |
| [Sobre o Winsock](about-winsock.md)<br/>                                                     | Informações gerais sobre considerações, arquitetura e recursos de programação do Windows Sockets disponíveis para desenvolvedores.<br/>                                                                                                                                                       |
| [Usando o Winsock](using-winsock.md)<br/>                                                     | Procedimentos e técnicas de programação usados com o Windows Sockets. Esta seção inclui técnicas básicas de programação do Winsock, como [introdução com o Winsock](getting-started-with-winsock.md), bem como técnicas avançadas úteis para desenvolvedores de Winsock experientes.<br/> |
| [Referência do Winsock](winsock-reference.md)<br/>                                             | Documentação da API do Windows Sockets.<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Auxiliar de IP](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[Qualidade de Serviço](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
