---
description: Outros objetos de origem
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Outros objetos de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8bbc1618cb7a76e87a4837fce3905a7c9ba7455b13297e779b8be8e80c40732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790906"
---
# <a name="other-source-objects"></a>Outros objetos de origem

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Além de fontes de áudio e vídeo, [DirectShow DES (Serviços](directshow-editing-services.md) de Edição) dá suporte aos seguintes objetos de origem.

**Imagens ainda**

O DES dá suporte aos seguintes formatos de arquivo para imagens ainda:

-   Bitmap (.bpm)
-   GIF (Graphics Interchange Format)
-   JPEG (Grupo de Especialistas em Fotografia Conjunta)
-   Adaptador gráfico Targa ou Truevision (.tga): Modo 2 (RGB descompactado) em formato de 16 bits, 24 bits ou 32 bits.

Esses arquivos podem ser usados como imagens ainda ou para criar animações. Para arquivos bitmap, JPEG e Targa, se você estiver usando o arquivo como uma imagem ainda, chame o método [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) para definir a taxa de quadros como zero.

**Sequências DIB**

Dada uma série de arquivos bitmap, JPEG ou Targa, o mecanismo de renderização pode construir uma sequência DIB. Para criar uma sequência DIB, dê aos arquivos nomes sequenciais numericamente, como Image001.bmp, Image002.bmp, Image003.bmp e assim por diante. Use o primeiro arquivo na sequência como a origem. De definir a taxa de quadros para a sequência chamando [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md). O mecanismo de renderização passa pelas imagens na sequência na taxa de quadros especificada.

Se a sequência for muito curta para preencher a duração, considerando a taxa de quadros, o restante da duração será preto sólido. Nenhum erro ocorre durante a renderização.

**Fontes GIF**

O DES dá suporte a fontes GIF, incluindo GIFs animados e transparentes, usando a especificação GIF89a. Com um GIF animado, ao contrário dos outros tipos de arquivo, você não precisa definir a taxa de quadros. O arquivo GIF especifica o atraso entre cada imagem na animação.

Para dar suporte a GIFs transparentes, o DES converte regiões transparentes na imagem para o RGB triplo RGB(0,0,0). Em seguida, você pode usar [a Transição de](key-transition.md) Chave para chave em RGB(0,0,0).

O DES também converte todas as regiões pretas que se enquadram no intervalo RGB(0-7,0–7,0-7) no valor RGB(8,8,8)— exceto pelo índice de transparência, se ele estiver nesse intervalo. Essa conversão não é detectável para o olho.

**Origem da cor do vídeo**

O [objeto Fonte de Cor do](video-color-source.md) Vídeo cria uma imagem de vídeo contínua de uma cor sólida. Um uso para esse objeto é torná-lo uma camada em uma transição. Por exemplo, use-o em um vídeo de esmaeça ou esmaeça.

**Filtros de origem personalizados**

O DES pode usar um DirectShow de origem como uma origem da linha do tempo, se o filtro atender às seguintes condições:

-   Ele dá suporte à busca
-   Ele produz um formato compatível com o DES. O formato pode ser compactado desde que o sistema do usuário tenha um filtro DirectShow capaz de decodificá-lo.

Para usar uma fonte personalizada, especifique o CLSID do filtro como o GUID do subobjeto do objeto de origem. Para obter mais informações, consulte [Subobjects](subobjects.md). Para dar suporte a propriedades personalizadas, implemente-as como propriedades "put" de **IDispatch.** Somente propriedades estáticas têm suporte em objetos de origem; não há suporte para propriedades dinâmicas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com fontes](working-with-sources.md)
</dt> </dl>

 

 



