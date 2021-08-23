---
description: Para obter um nível de confiança para cada resultado de reconhecimento, você pode obter a propriedade Confidence do objeto RecognitionAlternate ou a propriedade Confidence do objeto Gesture.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Propriedade Confidence [Sobre o reconhecimento]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3316e9637fe6dcf820f8412724363a25dab65ce9a291b8c3c70c5bcf9c83bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093013"
---
# <a name="confidence-property-about-recognition"></a>Propriedade Confidence \[ sobre reconhecimento\]

Para obter um nível de confiança para cada resultado de reconhecimento, você pode obter a propriedade [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) do objeto [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) ou a propriedade [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) do [**objeto Gesture.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) O nível de confiança é um número que indica o grau de confiança para cada resultado de reconhecimento alternativo que o reconhecedor retorna para um segmento de reconhecimento correspondente.

A confiança é retornada como baixa, média ou alta. O aplicativo usa esses resultados para:

-   Indique ao usuário que existem várias possibilidades.
-   Classificar as alternativas por nível de confiança.

## <a name="what-affects-confidence"></a>O que afeta a confiança

Algumas das coisas que dificultam o reconhecimento de manuscrito e afetam a confiança incluem:

-   Dificuldade para determinar a segmentação de palavras

![imagem mostrando a escrita muito próxima](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   Dificuldades de caso

![imagem mostrando dificuldades com versões manuscritas da palavra "case"](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   Estilos de escrita incomuns
-   Pontuação isolada

![imagem mostrando aspas que estão muito longe do texto](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   Caracteres acentos em reconhecedores em inglês

> [!Note]  
> A avaliação de confiança está disponível apenas para Estados Unidos inglês e todos os reconhecedores de gesto nesta versão. Métodos que fornecem a propriedade de confiança para qualquer outro reconhecedor retornarão **E \_ NOTIMPL.**

 

 

 



