---
title: Reutilando objetos
description: Reutilando objetos
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b6ef6d28b23ff2fcda5ed46d9b99a6634389793e48275c36e2f8a708f7266d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309417"
---
# <a name="reusing-objects"></a>Reutilando objetos

Uma meta importante de qualquer modelo de objeto é permitir que os autores de objeto reutilizar e estender objetos fornecidos por outras pessoas como partes de suas próprias implementações. Uma maneira de fazer isso no Microsoft Visual C++ e em outras linguagens é usando a herança de implementação *,* que permite que um objeto herde ("subclasse") algumas de suas funções de outro objeto enquanto substitui outras funções.

O problema para a interação de objeto em todo o sistema usando a herança de implementação tradicional é que o contrato (a interface) entre objetos em uma hierarquia de implementação não está claramente definido. Na verdade, ele é implícito e ambíguo. Quando o objeto pai ou filho altera sua implementação, o comportamento dos componentes relacionados pode se tornar indefinido ou não implementado. Em qualquer aplicativo individual, em que a implementação pode ser gerenciada por uma única equipe de engenharia que atualiza todos os componentes ao mesmo tempo, isso nem sempre é uma preocupação importante. Em um ambiente em que os componentes de uma equipe são construídos por meio da reutilização de caixa preta de outros componentes construídos por outras equipes, esse tipo de instabilidade prejudica a reutilização. Além disso, a herança de implementação geralmente funciona apenas dentro dos limites do processo. Isso torna a herança de implementação tradicional impraticável para sistemas grandes e em evolução compostos por componentes de software construídos por muitas equipes de engenharia.

A chave para criar componentes reutilizáveis é poder tratar o objeto como uma caixa opaca. Isso significa que o trecho de código que tenta reutilizar outro objeto não sabe nada e não precisa saber nada sobre a estrutura interna ou a implementação do componente que está sendo usado. Em outras palavras, o código que tenta reutilizar um componente depende do comportamento do objeto e não de sua implementação exata.

Para obter reutilização de caixa preta, o COM adota outros mecanismos de reutilização estabelecidos, como *contenção/delegação* e *agregação.*

> [!NOTE]  
> Para sua conveniência, o objeto que  está sendo *reutilizado* é chamado de objeto interno e o objeto que faz uso desse objeto interno é o objeto externo .

 

É importante lembrar em ambos os mecanismos como o objeto externo aparece para seus clientes. No que diz respeito aos clientes, ambos os objetos implementam qualquer interface para a qual o cliente possa obter um ponteiro. O cliente trata o objeto externo como uma caixa opaca e, portanto, não se importa, nem precisa se preocupar com a estrutura interna do objeto externo", o cliente se preocupa apenas com o comportamento.

Para obter mais informações, consulte estes tópicos:

-   [Contenção/delegação](containment-delegation.md)
-   [Agregação](aggregation.md)

 

 




