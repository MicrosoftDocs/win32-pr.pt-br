---
description: os reconhecedores criados para uso com o Windows Vista e o Windows XP Tablet PC Edition usam um conjunto de estruturas, cada uma delas chamada de malha, para passar os resultados de reconhecimento para as bibliotecas da plataforma do Tablet PC.
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: Estrutura malha do reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5610d60428bd3259672f43e45efa59c25f78b7ddc5909c363610eaf08520e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716006"
---
# <a name="recognizer-lattice-structure"></a>Estrutura malha do reconhecedor

os reconhecedores criados para uso com o Windows Vista e o Windows XP Tablet PC Edition usam um conjunto de estruturas, cada uma delas chamada de malha, para passar os resultados de reconhecimento para as bibliotecas da plataforma do Tablet PC. Em seguida, a plataforma do Tablet PC copia as informações nessas estruturas para o objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) , a coleção [**IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) e o objeto [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) .

Um ponteiro para o malha deve ser retornado pelo reconhecedor quando a plataforma chama a função [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) no identificador [HRECOCONTEXT](hrecocontext-handle.md) .

Esta seção descreve a estrutura malha em detalhes. Para obter uma visão geral dos reconhecedores e conceitos relacionados, consulte [sobre o reconhecimento de manuscrito](about-handwriting-recognition.md).

## <a name="the-need-for-a-lattice"></a>A necessidade de um malha

Um reconhecedor pode encontrar várias maneiras de quebrar um conjunto de traços de tinta em segmentos de reconhecimento. O que o reconhecedor usa como um segmento de reconhecimento depende do tipo de reconhecedor. Os reconhecedores de idioma inglês normalmente usam palavras como o segmento de reconhecimento. Outros reconhecedores podem usar caracteres, formas ou gestos como o segmento de reconhecimento. A flexibilidade das estruturas malha permite o gerenciamento lógico do grande número de resultados de reconhecimento que podem ser combinados em relações complexas.

Internamente, os reconhecedores usam um malha para manter as unidades de reconhecimento básicas para uma determinada folha de tinta. O malha também contém a pontuação, ou o nível de confiança, do resultado combinado. Além disso, o malha armazena o mapeamento de segmentos para os traços de tinta originais.

As estruturas malha são definidas no arquivo de cabeçalho rectypes. h. As estruturas malha incluem as seguintes estruturas:

-   [**RECUP \_ malha**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**\_coluna recup malha \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**\_elemento recup malha \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**Propriedades de RECUP \_ malha \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**\_Propriedade recup malha \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>Componentes do malha

Os exemplos a seguir usam os traços para a palavra "juntas", conforme mostrado na imagem a seguir. Nos exemplos, os segmentos são avaliados como uma ou mais palavras. Os números representam os traços individuais no segmento que está sendo avaliado. Observe que cada um dos caracteres "t" contém dois traços.

![traços para a palavra "juntas"](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

Um malha é composto de uma ou mais colunas, uma para cada segmento. Cada coluna, por sua vez, contém um ou mais elementos. Um elemento mantém uma alternativa de reconhecimento discreto. Para obter mais informações sobre colunas, consulte a estrutura de [**\_ \_ coluna recup malha**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) . Para obter mais informações sobre elementos, consulte a estrutura do [**\_ \_ elemento recup malha**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element) .

O reconhecedor pode retornar um único segmento ao avaliar o exemplo de tinta mostrado no exemplo anterior. Nesse caso, o malha contém uma única coluna com um único elemento.

Um exemplo mais complexo apresenta a si mesmo quando o reconhecedor avalia o exemplo de tinta e apresenta vários segmentos e várias alternativas para cada segmento.

O número de alternativas de reconhecimento pode ser escalonado, mesmo para uma amostra de tinta pequena. Por exemplo, "t o g e t h e r" podem produzir os seguintes resultados:

-   "para obter a sua" (além de alternativas para cada palavra)
-   "para reunir" (além de alternativas para cada palavra)
-   "para obter a sua" (além de alternativas para cada palavra)
-   "juntos" (além de alternativas para a palavra)

Nesse caso, um reconhecedor pode criar a seguinte estrutura malha.

![estrutura malha para a palavra "juntas"](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> Cada coluna compartilha a mesma ordem de traço porque todas se referem à mesma coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

 

 

 
