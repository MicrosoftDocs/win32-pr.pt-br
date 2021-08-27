---
description: Implemente o suporte para negociação de tipo de mídia como parte da gravação de um filtro de transformação. O tipo de mídia descreve o formato dos dados.
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: Etapa 3. Suporte à negociação de tipo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1558d5b1a7fd9db41fef7e5a9818d93c306f4f15f42099d4cb88f66b34725660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051466"
---
# <a name="step-3-support-media-type-negotiation"></a>Etapa 3. Suporte à negociação de tipo de mídia

Esta é a etapa 3 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).

Quando dois Pins se conectam, eles devem concordar com um tipo de mídia para a conexão. O tipo de mídia descreve o formato dos dados. Sem o tipo de mídia, um filtro pode fornecer um tipo de dados, apenas para que outro filtro o trate como algo mais.

O mecanismo básico para negociar tipos de mídia é o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) . O pino de saída chama esse método no pino de entrada com um tipo de mídia proposto. O PIN de entrada aceita a conexão ou a rejeita. Se ele rejeitar a conexão, o pino de saída poderá tentar outro tipo de mídia. Se nenhum tipo adequado for encontrado, a conexão falhará. Opcionalmente, o pino de entrada pode anunciar uma lista de tipos que ele prefere, por meio do método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) . O pino de saída pode usar essa lista quando propõe tipos de mídia, embora não seja necessário.

A classe **CTransformFilter** implementa uma estrutura geral para esse processo, da seguinte maneira:

-   O PIN de entrada não tem nenhum tipo de mídia preferencial. Ele se baseia inteiramente no filtro upstream para propor o tipo de mídia. Para dados de vídeo, isso faz sentido, pois o tipo de mídia inclui o tamanho da imagem e a taxa de quadros. Normalmente, essas informações devem ser fornecidas por um filtro de origem upstream ou um filtro de analisador. No caso de dados de áudio, o conjunto de formatos possíveis é menor, portanto, pode ser prático para o pino de entrada oferecer alguns tipos preferenciais. Nesse caso, substitua [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) no pino de entrada.
-   Quando o filtro upstream propõe um tipo de mídia, o pino de entrada chama o método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) , que aceita ou rejeita o tipo.
-   O pino de saída não será conectado, a menos que o PIN de entrada seja conectado primeiro. Esse comportamento é típico para filtros de transformação. Na maioria dos casos, o filtro deve determinar o tipo de entrada antes de poder definir o tipo de saída.
-   Quando o pino de saída se conecta, ele tem uma lista de tipos de mídia que ele propõe ao filtro downstream. Ele chama o método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) para gerar essa lista. O pino de saída também tentará quaisquer tipos de mídia que o filtro de downstream propõe.
-   Para verificar se um tipo de saída específico é compatível com o tipo de entrada, o pino de saída chama o método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .

Os três métodos **CTransformFilter** listados anteriormente são métodos virtuais puros, portanto, sua classe derivada deve implementá-los. Nenhum desses métodos pertence a uma interface COM; Eles são simplesmente parte da implementação fornecida pelas classes base.

As seções a seguir descrevem cada método em mais detalhes:

-   [Etapa 3A. Implementar o método CheckInputType](step-3a--implement-the-checkinputtype-method.md)
-   [Etapa 3B. Implementar o método GetMediaType](step-3b--implement-the-getmediatype-method.md)
-   [Etapa 3C. Implementar o método CheckTransform](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[como os filtros Conexão](how-filters-connect.md)
</dt> <dt>

[gravando filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



