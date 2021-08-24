---
description: A classe CBaseControlVideo implementa a interface IBasicVideo e controla as propriedades de vídeo de uma janela de vídeo genérica. Em geral, um objeto CBaseControlVideo é um renderador de vídeo que desenha vídeo em uma janela na exibição.
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
ms.openlocfilehash: 3d8e6f7c881cc62f9124a58cb168bb3b2123d5f8e3c99b1d86b6aed0f87e2aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697936"
---
# <a name="cbasecontrolvideo-class"></a>Classe CBaseControlVideo

![Hierarquia de classes cbasecontrolvideo](images/wctrl02.png)

A **classe CBaseControlVideo** implementa a interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e controla as propriedades de vídeo de uma janela de vídeo genérica. Em geral, **um objeto CBaseControlVideo** é um renderador de vídeo que desenha vídeo em uma janela na exibição.

Muitas **funções de membro CBaseControlVideo** exigem apenas que o renderador de vídeo esteja conectado a um grafo de filtro. Se não estiver conectado, as funções membro retornarão **VFW \_ E \_ NOT \_ CONNECTED.** As propriedades definidas em um renderador de vídeo persistem entre conexões sucessivas e desconexões. Todos os aplicativos devem garantir que eles redefinim as propriedades do renderdor antes de iniciar uma apresentação.

Ao trabalhar com vídeo, o aplicativo pode selecionar uma parte do vídeo a ser usada. Essa parte é o retângulo de origem que o **objeto CBaseControlVideo** controla. **O CBaseControlVideo** permite que seu aplicativo de definir e recuperar o retângulo de origem. Todos os retângulos que **CBaseControlVideo usa** empregam valores de largura e altura em vez de valores de direita e inferior. Quando nenhum retângulo de origem foi definido, as propriedades do retângulo de origem retornam o tamanho completo e nativo do vídeo.



