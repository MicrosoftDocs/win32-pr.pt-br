---
description: SPI (interface do provedor de serviços) do Windows Sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: SPI do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752215"
---
# <a name="winsock-spi"></a>SPI do Winsock

A interface do provedor de serviço do Winsock ou SPI do Winsock é uma disciplina especializada do Winsock usada para criar provedores; provedores de transporte, como as pilhas de protocolo TCP/IP ou IPX/SPX, usam a SPI do Winsock, como os provedores de namespace, como o DNS (sistema de cadastramento de domínio) da Internet.

Programação de rede tradicional, como permitir que aplicativos se comuniquem pela rede, não requer o uso de interfaces do Winsock SPI; em vez disso, use as interfaces padrão do [Winsock](winsock-reference.md) .

 

A SPI do Winsock usa a seguinte convenção de nomenclatura de prefixo de função.



| Prefixo | Significado                          | Descrição                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Provedor de serviços do Windows Sockets | Pontos de entrada do provedor de serviço de transporte           |
| WPU    | Upchamada do provedor do Windows Sockets  | Ws2 \_ pontos de entrada de32.dll para provedores de serviço    |
| WSC    | Configuração do Windows Sockets    | WS2 \_ pontos de entrada de32.dll para miniaplicativos de instalação |
| NSP    | Provedor de namespace               | Pontos de entrada do provedor de namespace                   |



 

 

 



