---
description: Ao transformar o código de atualização da célula de vida, várias diretrizes para escrever aplicativos de rede de alto desempenho foram descobertas.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Práticas recomendadas para aplicativos interativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771356"
---
# <a name="best-practices-for-interactive-applications"></a>Práticas recomendadas para aplicativos interativos

Ao transformar o código de atualização da célula de vida, várias diretrizes para escrever aplicativos de rede de alto desempenho foram descobertas. Algumas estratégias gerais a serem aplicadas ao escrever esses tipos de aplicativos são:

-   Torne o fluxo de dados o máximo possível, em vez de entrar em partes.
-   Use algumas transações grandes em vez de muitas pequenas. As transações grandes também podem ser transmitidas com eficiência.
-   Reconheça que a rede é um recurso lento e não confiável e desenvolva cada aplicativo para minimizar sua dependência na rede.
-   Use uma representação bem arquitetada dos dados na rede. A representação de dados deve ser independente da arquitetura do computador, não conter FAT e possivelmente compactada.
-   Durante a inicialização e o desligamento, não faça o usuário esperar que a rede seja inicializada ou desligada. A inicialização relacionada à rede pode levar um tempo relativamente longo. Separe o código de rede não crítico.
-   Manipule erros conforme apropriado para seu impacto. Nem todos os erros são críticos. Implemente mecanismos de recuperação e forneça comentários de usuários não intrusivos.
-   Use RPC (chamadas de procedimento remoto) somente quando apropriado. O RPC é síncrono no Windows me/98 e sempre resulta em protocolos de Fat informais quando usados para enviar pequenas quantidades de dados.
-   Meça sua sobrecarga de rede usando netstat; Você pode ficar surpreso com o que suas medidas revelam.
-   Teste o aplicativo em uma variedade de redes, especialmente redes lentas ou sujeitas a perda. Redes LAN sem fio, Modems e VPN (redes virtuais privadas) pela Internet são boas redes para teste.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de alto desempenho do Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



