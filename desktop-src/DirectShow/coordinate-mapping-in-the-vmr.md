---
description: Mapeamento de coordenadas no VMR
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: Mapeamento de coordenadas no VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c18b38249471e6e68e36f1b9051f51e920f62b31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825626"
---
# <a name="coordinate-mapping-in-the-vmr"></a>Mapeamento de coordenadas no VMR

Esta seção descreve as cinco transformações que são aplicadas a uma imagem de origem antes de serem mapeadas pelo VMR na imagem de saída final.

1.  A transformação *T (src)* mapeia o retângulo de origem para o retângulo de destino. Eles são especificados pelos membros **rcSource** e **RcTarget** da estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) no tipo de mídia. Esse mapeamento processa a imagem de origem conforme ela passa para o VMR.
2.  A transformação *T (Flag)* executa quaisquer manipulações de imagem especificadas por sinalizadores no exemplo de mídia. Elas incluíram transformações, como a tradução vertical e a escala para acomodar os sinalizadores de entrelaçamento de Bob. A transformação entrelaçar dobra a altura da imagem e possivelmente traduz a imagem pela metade de uma linha de vídeo se ela estiver no campo ímpar.
3.  A transformação *T (ar)* ajusta a imagem para pixels quadrados, com base na taxa de proporção da imagem. Para tipos de mídia **VIDEOINFOHEADER** , a taxa de proporção é determinada pelo tamanho da imagem. Para tipos **VIDEOINFOHEADER2** , a taxa de proporção é determinada pelos campos **dwPictAspectRatioX** e **dwPictAspectRatioY** , a menos que o \_ painel AMCONTROL \_ para \_ 16x9 ou AMCONTROL \_ pad \_ para \_ 4x3 flags seja definido. Essa transformação pressupõe que a configuração de exibição do monitor corresponda à taxa de proporção física do monitor. Por exemplo, se o usuário tiver um monitor com taxa de proporção de 4 x 3, mas definir a exibição como 1280 x 768 pixels (5 x 3), a imagem não terá a taxa de proporção correta.
4.  As transformações *T (Mix)* de transformação posicionam a imagem na imagem de destino, usando os retângulos normalizados especificados nos métodos [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) . Os retângulos normalizados permitem que o aplicativo organize como os fluxos de origem são posicionados e dimensionados em relação uns com os outros. O VMR computa a imagem de destino computando as dimensões máximas de todas as imagens de origem e centralizando cada uma dentro de um retângulo delimitador geral. Os cantos do retângulo delimitador são atribuídos ao intervalo (0, 0) a (1, 1). O retângulo delimitador é corrigido antes que o grafo seja executado e permaneça constante, mesmo se os fluxos forem adicionados ou excluídos. Os retângulos de destino de cada fluxo podem ficar fora do intervalo (0, 0) a (1, 1) e ainda ser válidos.
5.  Por fim, uma parte da imagem mista pode ser transformada pelo *T de mapeamento (DST)*, especificado pelos retângulos de origem e de destino na interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) no VMR. Se a Allocator-Presenter for substituída e a interface **IBasicVideo** não for usada, o aplicativo deverá implementar a interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) e mapear as coordenadas de volta para um espaço linear 2D. As coordenadas do mouse retornadas para o navegador de DVD também devem estar nesse espaço. Por exemplo, se um aplicativo renderizar o vídeo em um cubo de rotação, ele relatará a exibição inteira para o controle sem janela e retornará as coordenadas do mouse relativas à exibição.

A transformação de imagem geral dos dados de origem para o renderizador final é:

T = T (src) \* t (Flag) t (ar) t (Mix) \* t (DST)\*

onde \* indica que a imagem pode ser recortada para a imagem de destino nesse estágio. Observe que todas são transformações afim, de modo que o VMR pode combiná-las em uma única transformação.

O inverso da transformação é:

![transformação inversa](images/vmrmapping-t-1.png)

O fator T (src) T (Flag) T (ar) é relativo à resolução de origem. No fator T (Mix), o retângulo de origem normalizado é relativo à imagem com correção de aspecto. O retângulo de destino normalizado é relativo à resolução de saída. O diagrama a seguir mostra essas relações.

![etapas de transformação de imagem](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o VMR para desenvolvedores de filtro do DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



