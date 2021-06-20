---
title: Bloco de rascunho de toque do Windows usando o exemplo de caneta Real-Time (C#)
description: Examine um exemplo de C# do Windows Touch (MTScratchpadRTStylus), que mostra como usar as mensagens do Windows Touch para desenhar rastreamentos de pontos de toque em uma janela.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch, exemplos de código
- Windows Touch, código de exemplo
- Windows Touch, amostras de bloco de rascunho
- Amostras de bloco de rascunho
- Windows Touch, objeto de caneta em tempo real (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 3c30d3543024a48394ddd7b9b2b06a05b61f5025
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406309"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Bloco de rascunho de toque do Windows usando o exemplo de caneta Real-Time (C#)

O exemplo de bloco de rascunho do Windows ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) mostra como usar mensagens de toque do Windows para desenhar rastreamentos dos pontos de toque em uma janela. O rastreamento do dedo principal, aquele que foi colocado no digitalizador primeiro, é desenhado em preto. Os dedos secundários são desenhados em seis outras cores: vermelho, verde, azul, ciano, magenta e amarelo. A captura de tela a seguir mostra como o aplicativo pode ser examinado durante a execução.

![captura de tela mostrando o exemplo de bloco de rascunho de toque do Windows usando a caneta em tempo real em c Sharp, com rabiscos pretos e vermelhos na tela](images/mtscratchpadrtstyluscs.png)

Para este exemplo, o objeto de Real-Time Stylus (RTS) é criado e o suporte para vários pontos de contato está habilitado. Um plug-in DynamicRenderer é adicionado ao RTS para renderizar o conteúdo. Um plug-in, EventHandlerPlugIn, é implementado para rastrear o número de dedos e alterar a cor que o renderizador dinâmico está desenhando. Com ambos os plug-ins na pilha de plug-in de RTS, o aplicativo de bloco de rascunho do Windows irá renderizar o contato principal em preto e o restante dos contatos nas várias cores.

O código a seguir mostra como o EventHandlerPlugIn incrementa e decrementa uma contagem do número de contatos e define a cor do renderizador dinâmico.

```CSharp
        public void StylusDown(RealTimeStylus sender, StylusDownData data)
        {
            // Set new stroke color to the DrawingAttributes of the DynamicRenderer
            // If there are no fingers down, this is a primary contact
            dynamicRenderer.DrawingAttributes.Color = touchColor.GetColor(cntContacts == 0);

            ++cntContacts;  // Increment finger-down counter
        }

        public void StylusUp(RealTimeStylus sender, StylusUpData data)
        {
            --cntContacts;  // Decrement finger-down counter
        }
```

O código a seguir mostra como o RTS é criado com o suporte a vários pontos de contato.

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            // Create RealTimeStylus object and enable it for multi-touch
            realTimeStylus = new RealTimeStylus(this);
            realTimeStylus.MultiTouchEnabled = true;

            // Create DynamicRenderer and event handler, and add them to the RTS object as synchronous plugins
            dynamicRenderer = new DynamicRenderer(this);
            eventHandler = new EventHandlerPlugIn(this.CreateGraphics(), dynamicRenderer);
            realTimeStylus.SyncPluginCollection.Add(eventHandler);
            realTimeStylus.SyncPluginCollection.Add(dynamicRenderer);

            // Enable RTS and DynamicRenderer object, and enable auto-redraw of the DynamicRenderer
            realTimeStylus.Enabled = true;
            dynamicRenderer.Enabled = true;
            dynamicRenderer.EnableDataCache = true;
        }
```

Depois que a cor do objeto DynamicRenderer tiver sido alterada e os traços tiverem sido desenhados, uma chamada para DynamicRenderer:: Refresh fará com que os novos traços sejam exibidos. O código a seguir mostra como isso é executado no método OnPaintHandler.

```CSharp
        private void OnPaintHandler(object sender, PaintEventArgs e)
        {
            // Erase the background
            Brush brush = new SolidBrush(SystemColors.Window);
            e.Graphics.FillRectangle(brush, ClientRectangle);

            // Ask DynamicRenderer to redraw itself
            dynamicRenderer.Refresh();
        }
```

## <a name="related-topics"></a>Tópicos relacionados

[Aplicativo de bloco de rascunho multitoque (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [aplicativo de bloco de rascunho multitoque (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [exemplos de toque do Windows](windows-touch-samples.md)
