---
description: A classe CBaseControlWindow implementa a interface IVideoWindow e controla o acesso externo ao filtro associado.
ms.assetid: 3657ba24-ffaa-491f-9eb3-f9913d5d421a
title: Classe CBaseControlWindow
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow
api_type:
- COM
api_location: ''
ms.openlocfilehash: 500706531d7e7a934681dabe3bcd00b7de0d80e42b8bbf27a5456a8fd4415f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017225"
---
# <a name="cbasecontrolwindow-class"></a>Classe CBaseControlWindow

![Hierarquia de classes cbasecontrolwindow](images/wctrl01.png)

A **classe CBaseControlWindow** implementa a interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e controla o acesso externo ao filtro associado. Você deve sincronizar o **objeto CBaseControlWindow** com o filtro passando um ponteiro para um objeto de sincronização de seção crítico. A **classe CBaseControlWindow** fornece vários métodos que retornam configurações de propriedade sem lidar com esta seção crítica. Por exemplo, chamar [**CBaseControlWindow::get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md) para recuperar o valor do membro de dados **m \_ bAutoShow** bloqueia a seção crítica. No entanto, o filtro já pode ter uma seção crítica interna bloqueada, o que pode violar a hierarquia de bloqueio do filtro. Em vez disso, chamar a função membro [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) retorna o valor necessário sem afetar a seção crítica.

Todos os métodos [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) implementados pelo **CBaseControlWindow** exigem que o filtro seja conectado corretamente com seu filtro upstream. Por esse motivo, os objetos de classe exigem um pin de sincronização, que você definiu chamando o [**método CBaseControlWindow::SetControlWindowPin.**](cbasecontrolwindow-setcontrolwindowpin.md) Sempre que você chama **um método IVideoWindow,** o **objeto CBaseControlWindow** verifica se o pino ainda está conectado.



