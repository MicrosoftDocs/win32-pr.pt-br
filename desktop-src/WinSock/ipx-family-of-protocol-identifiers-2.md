---
description: O parâmetro de protocolo em Socket e WSASocket é um identificador que estabelece um tipo de rede e um método para identificar os vários protocolos de transporte executados na rede.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Família IPX de identificadores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090379"
---
# <a name="ipx-family-of-protocol-identifiers"></a>Família IPX de identificadores de protocolo

O parâmetro de *protocolo* em [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) é um identificador que estabelece um tipo de rede e um método para identificar os vários protocolos de transporte executados na rede. Ao contrário do IP, o IPX não usa um valor de protocolo único para selecionar uma pilha de transporte. Como não há nenhum requisito de rede para usar um valor específico para cada protocolo de transporte, estamos livres para atribuí-los de maneira conveniente para aplicativos Winsock. Evitamos valores de 0 a 255 para evitar colisões com os valores de protocolo de PF \_ inet correspondentes.



| Nome         | Valor       | Tipos de soquete              | Descrição                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| Reservado     | 0-255       |                           | Reservado para valores de protocolo de PF \_ inet.              |
| NSPROTO \_ IPX | 1000-1255 | SOCK \_ DGRAM Sock \_ RAW     | Serviço de datagrama para IPX.                           |
| NSPROTO \_ SPX | 1256        | SOCK \_ Stream Sock \_ SEQPKT | Troca de pacotes confiável usando pacotes de tamanho fixo. |



 

> [!Note]  
> Quando NSPROTO \_ SPX for especificado, o protocolo SPX II será automaticamente utilizado se ambos os pontos de extremidade forem capazes de fazer isso.

 

 

 



