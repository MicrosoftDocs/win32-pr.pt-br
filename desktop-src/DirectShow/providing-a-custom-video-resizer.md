---
description: Fornecendo um redimensionador de vídeo personalizado
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Fornecendo um redimensionador de vídeo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087468"
---
# <a name="providing-a-custom-video-resizer"></a>Fornecendo um redimensionador de vídeo personalizado

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

> [!Note]  
> Este recurso requer o DirectX 9,0 ou posterior.

 

Quando os [serviços de edição do DirectShow](directshow-editing-services.md) (des) redimensionam um clipe de fonte de vídeo, o comportamento padrão é um *StretchBlt*, que é rápido, mas sem suavização de serrilhado. Você pode alterar o comportamento de redimensionamento implementando um redimensionador personalizado como um filtro de transformação do DirectShow. O filtro deve expor a interface [**IResize**](iresize.md) , que permite que o des especifique o tamanho do vídeo de entrada e saída. Para obter informações sobre como escrever um filtro de transformação, consulte [escrevendo filtros de transformação](writing-transform-filters.md). A classe base **CTransformFilter** é recomendada como ponto de partida. Ao implementar o filtro, observe o seguinte:

-   Suporte à interface **IResize** no filtro (não nos Pins).
-   O filtro deve aceitar somente formatos [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (Format \_ VIDEOINFO). Rejeite outros tipos de formato.
-   O formato de vídeo de DES pode ser qualquer tipo RGB descompactado, incluindo o RGB de 32 bits com alfa (MEDIASUBTYPE \_ ARGB32). O filtro pode rejeitar com segurança formatos com a **altura** < 0.
-   Antes que o mecanismo de renderização Conecte o pino de saída do filtro, ele chama [**IResize::p UT \_ MediaType**](iresize-put-mediatype.md) para definir o tipo de saída. Ele também pode chamar [**IResize::p UT \_ size**](iresize-put-size.md) para ajustar o tamanho da saída. Ele pode chamar esses dois métodos em qualquer ordem, qualquer número de vezes, antes de conectar o pino de saída.
-   Depois que o mecanismo de renderização conecta o pino de saída, ele pode chamar **Put \_ size** novamente. O filtro de redimensionador deve reconectar seu pino de saída com o novo tamanho.
-   Dentro do método [**CTransformFilter:: Transform**](ctransformfilter-transform.md) do filtro, estique o vídeo de entrada para o tamanho de saída.
-   O filtro nunca deve definir o sinalizador de discontinuidade no exemplo de saída ou anexar um tipo de mídia ao exemplo de saída.
-   Para salvar o estado do filtro em um arquivo GraphEdit (. GRF), implemente a interface **IPersistStream** . (Isso é opcional, mas útil para teste.)

Para usar o filtro redimensionador, o filtro deve ser registrado como um objeto COM no sistema do usuário. Antes de o aplicativo renderizar o projeto de vídeo, consulte o mecanismo de renderização para a interface [**IRenderEngine2**](irenderengine2.md) e chame [**IRenderEngine2:: SETRESIZERGUID**](irenderengine2-setresizerguid.md) com o CLSID do filtro de redimensionador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um projeto](rendering-a-project.md)
</dt> </dl>

 

 



