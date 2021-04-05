---
description: A arquitetura do Windows Sockets 2 (Winsock) é compatível com a arquitetura do sistema aberto do Windows (WOSA).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Arquitetura do Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091004"
---
# <a name="windows-sockets-2-architecture"></a>Arquitetura do Windows Sockets 2

A arquitetura do Windows Sockets 2 é compatível com a WOSA (arquitetura de sistema aberto do Windows), conforme ilustrado abaixo:

![arquitetura do Windows Sockets 2](images/ovrvw2-1.png)

O Winsock define uma SPI (interface de provedor de serviços) padrão entre a API (interface de programação de aplicativo), com suas funções exportadas de WS2 \_32.dll e as pilhas de protocolo. Consequentemente, o suporte a Winsock não está limitado a pilhas de protocolo TCP/IP como é o caso do Windows Sockets 1,1.

Com a arquitetura do Windows Sockets 2, não é necessário ou desejável, para que os fornecedores de pilha forneçam sua própria implementação de WS2 \_32.dll, já que uma única WS2 \_32.dll deve funcionar em todas as pilhas. O \_32.dll Ws2 e os shims de compatibilidade devem ser exibidos da mesma maneira que um componente do sistema operacional.

 

 



