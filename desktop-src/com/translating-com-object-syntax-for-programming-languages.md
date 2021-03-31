---
title: Convertendo sintaxe de objeto COM para linguagens de programação
description: Convertendo sintaxe de objeto COM para linguagens de programação
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822559"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>Convertendo sintaxe de objeto COM para linguagens de programação

Para chamar um objeto COM de um aplicativo escrito em uma linguagem de programação diferente daquela usada para gravar o objeto COM, você deve primeiro converter a sintaxe do objeto em sua linguagem de programação. Isso pode ser feito usando as seguintes etapas:

1.  Exiba a biblioteca de tipos do objeto COM na sintaxe da linguagem de programação. Isso fornece descrições das classes, interfaces, métodos, propriedades e eventos do objeto na sintaxe de linguagem usada.

    Os produtos de desenvolvedor da Microsoft fornecem várias ferramentas para ajudá-lo a exibir e converter bibliotecas de tipos. Para obter mais informações, consulte [visualizadores de biblioteca de tipos e ferramentas de conversão](type-library-viewers-and-conversion-tools.md) e [como ferramentas para desenvolvedores usar bibliotecas de tipos](how-developer-tools-use-type-libraries.md).

    Depois de exibir a biblioteca de tipos do objeto em sua linguagem de programação preferida, você pode comparar sua sintaxe com essa na documentação do objeto. Se o objeto estiver documentado em uma linguagem de programação diferente daquela que você está usando, os tipos de dados e a sintaxe poderão ser diferentes, mas as descrições dos parâmetros, os valores de retorno e a funcionalidade do objeto deverão ser iguais.

2.  Leve em consideração quaisquer considerações especiais para a tradução para a linguagem de programação.

    Como cada linguagem de programação define conceitos que podem não ter um equivalente em outras linguagens, parte da funcionalidade de um objeto pode funcionar de modo diferente em outra linguagem ou não estar disponível. Por exemplo, a linguagem de programação Visual Basic não reconhece tipos de dados C++ não assinados, como **unsignedÂ Long**. Um aplicativo escrito em Visual Basic não pode usar métodos COM que aceitem ou retornem variáveis de tipo de dados não assinado.

3.  Adicione o código compilado do objeto COM ao seu projeto. O código compilado normalmente está contido em um arquivo. dll ou. ocx. Essa etapa é necessária para que o compilador reconheça as classes do objeto COM. Depois de adicionar o objeto COM, seu aplicativo poderá usar suas classes e interfaces.

Os tópicos a seguir descrevem como converter e usar objetos COM em uma variedade de linguagens de programação:

-   [Convertendo para C++](translating-to-c--.md)
-   [Convertendo para Visual Basic](translating-to-visual-basic.md)
-   [Convertendo para Java](translating-to-java.md)

Estes tópicos descrevem as ferramentas de conversão e os processos fornecidos pelos produtos de desenvolvedor da Microsoft. Para obter instruções sobre como programar objetos COM usando ferramentas de desenvolvimento criadas por outras empresas, consulte a documentação das ferramentas de desenvolvimento.

 

 




