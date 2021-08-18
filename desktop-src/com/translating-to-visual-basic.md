---
title: Traduzindo para Visual Basic
description: Traduzindo para Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9aa8a163141c6361df464a22ce873770c8385607bdf8f84d333d204c55a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550610"
---
# <a name="translating-to-visual-basic"></a>Traduzindo para Visual Basic

Você pode adicionar um objeto COM ao seu projeto Visual Basic como uma referência ou um componente. Depois que o objeto é adicionado ao seu projeto, seu aplicativo pode acessar suas classes e interfaces. Em seguida, você pode usar o Visual Basic Object Browser para exibir as informações da biblioteca de tipos do objeto Visual Basic sintaxe.

Normalmente, os controles são adicionados a um projeto como componentes e não controles são adicionados como referências. Quando um objeto COM é adicionado como um componente, ele aparece na caixa Visual Basic ferramentas. Novas instâncias desse objeto são criadas arrastando o ícone de objeto da caixa de ferramentas para Visual Basic formulário ou outro tipo de contêiner. Novas instâncias de objetos COM adicionadas como referências são criadas usando a **nova palavra-chave** .

A distinção entre usar uma classe como uma referência versus um componente é sutil, mas importante. Ao adicionar um objeto como referência, você pode usar apenas a biblioteca de tipos que o controle fornece ou a biblioteca de tipos "brutos".

Se você adicionar um controle como um componente, o Visual Basic mesclará as propriedades e métodos do extensor do formulário no qual o controle é inserido com a biblioteca de tipos do controle, fornecendo, assim, uma versão estendida e empacotada da biblioteca de tipos. Com essa versão da biblioteca de tipos, você pode usar propriedades de extensor, como Top e Left, como se elas fossem parte do controle, em vez do contêiner do controle.

Visual Basic atualmente não dá suporte a várias bibliotecas de tipos criadas em um único .dll arquivo. Se você tiver uma DLL que incorpora várias bibliotecas de tipos, deverá obter cópias autônomos das bibliotecas de tipo da origem que forneceu o objeto para usar o objeto com Visual Basic.

Para obter mais informações, consulte estes tópicos:

-   [Traduzindo para Visual Basic do C++](translating-to-visual-basic-from-c--.md)
-   [Traduzindo para Visual Basic do Java](translating-to-visual-basic-from-java.md)
-   [Adicionando um componente a um Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
-   [Adicionando uma referência a um Visual Basic Project](adding-a-reference-to-a-visual-basic-project.md)
-   [Visual Basic Pesquisador de Objetos](visual-basic-object-browser.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Traduzindo para C++](translating-to-c--.md)
</dt> <dt>

[Traduzindo para Java](translating-to-java.md)
</dt> </dl>

 

 




