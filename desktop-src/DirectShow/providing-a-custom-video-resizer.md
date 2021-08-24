---
description: Fornecendo um resizer de vídeo personalizado
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Fornecendo um resizer de vídeo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a006f4620accc3917ae3072846f99f7537a1eadfaab21da36aab17f17d94e433
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747896"
---
# <a name="providing-a-custom-video-resizer"></a>Fornecendo um resizer de vídeo personalizado

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

> [!Note]  
> Esse recurso requer o DirectX 9.0 ou posterior.

 

Quando DirectShow DES [(Serviços](directshow-editing-services.md) de Edição) reize um clipe de origem de vídeo, o comportamento padrão é *um StretchBlt*, que é rápido, mas não tem alias. Você pode alterar o comportamento de reizing implementando um resizer personalizado como um filtro DirectShow transformação. O filtro deve expor a interface [**IResize,**](iresize.md) que permite que o DES especifique o tamanho do vídeo de entrada e saída. Para obter informações sobre como escrever um filtro de transformação, consulte [Escrevendo filtros de transformação.](writing-transform-filters.md) A **classe base CTransformFilter** é recomendada como o ponto de partida. Ao implementar o filtro, observe o seguinte:

-   Suporte à interface **IResize** no filtro (não nos pinos).
-   O filtro deve aceitar apenas [**formatos VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (FORMAT \_ VideoInfo). Rejeitar outros tipos de formato.
-   O formato de vídeo do DES pode ser qualquer tipo RGB descompactado, incluindo RGB de 32 bits com alfa (MEDIASUBTYPE \_ ARGB32). Seu filtro pode rejeitar formatos com segurança com **biHeight** < 0.
-   Antes que o Mecanismo de Renderização conecte o pino de saída do filtro, ele chama [**IResize::p ut \_ MediaType**](iresize-put-mediatype.md) para definir o tipo de saída. Ele também pode chamar [**IResize::p ut \_ para**](iresize-put-size.md) ajustar o tamanho da saída. Ele pode chamar esses dois métodos em qualquer ordem, qualquer número de vezes, antes de conectar o pino de saída.
-   Depois que o Mecanismo de Renderização conecta o pino de saída, ele pode chamar **colocar \_ Tamanho** novamente. O filtro do resizer deve reconectar seu pino de saída com o novo tamanho.
-   Dentro do método [**CTransformFilter::Transform**](ctransformfilter-transform.md) do filtro, alonge o vídeo de entrada para o tamanho da saída.
-   O filtro nunca deve definir o sinalizador de descontinuidade no exemplo de saída ou anexar um tipo de mídia ao exemplo de saída.
-   Para salvar o estado do filtro em um arquivo GraphEdit (.grf), implemente a interface **IPersistStream.** (Isso é opcional, mas útil para teste.)

Para usar o filtro de resizer, o filtro deve ser registrado como um objeto COM no sistema do usuário. Antes de o aplicativo renderizar o projeto de vídeo, consulte o Mecanismo de Renderização para a interface [**IRenderEngine2**](irenderengine2.md) e chame [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) com o CLSID do filtro de resizer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizar um Project](rendering-a-project.md)
</dt> </dl>

 

 



