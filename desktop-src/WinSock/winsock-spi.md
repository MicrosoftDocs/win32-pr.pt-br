---
description: Windows Spi (Interface do Provedor de Serviços) sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec29ad26d97b62c884d2944b31d54c94ea1f61b02f74de28c6ff4c84acc6a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051324"
---
# <a name="winsock-spi"></a>Winsock SPI

A Interface do Provedor de Serviços Winsock, ou SPI winsock, é uma disciplina especializada do Winsock usada para criar provedores; provedores de transporte, como pilhas de protocolo TCP/IP ou IPX/SPX, usam a SPI winsock, assim como provedores de namespace, como o DNS (Sistema de Nomenal de Domínio) da Internet.

A programação de rede tradicional, como permitir que aplicativos se comuniquem pela rede, não exige o uso de interfaces spi winsock; em vez disso, use interfaces [Winsock](winsock-reference.md) padrão.

 

A SPI winsock usa a seguinte convenção de nomen por prefixo de função.



| Prefixo | Significado                          | Descrição                                       |
|--------|----------------------------------|---------------------------------------------------|
| Wsp    | Windows Provedor de Serviços de Soquetes | Pontos de entrada do provedor de serviços de transporte           |
| WPU    | Windows Chamada de upcall do provedor de soquetes  | Ws2 \_32.dll de entrada para provedores de serviços    |
| Wsc    | Windows Configuração de soquetes    | Pontos de entrada \_32.dll WS2 para applets de instalação |
| Nsp    | Provedor de namespace               | Pontos de entrada do provedor de namespace                   |



 

 

 



