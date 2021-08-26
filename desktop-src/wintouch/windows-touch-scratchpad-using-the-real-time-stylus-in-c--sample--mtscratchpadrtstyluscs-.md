---
title: Windows Toque em Scratchpad usando Real-Time exemplo de caneta (C#)
description: Revise um exemplo Windows touch scratchpad C# (MTSqueichpadRTStylus), que mostra como usar mensagens Windows Touch para desenhar rastreamentos dos pontos de toque para uma janela.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Toque, exemplos de código
- Windows Toque, código de exemplo
- Windows Toque, exemplos do Scratchpad
- Exemplos de bloco de rascunho
- Windows Touch, objeto RTS (Caneta em Tempo Real)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: a76f7a66f8bc26b7e1cad8f1fa71d9703f0c0da1ad1452a078b374a0f1603238
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055837"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows Toque em Scratchpad usando Real-Time exemplo de caneta (C#)

O exemplo Windows Touch Scratchpad ([MTSqueichpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) mostra como usar mensagens Windows Touch para desenhar rastreamentos dos pontos de toque para uma janela. O rastreamento do dedo primário, aquele que foi colocado primeiro no digitalizador, é desenhado em preto. Os dedos secundários são desenhados em seis outras cores: vermelho, verde, azul, ciano, magenta e amarelo. A captura de tela a seguir mostra a aparência do aplicativo durante a execução.

![captura de tela mostrando o exemplo de bloco de rascunho de toque do Windows usando a caneta em tempo real em c sharp, com alternâncias pretas e vermelhas na tela](images/mtscratchpadrtstyluscs.png)

Para este exemplo, o objeto Real-Time caneta (RTS) é criado e o suporte para vários pontos de contato está habilitado. Um plug-in DynamicRenderer é adicionado ao RTS para renderizar o conteúdo. Um plug-in, EventHandlerPlugIn, é implementado para rastrear o número de dedos e alterar a cor que o renderador dinâmico está desenhando. Com ambos os plug-ins na pilha de plug-in RTS, o aplicativo Windows Touch Scratchpad renderizará o contato principal em preto e o restante dos contatos nas várias cores.

O código a seguir mostra como EventHandlerPlugIn incrementa e diminui uma contagem do número de contatos e define a cor do renderador dinâmico.

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

O código a seguir mostra como o RTS é criado com suporte a vários pontos de contato.

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

Depois que a cor do objeto DynamicRenderer tiver sido alterada e os traços foram desenhados, uma chamada para DynamicRenderer::Refresh fará com que os novos traços apareçam. O código a seguir mostra como isso é executado no método OnPaintHandler.

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

[Aplicativo RTS/C#, RTS(Multi](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS) [touch Scratchpad Application) , RTS/C++),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp) [Windows de](windows-touch-samples.md) toque
