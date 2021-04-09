---
description: Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente. O uso de soquetes brutos ao portar aplicativos para Winsock não é recomendado por vários motivos.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Soquetes brutos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091308"
---
# <a name="raw-sockets"></a>Soquetes brutos

Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente. O uso de soquetes brutos ao portar aplicativos para Winsock não é recomendado por vários motivos.

A especificação do Windows Sockets não exige que um provedor de serviços Winsock dê suporte a soquetes brutos, ou seja, soquetes do tipo **Sock \_ RAW**. No entanto, os provedores de serviços são incentivados a fornecer suporte a soquetes brutos. Um aplicativo compatível com Windows Sockets que deseja usar soquetes brutos deve tentar abrir o soquete com a chamada de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e, se ele falhar, tentar usar outro tipo de soquete ou indicar a falha para o usuário.

No Windows 7, no Windows Server 2008 R2, no Windows Vista e no Windows XP com Service Pack 2 (SP2), a capacidade de enviar tráfego sobre soquetes brutos foi restrita de várias maneiras. Para obter mais informações, consulte [soquetes brutos TCP/IP](tcp-ip-raw-sockets-2.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**SSA**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[Soquetes brutos TCP/IP](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



