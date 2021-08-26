---
description: Ao transformar o código de atualização da célula de vida, várias diretrizes para escrever aplicativos de rede de alto desempenho foram descobertas.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Práticas recomendadas para aplicativos interativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497fc56419f8859b7490671590b4589092c4c5b37047a01b0bf80cee9bf8c213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996896"
---
# <a name="best-practices-for-interactive-applications"></a>Práticas recomendadas para aplicativos interativos

Ao transformar o código de atualização da célula de vida, várias diretrizes para escrever aplicativos de rede de alto desempenho foram descobertas. Algumas estratégias gerais a serem aplicadas ao escrever esses tipos de aplicativos são:

-   Torne o fluxo de dados o máximo possível, em vez de entrar em partes.
-   Use algumas transações grandes em vez de muitas pequenas. As transações grandes também podem ser transmitidas com eficiência.
-   Reconheça que a rede é um recurso lento e não confiável e desenvolva cada aplicativo para minimizar sua dependência na rede.
-   Use uma representação bem arquitetada dos dados na rede. A representação de dados deve ser independente da arquitetura do computador, não conter FAT e possivelmente compactada.
-   Durante a inicialização e o desligamento, não faça o usuário esperar que a rede seja inicializada ou desligada. A inicialização relacionada à rede pode levar um tempo relativamente longo. Separe o código de rede não crítico.
-   Manipule erros conforme apropriado para seu impacto. Nem todos os erros são críticos. Implemente mecanismos de recuperação e forneça comentários de usuários não intrusivos.
-   Use RPC (chamadas de procedimento remoto) somente quando apropriado. o RPC é síncrono no Windows Me/98 e sempre resulta em protocolos de fat informais quando usados para enviar pequenas quantidades de dados.
-   Meça sua sobrecarga de rede usando netstat; Você pode ficar surpreso com o que suas medidas revelam.
-   Teste o aplicativo em uma variedade de redes, especialmente redes lentas ou sujeitas a perda. Redes LAN sem fio, Modems e VPN (redes virtuais privadas) pela Internet são boas redes para teste.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[aplicativos de alto desempenho Windows sockets](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



