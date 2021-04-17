---
description: Este tópico ajuda você a começar a criar aplicativos preparados para o mundo, especificando pré-requisitos, resumindo tecnologias e apresentando um tutorial de introdução.
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: Introdução com desenvolvimento internacional do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cc77a86b652f1b713b29517b513cddc26ed801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759663"
---
# <a name="getting-started-with-international-windows-development"></a>Introdução com desenvolvimento internacional do Windows

Este tópico ajuda você a começar a criar aplicativos preparados para o mundo, especificando pré-requisitos, resumindo tecnologias e apresentando um tutorial de introdução.

## <a name="getting-started"></a>Introdução

Se você escrever aplicativos para usuários em uma única localidade, esses aplicativos poderão ser bem-sucedidos mesmo que você os projete com suposições específicas de localidade, como a apresentação de datas em um formato específico ou a classificação de cadeias de caracteres em uma sequência específica. Mas agora você precisa garantir que seus aplicativos possam ser usados em vários países, por usuários que têm diferentes idiomas e diferentes culturas. Para obter sucesso em várias localidades, os aplicativos precisam ser ajustados para a localidade em que são executados. Essa flexibilidade é importante se você a adiciona a um aplicativo existente ou o projeta em um novo aplicativo.

Esta seção ajuda você a começar a usar o desenvolvimento internacional. Ele apresenta links para tópicos que fornecem visões gerais de pré-requisitos de internacionalização. Ele resume as tecnologias que o SDK oferece para dar suporte a clientes mundiais. Por fim, esta seção fornece um exemplo de aplicativo que resolve um problema que você costuma encontrar ao escrever software global.

## <a name="prerequisites"></a>Pré-requisitos

Você deve se familiarizar com os problemas que surgem no desenvolvimento de software internacional para Windows. Comece com essas visões gerais.

