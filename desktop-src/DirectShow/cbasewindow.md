---
description: A classe CBaseWindow é uma classe base para gerenciar o Windows.
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: Classe CBaseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 313f1b222f3b0096d3f5bf92c15e2097afb29848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750054"
---
# <a name="cbasewindow-class"></a>Classe CBaseWindow

A `CBaseWindow` classe é uma classe base para gerenciar o Windows. Os renderizadores de vídeo podem usar essa classe para criar janelas de vídeo. Para usar essa classe, crie uma classe derivada que herda de `CBaseWindow` . Na classe derivada:

-   Implemente o método virtual puro [**CBaseWindow:: GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md), que define os estilos de janela.
-   Substitua o método [**CBaseWindow:: OnReceiveMessage**](cbasewindow-onreceivemessage.md) , que lida com as mensagens de janela.
-   Implemente um destruidor que chama o método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) .

Antes de usar uma instância da classe derivada, chame o método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) .



| Variáveis de membro protegido                                           | Descrição                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**\_HINSTANCE m**](cbasewindow-m-hinstance.md)                      | Identificador para a instância do módulo.                                                 |
| [**\_HWND m**](cbasewindow-m-hwnd.md)                                | Identificador para a janela do objeto.                                                 |
| [**\_HDC m**](cbasewindow-m-hdc.md)                                  | Identificador para o contexto do dispositivo da janela.                                         |
| [**\_Largura m**](cbasewindow-m-width.md)                              | Largura da área do cliente, em pixels.                                           |
| [**altura de m \_**](cbasewindow-m-height.md)                            | Altura da área do cliente, em pixels.                                          |
| [**\_bActivated m**](cbasewindow-m-bactivated.md)                    | Sinalizador que especifica se a janela foi ativada.                     |
| [**\_pClassName m**](cbasewindow-m-pclassname.md)                    | Cadeia de caracteres estática que contém o nome da classe de janela.                      |
| [**\_ClassStyles m**](cbasewindow-m-classstyles.md)                  | Estilos de classe para a janela.                                                   |
| [**\_WindowStyles m**](cbasewindow-m-windowstyles.md)                | Estilos de janela para a janela.                                                  |
| [**\_WindowStylesEx m**](cbasewindow-m-windowstylesex.md)            | Estilos de janela estendidos para a janela.                                         |
| [**\_ShowStageMessage m**](cbasewindow-m-showstagemessage.md)        | Mensagem privada que traz a janela para o primeiro plano.                      |
| [**\_ShowStageTop m**](cbasewindow-m-showstagetop.md)                | Mensagem privada que define o estilo da janela como WS \_ ex mais \_ alta.                 |
| [**\_RealizePalette m**](cbasewindow-m-realizepalette.md)            | Mensagem privada que realiza a paleta.                                     |
| [**\_MemoryDC m**](cbasewindow-m-memorydc.md)                        | Identificador para o contexto do dispositivo de memória.                                           |
| [**\_hPalette m**](cbasewindow-m-hpalette.md)                        | Identificador para a paleta da janela.                                                |
| [**\_bNoRealize m**](cbasewindow-m-bnorealize.md)                    | Sinalizador que especifica se a janela deve reconhecer sua paleta.             |
| [**\_bBackground m**](cbasewindow-m-bbackground.md)                  | Sinalizador que especifica se a paleta deve ser uma paleta de plano de fundo.        |
| [**\_bRealizing m**](cbasewindow-m-brealizing.md)                    | Sinalizador que especifica se uma nova paleta está sendo realizada.                   |
| [**\_WindowLock m**](cbasewindow-m-windowlock.md)                    | Seção crítica para serializar o acesso ao objeto.                           |
| [**\_bDoGetDC m**](cbasewindow-m-bdogetdc.md)                        | Sinalizador que especifica se o contexto do dispositivo deve ser recuperado.                    |
| [**\_bDoPostToDestroy m**](cbasewindow-m-bdoposttodestroy.md)        | Sinalizador que especifica se a janela publica ou envia sua mensagem de destruição. |
| Métodos Protegidos                                                    | Descrição                                                                    |
| [**OnPaletteChange**](cbasewindow-onpalettechange.md)               | Manipula as mensagens de alteração da paleta. VirtuaisLUNs.                                      |
| Métodos públicos                                                       | Descrição                                                                    |
| [**CBaseWindow**](cbasewindow-cbasewindow.md)                       | Método de construtor.                                                            |
| [**DoneWithWindow**](cbasewindow-donewithwindow.md)                 | Destrói a janela. VirtuaisLUNs.                                                  |
| [**PrepareWindow**](cbasewindow-preparewindow.md)                   | Cria a janela. VirtuaisLUNs.                                                   |
| [**InactivateWindow**](cbasewindow-inactivatewindow.md)             | Desativa a janela. VirtuaisLUNs.                                               |
| [**ActivateWindow**](cbasewindow-activatewindow.md)                 | Dimensiona a janela de acordo com os requisitos da classe derivada. VirtuaisLUNs.  |
| [**OnSize**](cbasewindow-onsize.md)                                 | Manipula mensagens de tamanho do WM \_ . VirtuaisLUNs.                                            |
| [**Fechamento**](cbasewindow-onclose.md)                               | Manipula mensagens de fechamento do WM \_ . VirtuaisLUNs.                                           |
| [**GetDefaultRect**](cbasewindow-getdefaultrect.md)                 | Recupera o tamanho padrão da área do cliente. VirtuaisLUNs.                        |
| [**UninitialiseWindow**](cbasewindow-uninitialisewindow.md)         | Libera os recursos da janela. VirtuaisLUNs.                                      |
| [**InitialiseWindow**](cbasewindow-initialisewindow.md)             | Inicializa a janela. VirtuaisLUNs.                                               |
| [**CompleteConnect**](cbasewindow-completeconnect.md)               | Notifica a janela de que o pino de entrada do renderizador foi conectado.          |
| [**Docreatewindow**](cbasewindow-docreatewindow.md)                 | Cria a janela.                                                            |
| [**PerformanceAlignWindow**](cbasewindow-performancealignwindow.md) | Alinha a janela a um limite **DWORD** , para o desempenho máximo.            |
| [**DoShowWindow**](cbasewindow-doshowwindow.md)                     | Define o estado de exibição da janela.                                                  |
| [**PaintWindow**](cbasewindow-paintwindow.md)                       | Faz com que a janela seja repintada.                                             |
| [**DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md)   | Traz a janela para o primeiro plano.                                           |
| [**SetPalette**](cbasewindow-setpalette.md)                         | Instala uma paleta para a janela. VirtuaisLUNs.                                    |
| [**Setrealde**](cbasewindow-setrealize.md)                         | Especifica se a janela percebe paletas.                                |
| [**DoRealisePalette**](cbasewindow-dorealisepalette.md)             | Percebe a paleta atual da janela. VirtuaisLUNs.                                |
| [**PossiblyEatMessage**](cbasewindow-possiblyeatmessage.md)         | Permite que uma classe derivada encaminhe mensagens para outra janela. VirtuaisLUNs.        |
| [**GetWindowWidth**](cbasewindow-getwindowwidth.md)                 | Recupera a largura atual da janela.                                     |
| [**GetWindowHeight**](cbasewindow-getwindowheight.md)               | Recupera a altura atual da janela.                                    |
| [**GetWindowHWND**](cbasewindow-getwindowhwnd.md)                   | Recupera um identificador para a janela.                                              |
| [**GetMemoryHDC**](cbasewindow-getmemoryhdc.md)                     | Recupera um identificador para o contexto do dispositivo de memória.                               |
| [**GetWindowHDC**](cbasewindow-getwindowhdc.md)                     | Recupera um identificador para o contexto do dispositivo da janela.                             |
| [**OnReceiveMessage**](cbasewindow-onreceivemessage.md)             | Manipula mensagens de janela. VirtuaisLUNs.                                              |
| [**UnsetPalette**](cbasewindow-unsetpalette.md)                     | Exclui a paleta atual da janela e restaura a paleta padrão do sistema.  |
| Métodos virtuais puros                                                 | Descrição                                                                    |
| [**GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md)     | Recupera os estilos de classe da janela e os estilos de janela.                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




