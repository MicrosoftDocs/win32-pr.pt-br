---
description: Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente. O uso de soquetes brutos ao portar aplicativos para Winsock não é recomendado por vários motivos.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Soquetes brutos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c1522c2b8499e2ba8f1bb693513105804ec936fc2224fccaa55dd90a1b0dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740530"
---
# <a name="raw-sockets"></a>Soquetes brutos

Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente. O uso de soquetes brutos ao portar aplicativos para Winsock não é recomendado por vários motivos.

a especificação de soquetes Windows não exige que um provedor de serviços Winsock dê suporte a soquetes brutos, ou seja, soquetes do tipo **SOCK \_ raw**. No entanto, os provedores de serviços são incentivados a fornecer suporte a soquetes brutos. um aplicativo compatível com soquetes Windows que deseja usar soquetes brutos deve tentar abrir o soquete com a chamada de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e, se ele falhar, tentar usar outro tipo de soquete ou indicar a falha para o usuário.

no Windows 7, Windows Server 2008 R2, Windows Vista e Windows XP com Service Pack 2 (SP2), a capacidade de enviar tráfego sobre soquetes brutos foi restrita de várias maneiras. Para obter mais informações, consulte [soquetes brutos TCP/IP](tcp-ip-raw-sockets-2.md).

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

 

 



