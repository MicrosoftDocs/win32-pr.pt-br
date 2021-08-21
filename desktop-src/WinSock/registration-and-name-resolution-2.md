---
description: Windows Soquetes 2 é um conjunto de funções que padroniza a maneira como os aplicativos acessam e usam os vários serviços de nomenização de rede.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Registro e resolução de nomes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1ef16357a30ff567fd2c7c9e1b8a24a93e80635eacca5319ae166e91033372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111729"
---
# <a name="registration-and-name-resolution"></a>Registro e resolução de nomes

Windows Soquetes 2 é um conjunto de funções que padroniza a maneira como os aplicativos acessam e usam os vários serviços de nomenização de rede. Ao usar essas funções, os aplicativos não precisam distinguir os protocolos amplamente diferentes associados a serviços de nome, como DNS, NIS, X.500, SAP etc. Para manter a compatibilidade completa com compatibilidade com conexões com o Windows Sockets 1.1, as funções **getXbyY** e assíncrona **WSAAsyncGetXbyY** de banco de dados continuam a ter suporte, mas são implementadas na interface do provedor de serviços do Windows Sockets em termos dos novos recursos de resolução de nomes. Para obter mais informações, consulte [**as funções getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) [**e getservbyport.**](/windows/desktop/api/winsock/nf-winsock-getservbyport) Além disso, [consulte Resolução de nomes compatíveis para TCP/IP na SPI Windows Soquetes 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).

Esta seção descreve os recursos de registro e resolução de nomes disponíveis para desenvolvedores do Winsock. A lista a seguir descreve os tópicos nesta seção:

-   [Resolução de nomes independentes de protocolo](protocol-independent-name-resolution-2.md)
-   [Resolução de nomes compatível para TCP/IP na API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Winsock](about-winsock.md)
</dt> <dt>

[Usando Winsock](using-winsock.md)
</dt> </dl>

 

 