| Membros de Dados Protegidos                                                                   | Descrição                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| m \_ pFilter                                                                               | Ponteiro para um filtro de mídia próprio.                                                              |
| m \_ pInterfaceLock                                                                        | Seção crítica definida externamente.                                                            |
| m \_ pPin                                                                                  | Controle dos tipos de mídia para conexão.                                                      |
| Funções de membro                                                                         | Descrição                                                                                     |
| [**Cbasecontrolvideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | Constrói **um objeto CBaseControlVideo.**                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | Cria uma cópia de memória de uma imagem de vídeo.                                                         |
| [**Getimagesize**](cbasecontrolvideo-getimagesize.md)                                   | Recupera informações de tamanho da imagem de vídeo.                                                         |
| [**SetControlVideoPin**](cbasecontrolvideo-setcontrolvideopin.md)                       | Define o pino com o qual esse objeto deve ser sincronizado.                                         |
| Funções de membro que podem ser substituídos                                                             | Descrição                                                                                     |
| [**CheckSourceRect**](cbasecontrolvideo-checksourcerect.md)                             | Determina se um retângulo de origem é válido.                                                      |
| [**CheckTargetRect**](cbasecontrolvideo-checktargetrect.md)                             | Determina se um retângulo de destino é válido.                                                      |
| [**GetSourceRect**](cbasecontrolvideo-getsourcerect.md)                                 | Recupera o retângulo de vídeo de origem atual (virtual puro).                                    |
| [**GetStaticImage**](cbasecontrolvideo-getstaticimage.md)                               | Retorna a imagem atual em um buffer de memória (virtual puro).                                    |
| [**GetTargetRect**](cbasecontrolvideo-gettargetrect.md)                                 | Recupera o retângulo de vídeo de destino atual (virtual puro).                                    |
| [**GetVideoFormat**](cbasecontrolvideo-getvideoformat.md)                               | Recupera a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contém o formato de vídeo. |
| [**IsDefaultSourceRect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | Determina se o renderador está usando o retângulo de origem padrão (virtual puro).                |
| [**IsDefaultTargetRect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | Determina se o renderador está usando o retângulo de destino padrão (virtual puro).                |
| [**OnUpdateRectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | Chamado quando o retângulo de origem ou de destino muda.                                             |
| [**OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)                         | Passa o TAMANHO DO VÍDEO DA EC \_ \_ ALTERADO para o \_ aplicativo.                                             |
| [**SetDefaultSourceRect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | Define o retângulo de vídeo de origem padrão (virtual puro).                                         |
| [**SetDefaultTargetRect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | Define o retângulo de vídeo de destino padrão (virtual puro).                                         |
| [**SetSourceRect**](cbasecontrolvideo-setsourcerect.md)                                 | Define o retângulo de vídeo de origem atual (virtual puro).                                         |
| [**SetTargetRect**](cbasecontrolvideo-settargetrect.md)                                 | Define o retângulo de destino atual (virtual puro).                                               |
| Métodos IBasicVideo                                                                      | Descrição                                                                                     |
| [**obter \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)                    | Recupera um tempo médio aproximado por quadro.                                                |
| [**get \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)                          | Recupera uma taxa de erro de bit aproximada.                                                        |
| [**get \_ BitRate**](cbasecontrolvideo-get-bitrate.md)                                    | Recupera uma taxa de bits aproximada para o vídeo.                                                |
| [**GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)                             | Recupera uma renderização de memória da imagem atual.                                              |
| [**get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)                | Recupera a altura do retângulo de destino atual.                                           |
| [**get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)                    | Recupera a coordenada esquerda do retângulo de destino atual.                                  |
| [**GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)               | Recupera a posição de destino atual.                                                     |
| [**get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)                      | Recupera a coordenada superior do retângulo de destino atual.                                   |
| [**get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)                  | Recupera a largura do retângulo de destino atual.                                            |
| [**obter \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)                          | Recupera a altura do retângulo de origem atual.                                                |
| [**obter \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)                              | Recupera a coordenada esquerda do retângulo de origem atual.                                       |
| [**GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)                         | Recupera a posição de origem atual.                                                          |
| [**get \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)                                | Recupera a coordenada superior do retângulo de origem atual.                                        |
| [**obter \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)                            | Recupera a largura do retângulo de origem atual.                                                 |
| [**obter \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)                            | Recupera a altura nativa do vídeo.                                                              |
| [**GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)               | Recupera um intervalo de entradas de paleta para o vídeo.                                             |
| [**GetVideoSize**](cbasecontrolvideo-getvideosize.md)                                   | Recupera a largura e a altura do vídeo nativo.                                             |
| [**obter \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)                              | Recupera a largura do vídeo nativo.                                                               |
| [**IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | Determina se o renderador está usando a janela de destino padrão.                             |
| [**IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md)                   | Determina se o renderador está usando a janela de origem padrão.                                  |
| [**put \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)                | Define a altura do retângulo de destino.                                                        |
| [**put \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)                    | Define a coordenada esquerda do retângulo de destino.                                               |
| [**put \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)                      | Define a coordenada superior do retângulo de destino.                                                |
| [**put \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)                  | Define a largura do retângulo de destino.                                                         |
| [**put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)                          | Define a altura do retângulo de origem.                                                             |
| [**put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)                              | Define a coordenada esquerda do retângulo de origem.                                                    |
| [**put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)                                | Define a coordenada superior do retângulo de origem.                                                     |
| [**put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)                            | Define a largura do retângulo de origem.                                                              |
| [**SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) | Define a posição de destino padrão novamente.                                                    |
| [**SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)           | Define a posição de origem padrão novamente.                                                         |
| [**SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)               | Define a posição do retângulo de destino.                                                        |
| [**SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)                         | Define a posição do retângulo de origem.                                                             |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Base Classes](directshow-base-classes.md)
</dt> </dl>

 

 



