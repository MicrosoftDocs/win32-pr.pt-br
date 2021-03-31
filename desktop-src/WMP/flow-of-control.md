---
title: Fluxo de controle
description: Fluxo de controle
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- visualizações, fluxo de programa
- visualizações personalizadas, fluxo do programa
- visualizações, fluxo de controle
- visualizações personalizadas, fluxo de controle
- visualizações, eventos cronometrados
- visualizações personalizadas, eventos cronometrados
- visualizações, função render
- visualizações personalizadas, função render
- visualizações, função RenderWindow
- visualizações personalizadas, função RenderWindow
- Função render, fluxo do programa de visualização
- Função RenderWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916032"
---
# <a name="flow-of-control"></a>Fluxo de controle

Os dados de áudio entram no Windows Media Player continuamente por meio de um arquivo ou fluxo. Esses dados são passados para sua visualização. Você desenha em uma superfície definida e passa essa superfície de volta para o Windows Media Player. Esse intercâmbio ocorre várias vezes por segundo e, para o usuário, o resultado é uma animação agradável que se move em tempo para a música.

Aqui está a sequência específica do fluxo do programa de visualização:

1.  Em um intervalo de tempo, o Windows Media Player tira um instantâneo do áudio que está sendo executado.
2.  O Windows Media Player fornece os dados desse instantâneo para sua visualização por meio da função **render** e da função **RenderWindowed** .
3.  Você deve escrever o código que será executado quando **render** e **RenderWindowed** for chamado. Seu código desenha usando um contexto de dispositivo definido pelo Windows Media Player ao renderizar sem janela ou usando uma janela que você cria ao renderizar janelas.
4.  Em uma região especificada pela aparência atual, o Windows Media Player exibe o que seu código desenhou.
5.  Esse processo se repete várias vezes por segundo, criando animações gráficas que são cronometradas para a música. Quando a música pára de ser reproduzida, a visualização é interrompida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor**](developer-overview.md)
</dt> </dl>

 

 




