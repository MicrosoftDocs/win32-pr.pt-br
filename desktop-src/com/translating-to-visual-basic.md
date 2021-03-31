---
title: Convertendo para Visual Basic
description: Convertendo para Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822760"
---
# <a name="translating-to-visual-basic"></a>Convertendo para Visual Basic

Você pode adicionar um objeto COM ao seu Visual Basic projeto como uma referência ou um componente. Depois que o objeto for adicionado ao seu projeto, seu aplicativo poderá acessar suas classes e interfaces. Em seguida, você pode usar o pesquisador de objetos de Visual Basic para exibir as informações da biblioteca de tipos do objeto na sintaxe Visual Basic.

Normalmente, os controles são adicionados a um projeto, pois os componentes e os não controlados são adicionados como referências. Quando um objeto COM é adicionado como um componente, ele aparece na caixa de ferramentas Visual Basic. Novas instâncias desse objeto são criadas arrastando o ícone de objeto da caixa de ferramentas para um formulário Visual Basic ou outro tipo de contêiner. Novas instâncias de objetos COM adicionados como referências são criadas usando a **nova** palavra-chave.

A distinção entre usar uma classe como referência versus um componente é sutil, mas importante. Quando você adiciona um objeto como uma referência, você pode usar apenas a biblioteca de tipos que o controle fornece ou a biblioteca de tipos "RAW".

Se você adicionar um controle como um componente, o Visual Basic mesclará as propriedades e os métodos do extensor do formulário no qual o controle é inserido com a biblioteca de tipos do controle, fornecendo assim uma versão estendida e encapsulada da biblioteca de tipos. Com essa versão da biblioteca de tipos, você pode usar propriedades do extensor, como Top e Left, como se fossem parte do controle, em vez do contêiner do controle.

Atualmente, o Visual Basic não dá suporte a várias bibliotecas de tipos criadas em um único arquivo. dll. Se você encontrar uma DLL que incorpora várias bibliotecas de tipos, deverá obter cópias autônomas das bibliotecas de tipos da fonte que forneceu o objeto para usar o objeto com Visual Basic.

Para mais informações, consulte os seguintes tópicos:

-   [Convertendo para Visual Basic do C++](translating-to-visual-basic-from-c--.md)
-   [Convertendo para Visual Basic do Java](translating-to-visual-basic-from-java.md)
-   [Adicionando um componente a um projeto Visual Basic](adding-a-component-to-a-visual-basic-project.md)
-   [Adicionando uma referência a um projeto Visual Basic](adding-a-reference-to-a-visual-basic-project.md)
-   [Pesquisador de objetos do Visual Basic](visual-basic-object-browser.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para C++](translating-to-c--.md)
</dt> <dt>

[Convertendo para Java](translating-to-java.md)
</dt> </dl>

 

 




