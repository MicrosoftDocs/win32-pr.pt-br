---
description: Windows Os Soquetes 2 (Winsock) permitem que os programadores criem aplicativos avançados de Internet, intranet e outros aplicativos com capacidade de rede para transmitir dados do aplicativo pela conexão, independentemente do protocolo de rede que está sendo usado.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Soquetes 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db6acd422e5a1aec90b454a9fce71bfd1ec5d071759edfdffd7aa3a8d02f1b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111118"
---
# <a name="windows-sockets-2"></a>Windows Soquetes 2

## <a name="purpose"></a>Finalidade

Windows Os Soquetes 2 (Winsock) permitem que os programadores criem aplicativos avançados de Internet, intranet e outros aplicativos com capacidade de rede para transmitir dados do aplicativo pela conexão, independentemente do protocolo de rede que está sendo usado. Com o Winsock, os programadores têm acesso aos recursos de rede avançados da Microsoft® Windows® como multicast e QoS (Qualidade de Serviço).

Winsock segue o Windows WOSA (Open System Architecture). ele define uma SPI (interface de provedor de serviços) padrão entre a API (interface de programação de aplicativo), com suas funções exportadas e as pilhas de protocolo. Ele usa o paradigma de soquetes que foi popularizado pela primeira vez pela BSD (Distribuição de Software de Berkeley) UNIX. Posteriormente, ele foi adaptado para Windows no Windows Sockets 1.1, com os quais os aplicativos Windows Sockets 2 são compatíveis com versões anteriores. A programação winsock foi centralizada anteriormente em torno de TCP/IP. Algumas práticas de programação que funcionaram com TCP/IP não funcionam com todos os protocolos. Como resultado, a API Windows Sockets 2 adiciona funções quando necessário para lidar com vários protocolos.

## <a name="developer-audience"></a>Público de desenvolvedores

Windows Os soquetes 2 foram projetados para uso por programadores C/C++. Familiaridade com Windows rede é necessária.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Windows Os soquetes 2 podem ser usados em todas as Windows plataformas. Quando determinadas implementações ou funcionalidades Windows de plataforma soquetes 2 existem, elas são claramente notadas na documentação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novidades para Windows Sockets](what-s-new-for-windows-sockets-2.md)<br/>                 | Informações sobre novos recursos para soquetes Windows dados.<br/>                                                                                                                                                                                                                                 |
| [Suporte ao protocolo Winsock Network Windows](network-protocol-support-in-windows.md)<br/> | Informações sobre o suporte de protocolo de rede Windows soquetes em diferentes versões do Windows.<br/>                                                                                                                                                                                    |
| [Sobre Winsock](about-winsock.md)<br/>                                                     | Informações gerais sobre Windows de programação de soquetes, arquitetura e funcionalidades disponíveis para desenvolvedores.<br/>                                                                                                                                                       |
| [Usando Winsock](using-winsock.md)<br/>                                                     | Procedimentos e técnicas de programação usados com Windows Sockets. Esta seção inclui técnicas básicas de programação Winsock, como [Ponto de Partida Com Winsock,](getting-started-with-winsock.md)bem como técnicas avançadas úteis para desenvolvedores experientes do Winsock.<br/> |
| [Referência winsock](winsock-reference.md)<br/>                                             | Documentação da API Windows Sockets.<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Auxiliar de IP](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[Qualidade de Serviço](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
