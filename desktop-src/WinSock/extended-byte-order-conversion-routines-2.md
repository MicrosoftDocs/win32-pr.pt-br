---
description: Windows Os soquetes 2 não pressupõem que a ordem de bytes de rede para todos os protocolos seja a mesma.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Rotinas de conversão de Byte-Order estendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2be1c217e89d19e607a64dfc943449351021506dc88f73ebcd4234a26b2b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132519"
---
# <a name="extended-byte-order-conversion-routines"></a>Rotinas de conversão de Byte-Order estendidas

Windows Os soquetes 2 não pressupõem que a ordem de bytes de rede para todos os protocolos seja a mesma. Um conjunto de rotinas de conversão é fornecido para a conversão de quantidades de 16 bits e de 32 bits de e para a ordem de bytes da rede. Essas rotinas assumem como um parâmetro de entrada o identificador de soquete que tem uma estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) associada a ela. O membro **NetworkByteOrder** da estrutura **de \_ informações de WSAPROTOCOL** especifica a ordem de bytes de rede desejada (atualmente big-endian ou little-endian).

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

 

 
