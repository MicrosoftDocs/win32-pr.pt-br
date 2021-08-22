---
title: Traduzindo sintaxe de objeto COM para linguagens de programação
description: Traduzindo sintaxe de objeto COM para linguagens de programação
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6871046a80537dd39b4c9b502d945e28e46e719e637c4e6a629179dd3c6454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500076"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>Traduzindo sintaxe de objeto COM para linguagens de programação

Para chamar um objeto COM de um aplicativo escrito em uma linguagem de programação diferente da usada para escrever o objeto COM, primeiro você deve traduzir a sintaxe do objeto para a linguagem de programação. Isso pode ser feito usando as seguintes etapas:

1.  Veja a biblioteca de tipos do objeto COM na sintaxe da linguagem de programação. Isso fornece descrições das classes, interfaces, métodos, propriedades e eventos do objeto na sintaxe de linguagem usada.

    Os produtos para desenvolvedores da Microsoft fornecem várias ferramentas para ajudá-lo a exibir e converter bibliotecas de tipos. Para obter mais informações, consulte [Visualizadores e](type-library-viewers-and-conversion-tools.md) ferramentas de conversão da biblioteca de tipos [e Como Ferramentas para Desenvolvedores usar bibliotecas de tipos](how-developer-tools-use-type-libraries.md).

    Depois de exibir a biblioteca de tipos do objeto em sua linguagem de programação preferencial, você pode comparar sua sintaxe com a da documentação do objeto. Se o objeto estiver documentado em uma linguagem de programação diferente da que você está usando, os tipos de dados e a sintaxe poderão ser diferentes, mas as descrições de parâmetros, valores de retorno e a funcionalidade do objeto deverão ser as mesmas.

2.  Leve em conta quaisquer considerações especiais para traduzir para sua linguagem de programação.

    Como cada linguagem de programação define conceitos que podem não ter um equivalente em outras linguagens, algumas das funcionalidades de um objeto podem funcionar de forma diferente em outra linguagem ou não estão disponíveis. Por exemplo, a Visual Basic de programação não reconhece tipos de dados não assinados C++, como **unsignedÂ long**. Um aplicativo escrito em Visual Basic pode usar métodos COM que aceitam ou retornam variáveis de tipo de dados não assinados.

3.  Adicione o código compilado do objeto COM ao seu projeto. O código compilado normalmente está contido em um arquivo .dll ou .ocx. Essa etapa é necessária para que o compilador reconheça as classes do objeto COM. Depois de adicionar o objeto COM, seu aplicativo poderá usar suas classes e interfaces.

Os tópicos a seguir descrevem como traduzir e usar objetos COM em uma variedade de linguagens de programação:

-   [Traduzindo para C++](translating-to-c--.md)
-   [Traduzindo para Visual Basic](translating-to-visual-basic.md)
-   [Traduzindo para Java](translating-to-java.md)

Estes tópicos descrevem as ferramentas de conversão e os processos fornecidos pelos produtos para desenvolvedores da Microsoft. Para obter instruções sobre como programar objetos COM usando ferramentas de desenvolvimento criadas por outras empresas, consulte a documentação dessas ferramentas de desenvolvimento.

 

 




