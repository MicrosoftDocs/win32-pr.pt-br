---
description: A classe CBaseControlWindow implementa a interface IVideoWindow e controla o acesso externo ao seu filtro associado.
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
ms.openlocfilehash: c4b53cc5ce1b209cc7de9d68648b68096e5c4911
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163824"
---
# <a name="cbasecontrolwindow-class"></a>Classe CBaseControlWindow

![hierarquia de classe CBaseControlWindow](images/wctrl01.png)

A classe **CBaseControlWindow** implementa a interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e controla o acesso externo ao seu filtro associado. Você deve sincronizar o objeto **CBaseControlWindow** com o filtro passando um ponteiro para um objeto de sincronização de seção crítica. A classe **CBaseControlWindow** fornece vários métodos que retornam configurações de propriedade sem lidar com essa seção crítica. Por exemplo, chamar [**CBaseControlWindow:: get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md) para recuperar o valor do membro de dados **m \_ bAutoShow** bloqueia a seção crítica. O filtro pode já ter uma seção crítica interna bloqueada, no entanto, que poderia violar a hierarquia de bloqueio do filtro. Em vez disso, chamar a função de membro [**CBaseControlWindow:: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) retorna o valor necessário sem afetar a seção crítica.

Todos os métodos [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) implementados pelo **CBaseControlWindow** exigem que o filtro esteja conectado corretamente com seu filtro upstream. Por esse motivo, os objetos de classe exigem um PIN de sincronização, que você define chamando o método [**CBaseControlWindow:: SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md) . Sempre que você chamar um método **IVideoWindow** , o objeto **CBaseControlWindow** verificará se o PIN ainda está conectado.



| Membros de Dados Protegidos                                                     | Descrição                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| \_bAutoShow m                                                               | Resultado quando o estado é alterado.                                                                                                              |
| \_bCursorHidden m                                                           | Determinação de se o cursor é exibido ou oculto.                                                                                 |
| \_BorderColour m                                                            | Cor da borda da janela atual.                                                                                                         |
| \_hwndDrain m                                                               | Identificador de janela para o qual as mensagens recebidas são lançadas.                                                                                        |
| \_hwndOwner m                                                               | Janela proprietária.                                                                                                                              |
| \_pFilter m                                                                 | Ponteiro para o filtro de mídia proprietário.                                                                                                         |
| \_pInterfaceLock m                                                          | Seção crítica definida externamente.                                                                                                        |
| \_pPin m                                                                    | Controle dos tipos de mídia para conexão.                                                                                                  |
| Funções de membro                                                           | Descrição                                                                                                                                 |
| [**CBaseControlWindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | Constrói um objeto **CBaseControlWindow** .                                                                                                 |
| [**DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md)            | Recupera os estilos de janela típicos ou estendidos.                                                                                     |
| [**DoSetWindowStyle**](cbasecontrolwindow-dosetwindowstyle.md)            | Define os estilos de janela típicos ou estendidos.                                                                                                 |
| [**GetBorderColour**](cbasecontrolwindow-getbordercolour.md)              | Recupera a cor da borda atual. Essa é uma função de membro auxiliar.                                                                       |
| [**GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md)                | Recupera a janela proprietária. Essa é uma função de membro auxiliar.                                                                              |
| [**IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md)          | Recupera informações sobre se a janela de vídeo é exibida automaticamente quando o filtro de renderização é pausado ou executado.                        |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera o estado atual do membro de dados **m \_ bCursorHidden** sem bloquear a seção crítica. Essa é uma função de membro auxiliar. |
| [**PossiblyEatMessage**](cbasecontrolwindow-possiblyeatmessage.md)        | Distribui mensagens para a janela pai.                                                                                                  |
| [**SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md)      | Notifica o objeto do Pin ao qual se aplica.                                                                                         |
| Métodos IVideoWindow                                                       | Descrição                                                                                                                                 |
| [**obter \_ Automostrar**](cbasecontrolwindow-get-autoshow.md)                   | Recupera a configuração atual do sinalizador AutoShow.                                                                                                |
| [**obter \_ BackgroundPalette**](cbasecontrolwindow-get-backgroundpalette.md) | Recupera a paleta realizada no sinalizador de segundo plano.                                                                                      |
| [**obter \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md)             | Recupera a cor da borda atual.                                                                                                         |
| [**obter \_ legenda**](cbasecontrolwindow-get-caption.md)                     | Recupera a legenda da janela atual.                                                                                                       |
| [**obter \_ tela inteira**](cbasecontrolwindow-get-fullscreenmode.md)      | Recupera o modo de tela inteira atual.                                                                                                     |
| [**obter \_ altura**](cbasecontrolwindow-get-height.md)                       | Recupera a altura da janela atual.                                                                                                        |
| [**obter \_ à esquerda**](cbasecontrolwindow-get-left.md)                           | Recupera a coordenada da janela esquerda atual.                                                                                               |
| [**GetMaxIdealImageSize**](cbasecontrolwindow-getmaxidealimagesize.md)    | Recupera o tamanho máximo da imagem ideal.                                                                                              |
| [**obter \_ MessageDrain**](cbasecontrolwindow-get-messagedrain.md)           | Recupera a mensagem atual drenagem.                                                                                                        |
| [**GetMinIdealImageSize**](cbasecontrolwindow-getminidealimagesize.md)    | Recupera o tamanho mínimo da imagem ideal.                                                                                              |
| [**obter \_ proprietário**](cbasecontrolwindow-get-owner.md)                         | Recupera o identificador da janela pai.                                                                                                         |
| [**GetRestorePosition**](cbasecontrolwindow-getrestoreposition.md)        | Recupera a posição na qual a janela será restaurada quando maximizada ou minimizada.                                                    |
| [**obter \_ parte superior**](cbasecontrolwindow-get-top.md)                             | Recupera a coordenada y para a parte superior da janela.                                                                                       |
| [**Fique \_ visível**](cbasecontrolwindow-get-visible.md)                     | Recupera a configuração de visibilidade atual da janela.                                                                                     |
| [**obter \_ largura**](cbasecontrolwindow-get-width.md)                         | Recupera a largura da janela.                                                                                                          |
| [**GetWindowPosition**](cbasecontrolwindow-getwindowposition.md)          | Recupera as coordenadas da janela atual.                                                                                                   |
| [**obter \_ janelastate**](cbasecontrolwindow-get-windowstate.md)             | Recupera o estado atual da janela.                                                                                                  |
| [**obter \_ janelastyle**](cbasecontrolwindow-get-windowstyle.md)             | Recupera os estilos de janela padrão.                                                                                                       |
| [**obter \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md)         | Recupera os estilos de janela estendida.                                                                                                       |
| [**HideCursor**](cbasecontrolwindow-hidecursor.md)                        | Oculta ou exibe o cursor.                                                                                                               |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera o estado atual do membro de dados **m \_ bCursorHidden** .                                                                        |
| [**NotifyOwnerMessage**](cbasecontrolwindow-notifyownermessage.md)        | Passa mensagens que são enviadas para as janelas proprietárias.                                                                                         |
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

[Classes base do DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 



