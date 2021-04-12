---
description: A classe CBaseControlVideo implementa a interface IBasicVideo e controla as propriedades de vídeo de uma janela de vídeo genérica. Geralmente, um objeto CBaseControlVideo é um processador de vídeo que desenha o vídeo em uma janela na tela.
ms.assetid: 16fc1b0a-e5b5-4f33-ac2b-5acff61bab81
title: Classe CBaseControlVideo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo
api_type:
- COM
api_location: ''
ms.openlocfilehash: e2e5962eb9d175bfbbeadd149a547f0d36fbf49f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456747"
---
# <a name="cbasecontrolvideo-class"></a>Classe CBaseControlVideo

![hierarquia de classe CBaseControlVideo](images/wctrl02.png)

A classe **CBaseControlVideo** implementa a interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e controla as propriedades de vídeo de uma janela de vídeo genérica. Geralmente, um objeto **CBaseControlVideo** é um processador de vídeo que desenha o vídeo em uma janela na tela.

Muitas funções de membro **CBaseControlVideo** exigem apenas que o processador de vídeo esteja conectado a um grafo de filtro. Se não estiver conectado, as funções de membro retornarão **VFW \_ E \_ não serão \_ conectadas**. As propriedades definidas em um processador de vídeo persistem entre conexões e desconexões sucessivas. Todos os aplicativos devem garantir que redefinam as propriedades do renderizador antes de iniciar uma apresentação.

Ao trabalhar com vídeo, o aplicativo pode selecionar uma parte do vídeo a ser usada. Essa parte é o retângulo de origem que o objeto **CBaseControlVideo** controla. **CBaseControlVideo** permite que seu aplicativo defina e recupere o retângulo de origem. Todos os retângulos que **CBaseControlVideo** usa usam valores de largura e altura em vez de valores direito e inferior. Quando nenhum retângulo de origem foi definido, as propriedades do retângulo de origem retornam o tamanho de vídeo nativo completo.