-   A [compreensão da internacionalização](understanding-internationalization.md) explica a dificuldade de desenvolver aplicativos preparados para o mundo e define os principais termos.
-   O tópico [obter preparado](https://msdn.microsoft.com/goglobal/bb895995.aspx) para o mundo leva a diretrizes e práticas recomendadas que você pode ler ou aprofundar conforme necessário.
-   A [lista de verificação de internacionalização](internationalization-checklist.md) resume as ações que você deve executar para criar um aplicativo preparado para o mundo.
-   A segurança é sempre um problema no desenvolvimento de software, mas você precisa considerar problemas adicionais ao desenvolver software internacional. Veja as considerações de [segurança: recursos internacionais](security-considerations--international-features.md).

Além disso, esteja atento aos artigos mais extensivos que podem ser encontrados no [centro de desenvolvedores do Go Global](https://msdn.microsoft.com/globalization/mt613165) na seção [passo a passo da globalização](https://msdn.microsoft.com/globalization/mt642951) . Ao desenvolver um software internacional, você desejará consultar as visões gerais adicionais e os artigos detalhados que podem ser encontrados lá.

## <a name="learning-paths"></a>Roteiros de aprendizagem

O caminho a seguir no aprendizado para criar software internacional depende dos cenários que você enfrenta. Os cenários a seguir se baseiam naqueles introduzidos no tópico principal da seção, [internacionalização para aplicativos do Windows](international-support.md).

-   **Crie aplicativos que podem ser implantados em várias regiões em vários idiomas.**

    O desafio é desenvolver um aplicativo que não precise ser reescrito para cada idioma ou cultura.

    -   Leia o artigo [noções básicas sobre o MUI (Multilingual User interface)](./about-multilingual-user-interface.md).
    -   Explore a documentação da [interface do usuário multilíngue](multilingual-user-interface.md).
    -   Introdução ao aplicativo [Hello MUI](#the-hello-mui-application) .

-   **Suporte à entrada e exibição de idiomas, conjuntos de caracteres e fontes diferentes.**

    Seu aplicativo pode precisar dar suporte a vários conjuntos de caracteres, dar suporte a scripts complexos (como aqueles usados para representar Hebraico, árabe, tailandês e idiomas índicos), permitir que o usuário selecione a partir de fontes internacionais ou permitir que o usuário insira caracteres e símbolos, como japonês kanji, para outros idiomas usando um teclado padrão.

    -   Leia os artigos:

        -   [Suporte a scripts e fontes no Windows](https://msdn.microsoft.com/globalization/mt791278)
        -   [Idioma de entrada: teclados e IMEs](https://msdn.microsoft.com/globalization/mt662332)

    -   Explore a documentação para:

        -   [Unicode e conjuntos de caracteres](unicode-and-character-sets.md)
        -   [Fontes internacionais e exibição de texto](international-fonts-and-text-display.md)
        -   [Gerenciador de métodos de entrada](input-method-manager.md)

-   **Exiba objetos dependentes de cultura em formatos apropriados.**

    Os aplicativos internacionais devem usar configurações de localidade para classificar cadeias de caracteres corretamente e para exibir informações sensíveis à cultura, como hora, datas e moeda.

    -   Explore o [centro de conhecimento de suporte ao idioma nacional](./national-language-support-reference.md).
    -   Examine a documentação do [NLS (suporte ao idioma nacional)](national-language-support.md).

-   **Descubra o idioma ou o script usado pelo usuário e aplique-o aos outros serviços do aplicativo.**

    Se seu aplicativo puder determinar o idioma no qual o texto e a entrada do usuário são gravados, ele poderá exibir o conteúdo, como prompts ou ajuda em uma linguagem compreensível.

    -   Leia o artigo [escrevendo aplicativos preparados para o mundo no Windows: serviços lingüísticos estendidos no Windows](./using-extended-linguistic-services.md).
    -   Explore a documentação de [Els (serviços lingüísticos estendidos)](extended-linguistic-services.md).

## <a name="internationalization-technologies-in-the-sdk"></a>Tecnologias de internacionalização no SDK

A seção de suporte ao desenvolvimento internacional do SDK fornece tecnologias que permitem que o aplicativo enumere idiomas, localidades e formatos específicos de localidade. Você pode usá-los em aplicativos Microsoft Win32 que você escreve em C ou C++.

Os [Serviços lingüísticos estendidos](extended-linguistic-services.md) oferecem tecnologia patenteada pela Microsoft para a identificação de idiomas e scripts em texto. Seu aplicativo pode determinar os serviços disponíveis com base na categoria, bem como no tipo de conteúdo, script e linguagem de entrada e saída.

As [fontes internacionais e a exibição de texto](international-fonts-and-text-display.md) fornecem informações sobre fontes internacionais, glifos e scripts complexos e o processamento correto da tipografia na plataforma Windows.

O [IMM (Input Method Manager)](input-method-manager.md) é uma tecnologia que ajuda o aplicativo a receber entradas do software IME (Input Method Editor), que, por sua vez, permite a entrada de caracteres e símbolos, como o japonês kanji, para outros idiomas usando um teclado padrão.

## <a name="the-hello-mui-application"></a>O aplicativo Hello MUI

Uma tarefa comum no desenvolvimento internacional começa com um aplicativo multilíngue que você deve tornar preparado para o mundo. Você precisa adicionar suporte para idiomas adicionais, mas de uma maneira que não exija que você reescreva o código para cada nova linguagem ou cultura.

Esta tarefa fornece a oportunidade de apresentar um tutorial que o conduz passo a passo por meio da criação de um aplicativo de Hello MUI, usando o modelo de recurso [MUI (Multilingual User interface)](multilingual-user-interface.md) e o suporte associado fornecido no Windows.

O tutorial adota o conceito do aplicativo Olá, Mundo familiar, demonstrando o uso do MUI para criar um aplicativo básico multilíngüe.

Você pode começar o tutorial de Hello MUI ao [Adicionar suporte à interface do usuário multilíngüe a um aplicativo](creating-a-multilingual-user-interface-application.md).

 

 