| Membros de Dados Protegidos                                                     | Descrição                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| m \_ bAutoShow                                                               | Resultado quando o estado muda.                                                                                                              |
| m \_ bCursorHidden                                                           | Determinação de se o cursor é exibido ou oculto.                                                                                 |
| m \_ BorderColorr                                                            | Cor da borda da janela atual.                                                                                                         |
| m \_ hwndDrain                                                               | O alça de janela para o qual as mensagens recebidas são postadas.                                                                                        |
| m \_ hwndOwner                                                               | Janela De propriedade.                                                                                                                              |
| m \_ pFilter                                                                 | Ponteiro para o filtro de mídia de propriedade.                                                                                                         |
| m \_ pInterfaceLock                                                          | Seção crítica definida externamente.                                                                                                        |
| m \_ pPin                                                                    | Controle dos tipos de mídia para conexão.                                                                                                  |
| Funções de membro                                                           | Descrição                                                                                                                                 |
| [**Cbasecontrolwindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | Constrói **um objeto CBaseControlWindow.**                                                                                                 |
| [**DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md)            | Recupera os estilos de janela típicos ou estendidos.                                                                                     |
| [**DoSetWindowStyle**](cbasecontrolwindow-dosetwindowstyle.md)            | Define os estilos de janela típicos ou estendidos.                                                                                                 |
| [**GetBorderColorr**](cbasecontrolwindow-getbordercolour.md)              | Recupera a cor da borda atual. Essa é uma função de membro auxiliar.                                                                       |
| [**GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md)                | Recupera a janela de propriedade. Essa é uma função de membro auxiliar.                                                                              |
| [**IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md)          | Recupera informações sobre se a janela de vídeo aparece automaticamente quando o filtro de renderização pausa ou é executado.                        |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera o estado atual do **membro de dados m \_ bCursorHidden** sem bloquear a seção crítica. Essa é uma função de membro auxiliar. |
| [**PossivelmenteEatMessage**](cbasecontrolwindow-possiblyeatmessage.md)        | Distribui mensagens para a janela pai.                                                                                                  |
| [**SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md)      | Notifica o objeto do pino ao qual ele se aplica.                                                                                         |
| Métodos IVideoWindow                                                       | Descrição                                                                                                                                 |
| [**get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md)                   | Recupera a configuração atual do sinalizador AutoShow.                                                                                                |
| [**obter \_ BackgroundPalette**](cbasecontrolwindow-get-backgroundpalette.md) | Recupera a paleta realizada no sinalizador de plano de fundo.                                                                                      |
| [**obter \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md)             | Recupera a cor da borda atual.                                                                                                         |
| [**obter \_ Legenda**](cbasecontrolwindow-get-caption.md)                     | Recupera a legenda da janela atual.                                                                                                       |
| [**get \_ FullScreenMode**](cbasecontrolwindow-get-fullscreenmode.md)      | Recupera o modo de tela inteira atual.                                                                                                     |
| [**obter \_ altura**](cbasecontrolwindow-get-height.md)                       | Recupera a altura atual da janela.                                                                                                        |
| [**get \_ Left**](cbasecontrolwindow-get-left.md)                           | Recupera a coordenada da janela esquerda atual.                                                                                               |
| [**GetMaxIdealImageSize**](cbasecontrolwindow-getmaxidealimagesize.md)    | Recupera o tamanho máximo da imagem ideal.                                                                                              |
| [**get \_ MessageDrain**](cbasecontrolwindow-get-messagedrain.md)           | Recupera o dreno de mensagens atual.                                                                                                        |
| [**GetMinIdealImageSize**](cbasecontrolwindow-getminidealimagesize.md)    | Recupera o tamanho mínimo da imagem ideal.                                                                                              |
| [**obter \_ Proprietário**](cbasecontrolwindow-get-owner.md)                         | Recupera o alça da janela pai.                                                                                                         |
| [**GetRestorePosition**](cbasecontrolwindow-getrestoreposition.md)        | Recupera a posição na qual a janela será restaurada quando maximizada ou minimizada.                                                    |
| [**get \_ Top**](cbasecontrolwindow-get-top.md)                             | Recupera a coordenada y para a parte superior da janela.                                                                                       |
| [**ficar \_ visível**](cbasecontrolwindow-get-visible.md)                     | Recupera a configuração de visibilidade atual da janela.                                                                                     |
| [**obter \_ Largura**](cbasecontrolwindow-get-width.md)                         | Recupera a largura da janela.                                                                                                          |
| [**GetWindowPosition**](cbasecontrolwindow-getwindowposition.md)          | Recupera as coordenadas da janela atual.                                                                                                   |
| [**get \_ WindowState**](cbasecontrolwindow-get-windowstate.md)             | Recupera o estado atual da janela.                                                                                                  |
| [**get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md)             | Recupera os estilos de janela padrão.                                                                                                       |
| [**obter \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md)         | Recupera os estilos de janela estendidos.                                                                                                       |
| [**HideCursor**](cbasecontrolwindow-hidecursor.md)                        | Oculta ou exibe o cursor.                                                                                                               |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera o estado atual do **membro de dados m \_ bCursorHidden.**                                                                        |
| [**NotifyOwnerMessage**](cbasecontrolwindow-notifyownermessage.md)        | Passa mensagens que são enviadas para janelas de propriedade.                                                                                         |
| [**colocar \_ Automostrar**](cbasecontrolwindow-put-autoshow.md)                   | Define a propriedade AutoShow.                                                                                                                 |
| [**colocar \_ BackgroundPalette**](cbasecontrolwindow-put-backgroundpalette.md) | Define um sinalizador para obter a paleta em segundo plano.                                                                                       |
| [**colocar \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md)             | Define a cor da borda atual.                                                                                                              |
| [**colocar \_ legenda**](cbasecontrolwindow-put-caption.md)                     | Define a legenda da janela atual.                                                                                                            |
| [**colocar \_ tela inteira**](cbasecontrolwindow-put-fullscreenmode.md)      | Define o modo de tela inteira.                                                                                                                  |
| [**colocar \_ altura**](cbasecontrolwindow-put-height.md)                       | Define a altura da janela atual.                                                                                                             |
| [**colocar \_ à esquerda**](cbasecontrolwindow-put-left.md)                           | Define a coordenada esquerda para a janela.                                                                                                    |
| [**colocar \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)           | Define a janela de drenagem de mensagem.                                                                                                              |
| [**colocar \_ proprietário**](cbasecontrolwindow-put-owner.md)                         | Define o identificador da janela pai do Microsoft Win32.                                                                                              |
| [**colocar na \_ parte superior**](cbasecontrolwindow-put-top.md)                             | Define a posição da parte superior da janela.                                                                                                |
| [**colocar \_ visível**](cbasecontrolwindow-put-visible.md)                     | Oculta ou mostra a janela.                                                                                                                  |
| [**colocar \_ largura**](cbasecontrolwindow-put-width.md)                         | Define a largura da janela.                                                                                                               |
| [**colocar \_ janelastate**](cbasecontrolwindow-put-windowstate.md)             | Define o estado da janela.                                                                                                               |
| [**colocar \_ janelastyle**](cbasecontrolwindow-put-windowstyle.md)             | Define os estilos de janela padrão.                                                                                                            |
| [**colocar \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md)         | Define os estilos de janela estendida.                                                                                                            |
| [**SetWindowForeground**](cbasecontrolwindow-setwindowforeground.md)      | Define a janela em primeiro plano.                                                                                                          |
| [**SetWindowPosition**](cbasecontrolwindow-setwindowposition.md)          | Define a posição da janela.                                                                                                                   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Classes base](directshow-base-classes.md)
</dt> </dl>

 

 



