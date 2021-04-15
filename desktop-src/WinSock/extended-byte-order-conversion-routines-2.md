---
description: O Windows Sockets 2 não pressupõe que a ordem de bytes de rede para todos os protocolos seja a mesma.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Rotinas de conversão de Byte-Order estendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501699"
---
# <a name="extended-byte-order-conversion-routines"></a>Rotinas de conversão de Byte-Order estendidas

O Windows Sockets 2 não pressupõe que a ordem de bytes de rede para todos os protocolos seja a mesma. Um conjunto de rotinas de conversão é fornecido para a conversão de quantidades de 16 bits e de 32 bits de e para a ordem de bytes da rede. Essas rotinas assumem como um parâmetro de entrada o identificador de soquete que tem uma estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) associada a ela. O membro **NetworkByteOrder** da estrutura **de \_ informações de WSAPROTOCOL** especifica a ordem de bytes de rede desejada (atualmente big-endian ou little-endian).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[**informações de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
