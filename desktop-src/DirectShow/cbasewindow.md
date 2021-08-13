---
description: A classe CBaseWindow é uma classe base para gerenciar janelas.
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: Classe CBaseWindow (Winutil.h)
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
ms.openlocfilehash: 60d2a3004343df7846d4bf600690bc6a1e45b46111f91828c7de31219a751308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657188"
---
# <a name="cbasewindow-class"></a>Classe CBaseWindow

A `CBaseWindow` classe é uma classe base para gerenciar janelas. Os renderadores de vídeo podem usar essa classe para criar janelas de vídeo. Para usar essa classe, crie uma classe derivada que herda de `CBaseWindow` . Na classe derivada:

-   Implemente o método virtual [**puro CBaseWindow::GetClassWindowStyles,**](cbasewindow-getclasswindowstyles.md)que define os estilos de janela.
-   Substitua o [**método CBaseWindow::OnReceiveMessage,**](cbasewindow-onreceivemessage.md) que lida com mensagens de janela.
-   Implemente um destruidor que chama o [**método CBaseWindow::D oneWithWindow.**](cbasewindow-donewithwindow.md)

Antes de usar uma instância da classe derivada, chame o [**método CBaseWindow::P repareWindow.**](cbasewindow-preparewindow.md)



| Variáveis de membro protegidas                                           | Descrição                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**m \_ hInstance**](cbasewindow-m-hinstance.md)                      | Lidar com a instância do módulo.                                                 |
| [**m \_ hwnd**](cbasewindow-m-hwnd.md)                                | Identificador para a janela do objeto.                                                 |
| [**m \_ hdc**](cbasewindow-m-hdc.md)                                  | Lidar com o contexto do dispositivo da janela.                                         |
| [**largura \_ m**](cbasewindow-m-width.md)                              | Largura da área do cliente, em pixels.                                           |
| [**m \_ Height**](cbasewindow-m-height.md)                            | Altura da área do cliente, em pixels.                                          |
| [**m \_ bActivated**](cbasewindow-m-bactivated.md)                    | Sinalizador que especifica se a janela foi ativada.                     |
| [**m \_ pClassName**](cbasewindow-m-pclassname.md)                    | Cadeia de caracteres estática que contém o nome da classe de janela.                      |
| [**m \_ ClassStyles**](cbasewindow-m-classstyles.md)                  | Estilos de classe para a janela.                                                   |
| [**m \_ WindowStyles**](cbasewindow-m-windowstyles.md)                | Estilos de janela para a janela.                                                  |
| [**m \_ WindowStylesEx**](cbasewindow-m-windowstylesex.md)            | Estilos de janela estendidos para a janela.                                         |
| [**m \_ ShowStageMessage**](cbasewindow-m-showstagemessage.md)        | Mensagem privada que leva a janela para o primeiro plano.                      |
| [**m \_ ShowStageTop**](cbasewindow-m-showstagetop.md)                | Mensagem privada que define o estilo da janela como WS \_ EX \_ TOPMOST.                 |
| [**m \_ RealizePalette**](cbasewindow-m-realizepalette.md)            | Mensagem privada que realiza a paleta.                                     |
| [**m \_ MemoryDC**](cbasewindow-m-memorydc.md)                        | Lidar com o contexto do dispositivo de memória.                                           |
| [**m \_ hPalette**](cbasewindow-m-hpalette.md)                        | Lidar com a paleta da janela.                                                |
| [**m \_ bNoRealize**](cbasewindow-m-bnorealize.md)                    | Sinalizador que especifica se a janela deve perceber sua paleta.             |
| [**m \_ bBackground**](cbasewindow-m-bbackground.md)                  | Sinalizador que especifica se a paleta deve ser uma paleta de plano de fundo.        |
| [**m \_ bRealizing**](cbasewindow-m-brealizing.md)                    | Sinalizador que especifica se uma nova paleta está sendo realizada.                   |
| [**m \_ WindowLock**](cbasewindow-m-windowlock.md)                    | Seção crítica, para serializar o acesso ao objeto .                           |
| [**m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md)                        | Sinalizador que especifica se o contexto do dispositivo deve ser recuperado.                    |
| [**m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md)        | Sinalizador que especifica se a janela posta ou envia sua mensagem de destruição. |
| Métodos Protegidos                                                    | Descrição                                                                    |
| [**OnPaletteChange**](cbasewindow-onpalettechange.md)               | Lida com mensagens de alteração de paleta. Virtual.                                      |
| Métodos públicos                                                       | Descrição                                                                    |
| [**Cbasewindow**](cbasewindow-cbasewindow.md)                       | Método do construtor.                                                            |
| [**DoneWithWindow**](cbasewindow-donewithwindow.md)                 | Destrói a janela. Virtual.                                                  |
| [**PrepareWindow**](cbasewindow-preparewindow.md)                   | Cria a janela. Virtual.                                                   |
| [**InactivateWindow**](cbasewindow-inactivatewindow.md)             | Inativa a janela. Virtual.                                               |
| [**ActivateWindow**](cbasewindow-activatewindow.md)                 | Tamanhos da janela de acordo com os requisitos da classe derivada. Virtual.  |
| [**Onsize**](cbasewindow-onsize.md)                                 | Lida com mensagens WM \_ SIZE. Virtual.                                            |
| [**Onclose**](cbasewindow-onclose.md)                               | Lida com mensagens WM \_ CLOSE. Virtual.                                           |
| [**GetDefaultRect**](cbasewindow-getdefaultrect.md)                 | Recupera o tamanho padrão da área do cliente. Virtual.                        |
| [**UninitialiseWindow**](cbasewindow-uninitialisewindow.md)         | Libera os recursos da janela. Virtual.                                      |
| [**InitialiseWindow**](cbasewindow-initialisewindow.md)             | Inicializa a janela. Virtual.                                               |
| [**Completeconnect**](cbasewindow-completeconnect.md)               | Notifica a janela de que o pino de entrada do renderista foi conectado.          |
| [**DoCreateWindow**](cbasewindow-docreatewindow.md)                 | Cria a janela.                                                            |
| [**PerformanceAlignWindow**](cbasewindow-performancealignwindow.md) | Alinha a janela a um **limite DWORD,** para desempenho máximo.            |
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
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




