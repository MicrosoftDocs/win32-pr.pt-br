---
title: Flow de controle
description: Flow de controle
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
ms.openlocfilehash: 332d9c907e7c25f81d01bc8adf48c6d4d91a7b17763a1b0daf0007a8534ac4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934735"
---
# <a name="flow-of-control"></a>Flow de controle

os dados de áudio entram em Windows Media Player continuamente por meio de um arquivo ou fluxo. Esses dados são passados para sua visualização. Você desenha em uma superfície definida e passa essa superfície de volta para Windows Media Player. Esse intercâmbio ocorre várias vezes por segundo e, para o usuário, o resultado é uma animação agradável que se move em tempo para a música.

Aqui está a sequência específica do fluxo do programa de visualização:

1.  em um intervalo de tempo, Windows Media Player captura um instantâneo do áudio que está sendo executado.
2.  Windows Media Player fornece os dados desse instantâneo para sua visualização por meio da função **Render** e da função **RenderWindowed** .
3.  Você deve escrever o código que será executado quando **render** e **RenderWindowed** for chamado. seu código desenha usando um contexto de dispositivo definido por Windows Media Player ao renderizar sem janela ou usando uma janela que você cria ao renderizar janelas.
4.  em uma região especificada pela capa atual, Windows Media Player exibe o que o código desenhou.
5.  Esse processo se repete várias vezes por segundo, criando animações gráficas que são cronometradas para a música. Quando a música pára de ser reproduzida, a visualização é interrompida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor**](developer-overview.md)
</dt> </dl>

 

 




