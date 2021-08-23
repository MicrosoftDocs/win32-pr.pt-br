---
description: A arquitetura Windows Sockets 2 (Winsock) está em conformidade com o WOSA (Windows Open System Architecture).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Windows Arquitetura de soquetes 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ad3dd29f692df94e1f66c13c00c75eeca36fb04d18c5f2e95e67b91773698f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569146"
---
# <a name="windows-sockets-2-architecture"></a>Windows Arquitetura de soquetes 2

A Windows de soquetes 2 está em conformidade com a WOSA (arquitetura de sistema aberto) do Windows, conforme ilustrado abaixo:

![arquitetura do Windows Sockets 2](images/ovrvw2-1.png)

Winsock define uma SPI (interface de provedor de serviços) padrão entre a API (interface de programação de aplicativo), com suas funções exportadas do WS232.dll e as pilhas \_ de protocolo. Consequentemente, o suporte ao Winsock não está limitado a pilhas de protocolo TCP/IP, como é o caso do Windows Sockets 1.1.

Com a arquitetura Windows Sockets 2, não é necessário ou desejável que os fornecedores de pilha fornecem sua própria implementação do WS232.dll, já que um único32.dll WS2 deve funcionar em todas as \_ \_ pilhas. Os shims de32.dll WS2 e compatibilidade devem ser exibidos da \_ mesma maneira que um componente do sistema operacional.

 

 



