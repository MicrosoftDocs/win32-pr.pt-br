---
description: O Windows Sockets 2 é um conjunto de funções que padroniza a maneira como os aplicativos acessam e usam os vários serviços de nomes de rede.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Registro e resolução de nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773032"
---
# <a name="registration-and-name-resolution"></a>Registro e resolução de nome

O Windows Sockets 2 é um conjunto de funções que padroniza a maneira como os aplicativos acessam e usam os vários serviços de nomes de rede. Ao usar essas funções, os aplicativos não precisam distinguir os protocolos amplamente diferentes associados aos serviços de nome, como DNS, NIS, X. 500, SAP, etc. Para manter a compatibilidade com versões anteriores com o Windows Sockets 1,1, as funções de pesquisa de banco de dados **getXbyY** e assíncronas **WSAAsyncGetXbyY** continuam a ser suportadas, mas são implementadas na interface do provedor de serviços do Windows Sockets em termos de novos recursos de resolução de nomes. Para obter mais informações, consulte as funções [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) . Além disso, consulte [resolução de nome compatível para TCP/IP no SPI do Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).

Esta seção descreve os recursos de registro e resolução de nomes disponíveis para desenvolvedores de Winsock. A lista a seguir descreve os tópicos nesta seção:

-   [Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)
-   [Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Winsock](about-winsock.md)
</dt> <dt>

[Usando o Winsock](using-winsock.md)
</dt> </dl>

 

 



