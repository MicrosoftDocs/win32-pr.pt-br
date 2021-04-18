---
title: Reutilizando objetos
description: Reutilizando objetos
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/08/2020
ms.locfileid: "104499013"
---
# <a name="reusing-objects"></a>Reutilizando objetos

Um objetivo importante de qualquer modelo de objeto é permitir que os autores de objetos reutilizem e estendam objetos fornecidos por outras pessoas como partes de suas próprias implementações. Uma maneira de fazer isso na Microsoft Visual C++ e em outras linguagens é usar a *herança de implementação*, que permite que um objeto herde ("subclasse") algumas de suas funções de outro objeto ao substituir outras funções.

O problema para a interação de objetos de todo o uso da herança de implementação tradicional é que o contrato (a interface) entre objetos em uma hierarquia de implementação não é claramente definido. Na verdade, ele é implícito e ambíguo. Quando o objeto pai ou filho altera sua implementação, o comportamento dos componentes relacionados pode se tornar indefinido ou unstably implementado. Em qualquer aplicativo único, onde a implementação pode ser gerenciada por uma única equipe de engenharia que atualiza todos os componentes ao mesmo tempo, isso nem sempre é uma grande preocupação. Em um ambiente em que os componentes de uma equipe são criados por meio da reutilização da caixa preta de outros componentes criados por outras equipes, esse tipo de instabilidade compromete a reutilização. Além disso, a herança de implementação geralmente funciona apenas dentro dos limites do processo. Isso torna a herança de implementação tradicional impraticável para sistemas grandes e em evolução compostos por componentes de software criados por muitas equipes de engenharia.

A chave para a criação de componentes reutilizáveis é poder tratar o objeto como uma caixa opaca. Isso significa que a parte do código que tenta reutilizar outro objeto não sabe nada e precisa saber nada, sobre a estrutura interna ou a implementação do componente que está sendo usado. Em outras palavras, o código que tenta reutilizar um componente depende do comportamento do objeto e não da sua implementação exata.

Para obter a reutilização de caixa preta, o COM adota outros mecanismos de reusabilidade estabelecidos, como *contenção/delegação* e *agregação*.

> [!NOTE]  
> Para sua conveniência, o objeto que está sendo reutilizado é chamado de *objeto interno* e o objeto que faz uso desse objeto interno é o *objeto externo*.

 

É importante lembrar-se de ambos os mecanismos como o objeto externo aparece para seus clientes. No que diz respeito aos clientes, ambos os objetos implementam qualquer interface para a qual o cliente possa obter um ponteiro. O cliente trata o objeto externo como uma caixa opaca e, portanto, não se importa, nem precisa se preocupar com a estrutura interna do objectâ externo. "o cliente se preocupa apenas com o comportamento.

Para mais informações, consulte os seguintes tópicos:

-   [Contenção/delegação](containment-delegation.md)
-   [Agregação](aggregation.md)

 

 




