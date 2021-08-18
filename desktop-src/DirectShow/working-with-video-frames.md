---
description: Trabalhando com quadros de vídeo
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Trabalhando com quadros de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86407f99138e0b38b67468668fc963bd1bcd7b65e875571643bc7727b4d0d339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870926"
---
# <a name="working-with-video-frames"></a>Trabalhando com quadros de vídeo

Vídeo descompactado é uma sequência de bitmaps tocada em sucessão rápida, normalmente a uma taxa de cerca de 30 quadros por segundo. Como a maioria dos vídeos entra em um DirectShow de filtro em um formato compactado, o fluxo de vídeo geralmente passa por um decodificador para descompactação. Muitos decodificadores de saída de dados em um formato YUV e deixam a conversão final em RGB para o hardware de vídeo logo antes da renderização. Se um decodificador usar a Aceleração de Vídeo directX, o hardware de vídeo executará trabalho adicional para decodificar a imagem. Portanto, a descompactação final dos bitmaps pode não ser executada até que os dados atinjam o hardware de vídeo.

No entanto, para executar muitos tipos de análise de vídeo, processamento ou edição, geralmente é necessário trabalhar em bitmaps descompactados em algum tipo de formato RGB ou YUV antes que eles sejam renderizados ou gravados no arquivo. Esse trabalho normalmente é feito em um filtro de transformação com base na classe base [**CTransformFilter,**](ctransformfilter.md) especificamente no **método Transform.** Esse método recebe um ponteiro para um [**objeto IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) que encapsula os dados de vídeo. O **método IMediaSample::GetPointer** retorna um ponteiro para o primeiro byte dos dados brutos. Para quadros descompactados, esses dados consistem em pixels que podem ser acessados ou modificados diretamente pelo filtro. As seções a seguir fornecem informações em segundo plano que ajudarão você a trabalhar efetivamente com os dados DIB dessa maneira.

> [!Note]  
> Você também pode modificar os bits usando funções GDI, GDI+, DirectDraw ou Direct3D, mas essas técnicas estão além do escopo deste artigo.

 

Esta seção contém os seguintes tópicos:

-   [TOP-Down versus Bottom-Up DIBs](top-down-vs--bottom-up-dibs.md)
-   [Trabalhando com RGB de 16 bits](working-with-16-bit-rgb.md)

 

 



