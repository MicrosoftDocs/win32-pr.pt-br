---
description: Trabalhando com quadros de vídeo
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Trabalhando com quadros de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812968"
---
# <a name="working-with-video-frames"></a>Trabalhando com quadros de vídeo

O vídeo descompactado é uma sequência de bitmaps reproduzidos em uma rápida sucessão, normalmente a uma taxa de aproximadamente 30 quadros por segundo. Como a maioria do vídeo entra em um grafo de filtro do DirectShow em um formato compactado, o fluxo de vídeo geralmente passa por um decodificador para descompactação. Muitos decodificadores geram dados em um formato YUV e deixam a conversão final em RGB para o hardware de vídeo logo antes da renderização. Se um decodificador usar a aceleração de vídeo do DirectX, o hardware de vídeo executará um trabalho adicional para decodificar a imagem. Assim, a descompactação final dos bitmaps pode não ser executada até que os dados cheguem ao hardware de vídeo.

Mas, para executar muitos tipos de análise de vídeo, processamento ou edição, geralmente é necessário trabalhar em bitmaps não compactados em algum tipo de formato RGB ou YUV antes de serem renderizados ou gravados no arquivo. Normalmente, esse trabalho é feito dentro de um filtro de transformação baseado na classe base [**CTransformFilter**](ctransformfilter.md) , especificamente no método **Transform** . Esse método recebe um ponteiro para um objeto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) que encapsula os dados de vídeo. O método **IMediaSample:: Getpointr** retorna um ponteiro para o primeiro byte dos dados brutos. Para quadros não compactados, esses dados consistem em pixels que podem ser acessados ou modificados diretamente pelo filtro. As seções a seguir fornecem informações básicas que o ajudarão a trabalhar efetivamente com dados DIB dessa maneira.

> [!Note]  
> Você também pode modificar os bits usando as funções GDI, GDI+, DirectDraw ou Direct3D, mas essas técnicas estão além do escopo deste artigo.

 

Esta seção contém os seguintes tópicos:

-   [Cima para baixo versus Bottom-Up DIBs](top-down-vs--bottom-up-dibs.md)
-   [Trabalhando com RGB de 16 bits](working-with-16-bit-rgb.md)

 

 



