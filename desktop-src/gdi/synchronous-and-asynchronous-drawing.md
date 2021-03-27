---
description: A maioria dos desenhos realizados durante o processamento da \_ mensagem de pintura do WM é assíncrona; ou seja, há um atraso entre o tempo em que uma parte da janela é invalidada e a hora em que o WM \_ Paint é enviado.
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: Desenho síncrono e assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80dd5d5d63cbe10d19ec98e9f5dc9ae9163c18a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922573"
---
# <a name="synchronous-and-asynchronous-drawing"></a>Desenho síncrono e assíncrono

A maioria dos desenhos realizados durante o processamento da mensagem de [**\_ pintura do WM**](wm-paint.md) é assíncrona; ou seja, há um atraso entre o tempo em que uma parte da janela é invalidada e a hora em que o WM \_ Paint é enviado. Durante o atraso, o aplicativo normalmente recupera mensagens da fila e executa outras tarefas. O motivo do atraso é que o sistema geralmente trata o desenho em uma janela como uma operação de baixa prioridade e funciona como se mensagens de entrada do usuário e mensagens que podem afetar a posição ou o tamanho de uma janela sejam processados antes do WM \_ Paint.

Em alguns casos, é necessário que um aplicativo desenhe de forma síncrona ou seja, desenhe na janela imediatamente após a invalidação de uma parte da janela. Um aplicativo típico desenha sua janela principal imediatamente após a criação da janela para sinalizar ao usuário que o aplicativo foi iniciado com êxito. O sistema desenha algumas janelas de controle de forma síncrona, como botões, porque essas janelas servem como foco para a entrada do usuário. Embora qualquer janela com uma rotina de desenho simples possa ser desenhada de forma síncrona, todo esse desenho deve ser feito rapidamente e não deve interferir na capacidade do aplicativo de responder à entrada do usuário.

As funções [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) e [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) permitem o desenho síncrono. **UpdateWindow** envia uma mensagem do [**WM \_ Paint**](wm-paint.md) diretamente para a janela se a região de atualização não estiver vazia. O **RedrawWindow** também envia uma mensagem de **\_ pintura do WM** , mas dá ao aplicativo um maior controle sobre como desenhar a janela, por exemplo, se deseja desenhar a área não cliente e o plano de fundo da janela ou se deseja enviar a mensagem independentemente se a região de atualização está vazia. Essas funções enviam a mensagem do **WM \_ Paint** diretamente para a janela, independentemente do número de outras mensagens na fila de mensagens do aplicativo.

Qualquer janela que exija operações demoradas de desenho deve ser desenhada de forma assíncrona para impedir que mensagens pendentes sejam bloqueadas à medida que a janela é desenhada. Além disso, qualquer aplicativo que, com frequência, invalida pequenas partes de uma janela deve permitir que essas partes inválidas sejam consolidadas em uma única mensagem assíncrona de [**\_ pintura do WM**](wm-paint.md) , em vez de uma série de mensagens de **\_ pintura do WM** síncronas.

 

 