| Membros de Dados Protegidos                                                                   | Descrição                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| \_pFilter m                                                                               | Ponteiro para um filtro de mídia proprietário.                                                              |
| \_pInterfaceLock m                                                                        | Seção crítica definida externamente.                                                            |
| \_pPin m                                                                                  | Controle dos tipos de mídia para conexão.                                                      |
| Funções de membro                                                                         | Descrição                                                                                     |
| [**CBaseControlVideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | Constrói um objeto **CBaseControlVideo** .                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | Cria uma cópia de memória de uma imagem de vídeo.                                                         |
| [**Getimageize**](cbasecontrolvideo-getimagesize.md)                                   | Recupera informações de tamanho da imagem de vídeo.                                                         |
| [**SetControlVideoPin**](cbasecontrolvideo-setcontrolvideopin.md)                       | Define o PIN com o qual esse objeto deve ser sincronizado.                                         |
| Funções de membro substituíveis                                                             | Descrição                                                                                     |
| [**CheckSourceRect**](cbasecontrolvideo-checksourcerect.md)                             | Determina se um retângulo de origem é válido.                                                      |
| [**CheckTargetRect**](cbasecontrolvideo-checktargetrect.md)                             | Determina se um retângulo de destino é válido.                                                      |
| [**GetSourceRect**](cbasecontrolvideo-getsourcerect.md)                                 | Recupera o retângulo de vídeo de origem atual (virtual puro).                                    |
| [**GetStaticImage**](cbasecontrolvideo-getstaticimage.md)                               | Retorna a imagem atual em um buffer de memória (virtual puro).                                    |
| [**GetTargetRect**](cbasecontrolvideo-gettargetrect.md)                                 | Recupera o retângulo de vídeo de destino atual (virtual puro).                                    |
| [**GetVideoFormat**](cbasecontrolvideo-getvideoformat.md)                               | Recupera a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contém o formato de vídeo. |
| [**IsDefaultSourceRect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | Determina se o renderizador está usando o retângulo de origem padrão (virtual puro).                |
| [**IsDefaultTargetRect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | Determina se o renderizador está usando o retângulo de destino padrão (virtual puro).                |
| [**OnUpdateRectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | Chamado quando o retângulo de origem ou de destino é alterado.                                             |
| [**OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)                         | Passa \_ \_ o tamanho do vídeo do EC \_ alterado para o aplicativo.                                             |
| [**SetDefaultSourceRect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | Define o retângulo de vídeo de origem padrão (virtual puro).                                         |
| [**SetDefaultTargetRect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | Define o retângulo de vídeo de destino padrão (virtual puro).                                         |
| [**SetSourceRect**](cbasecontrolvideo-setsourcerect.md)                                 | Define o retângulo de vídeo de origem atual (virtual puro).                                         |
| [**SetTargetRect**](cbasecontrolvideo-settargetrect.md)                                 | Define o retângulo de destino atual (virtual puro).                                               |
| Métodos IBasicVideo                                                                      | Descrição                                                                                     |
| [**obter \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)                    | Recupera um tempo médio aproximado por quadro.                                                |
| [**obter \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)                          | Recupera uma taxa aproximada de erros de bits.                                                        |
| [**obter \_ taxa de bits**](cbasecontrolvideo-get-bitrate.md)                                    | Recupera uma taxa de bits aproximada para o vídeo.                                                |
| [**GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)                             | Recupera uma renderização de memória da imagem atual.                                              |
| [**obter \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)                | Recupera a altura do retângulo de destino atual.                                           |
| [**obter \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)                    | Recupera a coordenada esquerda do retângulo de destino atual.                                  |
| [**GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)               | Recupera a posição de destino atual.                                                     |
| [**obter \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)                      | Recupera a coordenada superior do retângulo de destino atual.                                   |
| [**obter \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)                  | Recupera a largura do retângulo de destino atual.                                            |
| [**obter \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)                          | Recupera a altura do retângulo de origem atual.                                                |
| [**obter \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)                              | Recupera a coordenada esquerda do retângulo de origem atual.                                       |
| [**GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)                         | Recupera a posição de origem atual.                                                          |
| [**obter \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)                                | Recupera a coordenada superior do retângulo de origem atual.                                        |
| [**obter \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)                            | Recupera a largura do retângulo de origem atual.                                                 |
| [**obter \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)                            | Recupera a altura do vídeo nativo.                                                              |
| [**GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)               | Recupera um intervalo de entradas de paleta para o vídeo.                                             |
| [](cbasecontrolvideo-getvideosize.md)                                   | Recupera a largura e a altura do vídeo nativo.                                             |
| [**obter \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)                              | Recupera a largura do vídeo nativo.                                                               |
| [**IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | Determina se o renderizador está usando a janela de destino padrão.                             |
| [**IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md)                   | Determina se o renderizador está usando a janela de origem padrão.                                  |
| [**colocar \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)                | Define a altura do retângulo de destino.                                                        |
| [**colocar \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)                    | Define a coordenada esquerda do retângulo de destino.                                               |
| [**colocar \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)                      | Define a coordenada superior do retângulo de destino.                                                |
| [**colocar \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)                  | Define a largura do retângulo de destino.                                                         |
| [**colocar \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)                          | Define a altura do retângulo de origem.                                                             |
| [**colocar \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)                              | Define a coordenada esquerda do retângulo de origem.                                                    |
| [**colocar \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)                                | Define a coordenada superior do retângulo de origem.                                                     |
| [**colocar \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)                            | Define a largura do retângulo de origem.                                                              |
| [**SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) | Define a posição de destino padrão novamente.                                                    |
| [**SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)           | Define a posição de origem padrão novamente.                                                         |
| [**SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)               | Define a posição do retângulo de destino.                                                        |
| [**SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)                         | Define a posição do retângulo de origem.                                                             |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes base do DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 



