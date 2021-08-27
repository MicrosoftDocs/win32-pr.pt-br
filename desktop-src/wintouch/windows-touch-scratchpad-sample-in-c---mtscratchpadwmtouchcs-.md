---
title: Windows Exemplo de bloco de rascunho de toque em C (MTScratchpadWMTouchCS)
description: o exemplo de bloco de rascunho Windows touch em C# mostra como usar Windows toque de mensagens para desenhar rastreamentos dos pontos de toque em uma janela.
ms.assetid: 652124be-01a8-4df4-b590-e5c2ca3f012c
keywords:
- Windows Toque, exemplos de código
- Windows Toque, código de exemplo
- Windows Toque, amostras de bloco de rascunho
- Amostras de bloco de rascunho
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 112f8446af4b845bfd36e4262a11da807535c93baaf6257a10a9a8d2b03374e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089837"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Windows Exemplo de bloco de rascunho de toque (C#)

o [exemplo de bloco de rascunho Windows touch em C#](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS) mostra como usar Windows toque de mensagens para desenhar rastreamentos dos pontos de toque em uma janela. O rastreamento do dedo principal, aquele que foi colocado no digitalizador primeiro, é desenhado em preto. Os dedos secundários são desenhados em seis outras cores: vermelho, verde, azul, ciano, magenta e amarelo. A imagem a seguir mostra como o aplicativo pode ser exibido ao ser executado.

![captura de tela que mostra o exemplo de bloco de rascunho de toque do Windows em c Sharp, com preto, verde, azul e ondulado vermelho na tela](images/mtscratchpadwmtouchcs.png)

Para este exemplo, um formulário de toque é criado para manipular [**WM_TOUCH**](wm-touchdown.md) mensagens. esse formulário é herdado para habilitar Windows toque no aplicativo de bloco de rascunho. Quando as mensagens de **WM_TOUCH** chegam ao formulário, elas são interpretadas em pontos e adicionadas à coleção de traços. A coleção Strokes é renderizada para o objeto Graphics. O código a seguir mostra como o formulário tocável se registra para manipular **WM_TOUCH** mensagens e como ele lida com **WM_TOUCH** mensagens.

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            try
            {
                // Registering the window for multi-touch, using the default settings.
                // p/invoking into user32.dll
                if (!RegisterTouchWindow(this.Handle, 0))
                {
                    Debug.Print("ERROR: Could not register window for multi-touch");
                }
            }
            catch (Exception exception)
            {
                Debug.Print("ERROR: RegisterTouchWindow API not available");
                Debug.Print(exception.ToString());
                MessageBox.Show("RegisterTouchWindow API not available", "MTScratchpadWMTouch ERROR",
                    MessageBoxButtons.OK, MessageBoxIcon.Error, MessageBoxDefaultButton.Button1, 0);
            }
        }
(...)
        [PermissionSet(SecurityAction.Demand, Name = "FullTrust")]
        protected override void WndProc(ref Message m)
        {
            // Decode and handle WM_TOUCH message.
            bool handled;
            switch (m.Msg)
            {
                case WM_TOUCH:
                    handled = DecodeTouch(ref m);
                    break;
                default:
                    handled = false;
                    break;
            }

            // Call parent WndProc for default message processing.
            base.WndProc(ref m);

            if (handled)
            {
                // Acknowledge event if handled.
                m.Result = new System.IntPtr(1);
            }
        }
```

o código a seguir mostra como a mensagem de toque Windows é interpretada e os dados são adicionados às coleções de traços.

```CSharp
        private bool DecodeTouch(ref Message m)
        {
            // More than one touchinput may be associated with a touch message,
            // so an array is needed to get all event information.
            int inputCount = LoWord(m.WParam.ToInt32()); // Number of touch inputs, actual per-contact messages

            TOUCHINPUT[] inputs; // Array of TOUCHINPUT structures
            inputs = new TOUCHINPUT[inputCount]; // Allocate the storage for the parameters of the per-contact messages

            // Unpack message parameters into the array of TOUCHINPUT structures, each
            // representing a message for one single contact.
            if (!GetTouchInputInfo(m.LParam, inputCount, inputs, touchInputSize))
            {
                // Get touch info failed.
                return false;
            }

            // For each contact, dispatch the message to the appropriate message
            // handler.
            bool handled = false; // Boolean, is message handled
            for (int i = 0; i < inputCount; i++)
            {
                TOUCHINPUT ti = inputs[i];

                // Assign a handler to this message.
                EventHandler<WMTouchEventArgs> handler = null;     // Touch event handler
                if ((ti.dwFlags & TOUCHEVENTF_DOWN) != 0)
                {
                    handler = Touchdown;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_UP) != 0)
                {
                    handler = Touchup;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_MOVE) != 0)
                {
                    handler = TouchMove;
                }

                // Convert message parameters into touch event arguments and handle the event.
                if (handler != null)
                {
                    // Convert the raw touchinput message into a touchevent.
                    WMTouchEventArgs te = new WMTouchEventArgs(); // Touch event arguments

                    // TOUCHINFO point coordinates and contact size is in 1/100 of a pixel; convert it to pixels.
                    // Also convert screen to client coordinates.
                    te.ContactY = ti.cyContact/100;
                    te.ContactX = ti.cxContact/100;
                    te.Id = ti.dwID;
                    {
                        Point pt = PointToClient(new Point(ti.x/100, ti.y/100));
                        te.LocationX = pt.X;
                        te.LocationY = pt.Y;
                    }
                    te.Time = ti.dwTime;
                    te.Mask = ti.dwMask;
                    te.Flags = ti.dwFlags;

                    // Invoke the event handler.
                    handler(this, te);

                    // Mark this event as handled.
                    handled = true;
                }
            }

            CloseTouchInputHandle(m.LParam);

            return handled;
        }
    }
```

O código a seguir mostra como uma coleção de traços é exibida.

```CSharp
        public void Draw(Graphics graphics)
        {
            if ((points.Count < 2) || (graphics == null))
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

O código a seguir mostra como os objetos de traço individuais são exibidos com um objeto gráfico.

```CSharp
        public void Draw(Graphics graphics)
        {
            if(points.Count < 2 || graphics == null)
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

## <a name="related-topics"></a>Tópicos relacionados

[exemplo de bloco de rascunho de Windows Touch (C++)](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md), [aplicativo de bloco de rascunho multitoque (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [aplicativo de bloco de rascunho multitoque (WM_TOUCH/c + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [exemplos do Windows Touch](windows-touch-samples.md)

