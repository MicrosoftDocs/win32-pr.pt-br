---
description: Outros objetos de origem
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Outros objetos de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646037"
---
# <a name="other-source-objects"></a>Outros objetos de origem

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Além das fontes de vídeo e áudio, os [serviços de edição do DirectShow](directshow-editing-services.md) (des) oferecem suporte aos seguintes objetos de origem.

**Imagens ainda**

O DES dá suporte aos seguintes formatos de arquivo para imagens ainda:

-   Bitmap (.bpm)
-   GIF (Graphics Interchange Format)
-   JPEG (grupo de especialistas do conjunto fotográfico)
-   Adaptador gráfico Targa ou Truevision (. tga): modo 2 (RGB não compactado) em formato de 16 bits, 24, bits ou 32 bits.

Esses arquivos podem ser usados como imagens ainda ou para criar animações. Para arquivos bitmap, JPEG e Targa, se você estiver usando o arquivo como uma imagem ainda, chame o método [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) para definir a taxa de quadros como zero.

**Sequências DIB**

Dada uma série de arquivos bitmap, JPEG ou Targa, o mecanismo de renderização pode construir uma sequência DIB. Para criar uma sequência DIB, dê aos arquivos nomes sequenciais numéricos, como Image001.bmp, Image002.bmp, Image003.bmp e assim por diante. Use o primeiro arquivo na sequência como a origem. Defina a taxa de quadros para a sequência chamando [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md). O mecanismo de renderização percorre as imagens na sequência na taxa de quadros especificada.

Se a sequência for muito curta para preencher a duração, considerando a taxa de quadros, o restante da duração será um preto sólido. Nenhum erro ocorre durante a renderização.

**Fontes GIF**

O DES dá suporte a fontes GIF, incluindo GIFs animadas e transparentes, usando a especificação GIF89a. Com um GIF animado, ao contrário dos outros tipos de arquivo, você não precisa definir a taxa de quadros. O arquivo GIF especifica o atraso entre cada imagem na animação.

Para dar suporte a GIFs transparentes, o DES converte regiões transparentes na imagem para o RGB terceto RGB (0, 0, 0). Em seguida, você pode usar a [transição de chave](key-transition.md) para a chave em RGB (0, 0, 0).

O DES também converte todas as regiões pretas que estão dentro do intervalo RGB (0 – 7, 0 – 7, 0 – 7) para o valor RGB (8, 8, 8) — exceto para o índice de transparência, se ele cair nesse intervalo. Essa conversão não é detectável para os olhos.

**Fonte de cores do vídeo**

O objeto de [fonte de cor do vídeo](video-color-source.md) cria uma imagem de vídeo contínua de uma cor sólida. Um uso para esse objeto é torná-lo uma camada em uma transição. Por exemplo, use-o em um vídeo fade-in ou esmaecimento.

**Filtros de origem personalizados**

O DES pode usar um filtro de origem do DirectShow como uma origem da linha do tempo, se o filtro atender às seguintes condições:

-   Ele dá suporte à busca
-   Ele produz um formato compatível com o DES. O formato pode ser compactado, desde que o sistema do usuário tenha um filtro do DirectShow capaz de decodificá-lo.

Para usar uma fonte personalizada, especifique o CLSID do filtro como o GUID do subobjeto do objeto de origem. Para obter mais informações, consulte [subobjetos](subobjects.md). Para dar suporte a propriedades personalizadas, implemente-as como propriedades de **IDispatch** "Put". Somente propriedades estáticas têm suporte em objetos de origem; Não há suporte para propriedades dinâmicas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com fontes](working-with-sources.md)
</dt> </dl>

 

 



