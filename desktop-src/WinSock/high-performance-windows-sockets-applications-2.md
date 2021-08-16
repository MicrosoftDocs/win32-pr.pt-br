---
description: Os Windows de rede da Microsoft foram desenvolvidos para desempenho e escalabilidade.
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: Aplicativos de soquetes Windows de alto desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df2b050ac45bf0bf7788a356f4fdba98197d481dd99180f99f7dbf8cdfb5b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927865"
---
# <a name="high-performance-windows-sockets-applications"></a>Aplicativos de soquetes Windows de alto desempenho

Os Windows de rede da Microsoft foram desenvolvidos para desempenho e escalabilidade. Isso permite que os aplicativos maximizem a largura de banda de rede disponível. Windows Os soquetes e Windows de protocolo TCP/IP foram ajustados e simplificados. Como resultado, os aplicativos de Windows podem obter uma produtividade e desempenho excepcionais, como ilustram os seguintes fatos:

-   Windows é capaz de atender a mais de 200.000 conexões TCP simultâneas.
-   Em um teste realizado por SPECWeb96, o Servidor de Informações da Internet Windows a serviço mais de 25.000 solicitações HTTP por segundo.
-   Windows um registro de transmissão de mais de 750 Mbps em uma rede gigabit transcontinental que consiste em 10 saltos.

Essas conquistas ilustram que Windows TCP/IP processa dados muito rapidamente. Muitos aplicativos, no entanto, não aproveitam as funcionalidades de desempenho Windows, TCP/IP e Windows Sockets porque implementam técnicas que dificultam o desempenho sem saber.

Neste guia, você aprenderá a identificar erros comuns de programação e como evitá-los. Em seguida, você aprenderá técnicas que permitem que Windows de soquetes executem o ideal. Este guia é apresentado em seis seções. A ordem das seções é intencional; para obter o máximo deste guia, leia-o em ordem. A tabela a seguir fornece links para cada seção, bem como uma breve descrição de cada tópico.



| Tópico                                                                                            | Descrição                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Terminologia de rede](network-terminology-2.md)                                                 | Define a terminologia de rede e as métricas necessárias para entender o desempenho de um aplicativo de rede.                                     |
| [Dimensões de desempenho](performance-dimensions-2.md)                                           | Discute dimensões de desempenho que afetam o desempenho de rede percebido e real de um aplicativo.                                        |
| [Características de TCP/IP](tcp-ip-characteristics-2.md)                                           | Define características de protocolo TCP/IP que podem resultar em problemas de desempenho para um aplicativo mal escrito.                                     |
| [Comportamento do aplicativo](application-behavior-2.md)                                               | Explica como reconhecer os sinais de um aplicativo de rede de baixo desempenho.                                                                     |
| [Melhorando um aplicativo lento](improving-a-slow-application-2.md)                               | Fornece exemplos de problemas de design de aplicativo que contribuem para um aplicativo de baixo desempenho e faz alterações no código para melhorar o desempenho. |
| [Práticas recomendadas para aplicativos interativos](best-practices-for-interactive-applications-2.md) | Lista as práticas recomendadas a empregar para desenvolver aplicativos de rede interativos ideais.                                                         |



 

 

 



