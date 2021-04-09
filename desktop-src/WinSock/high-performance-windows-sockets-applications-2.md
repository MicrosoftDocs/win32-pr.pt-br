---
description: Os componentes de rede do Microsoft Windows foram desenvolvidos para desempenho e escalabilidade.
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: Aplicativos de alto desempenho do Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0496198ef3a8f11e6a840fd75d0083899d23d5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010490"
---
# <a name="high-performance-windows-sockets-applications"></a>Aplicativos de alto desempenho do Windows Sockets

Os componentes de rede do Microsoft Windows foram desenvolvidos para desempenho e escalabilidade. Isso permite que os aplicativos maximizem a largura de banda de rede disponível. O Windows Sockets e a pilha do protocolo TCP/IP do Windows foram ajustados e simplificados. Como resultado, os aplicativos do Windows devidamente escritos podem alcançar uma taxa de transferência e desempenho excepcionais, como ilustram os seguintes fatos:

-   O Windows é capaz de atender mais de 200.000 conexões TCP simultâneas.
-   Em um teste conduzido pelo SPECWeb96, o Internet Information Server no Windows foi atendido em mais de 25.000 solicitações HTTP por segundo.
-   O Windows definiu um registro de transmissão de mais de 750Mbps em uma rede de transcontinental Gigabit que consiste em 10 saltos.

Essas conquistas ilustram que o TCP/IP do Windows processa dados muito rapidamente. Muitos aplicativos, no entanto, não aproveitam os recursos de desempenho do Windows, TCP/IP e Windows Sockets porque eles implementam inadvertidamente técnicas de dificultação de desempenho.

Neste guia, você aprenderá a identificar erros comuns de programação e como evitá-los. Em seguida, você aprenderá técnicas que permitem que os aplicativos do Windows Sockets sejam executados de forma ideal. Este guia é apresentado em seis seções. A ordem das seções é intencional; para obter o máximo deste guia, leia-o em ordem. A tabela a seguir fornece links para cada seção, bem como uma breve descrição de cada tópico.



| Tópico                                                                                            | Descrição                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Terminologia de rede](network-terminology-2.md)                                                 | Define a terminologia e as métricas de rede necessárias para a compreensão do desempenho de um aplicativo de rede.                                     |
| [Dimensões de desempenho](performance-dimensions-2.md)                                           | Discute as dimensões de desempenho que afetam o desempenho de rede percebido e real de um aplicativo.                                        |
| [Características de TCP/IP](tcp-ip-characteristics-2.md)                                           | Define as características do protocolo TCP/IP que podem resultar em problemas de desempenho para um aplicativo mal escrito.                                     |
| [Comportamento do aplicativo](application-behavior-2.md)                                               | Explica como reconhecer os sinais de um aplicativo de rede com mau desempenho.                                                                     |
| [Melhorando um aplicativo lento](improving-a-slow-application-2.md)                               | Fornece exemplos de problemas de design de aplicativo que contribuem para um aplicativo de desempenho insatisfatório e fazem alterações no código para melhorar o desempenho. |
| [Práticas recomendadas para aplicativos interativos](best-practices-for-interactive-applications-2.md) | Lista as práticas recomendadas a serem empregadas para o desenvolvimento de aplicativos de rede interativa ideais.                                                         |



 

 

 



