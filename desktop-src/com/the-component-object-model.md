---
title: O Component Object Model
description: O Component Object Model
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ad81adeaf41670468dd41bbf344a3fd7358c14f4b3cbeb2e482812a083ecfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462336"
---
# <a name="the-component-object-model"></a>O Component Object Model

O COM (Microsoft Component Object Model) é um sistema orientado a objetos independente de plataforma, distribuído para criar componentes de software binários que podem interagir. O COM é a tecnologia fundamental para o OLE (documentos compostos) da Microsoft, ActiveX (componentes habilitados para a Internet), bem como outros.

Para entender o COM (e, portanto, todas as tecnologias baseadas em COM), é crucial entender que ela não é uma linguagem orientada a objeto, mas um padrão. Nem o COM especifica como um aplicativo deve ser estruturado; os detalhes de idioma, estrutura e implementação são deixados para o desenvolvedor do aplicativo. Em vez disso, o COM especifica um modelo de objeto e requisitos de programação que permitem que objetos COM (também chamados de componentes COM ou, às vezes, simplesmente objetos *)* interajam com outros objetos. Esses objetos podem estar dentro de um único processo, em outros processos, e podem até mesmo estar em computadores remotos. Eles podem ser escritos em linguagens diferentes e podem ser estruturalmente bastante diferentes, por isso o COM é chamado de *padrão binário;* um padrão que se aplica depois que um programa é convertido em código de computador binário.

O único requisito de linguagem para COM é que o código seja gerado em uma linguagem que pode criar estruturas de ponteiros e, explicita ou implicitamente, chamar funções por meio de ponteiros. Linguagens orientadas a objeto, como C++ e Smalltalk, fornecem mecanismos de programação que simplificam a implementação de objetos COM, mas linguagens como C, Java e VBScript podem ser usadas para criar e usar objetos COM.

COM define a natureza essencial de um objeto COM. Em geral, um objeto de software é feito de um conjunto de dados e das funções que manipulam os dados. Um objeto COM é aquele no qual o acesso aos dados de um objeto é obtido exclusivamente por meio de um ou mais conjuntos de funções relacionadas. Esses conjuntos de funções são chamados *de interfaces* e as funções de uma interface são chamadas *de métodos*. Além disso, o COM requer que a única maneira de obter acesso aos métodos de uma interface seja por meio de um ponteiro para a interface.

Além de especificar o padrão de objeto binário básico, o COM define determinadas interfaces básicas que fornecem funções comuns a todas as tecnologias baseadas em COM e fornece um pequeno número de funções que todos os componentes exigem. O COM também define como os objetos funcionam juntos em um ambiente distribuído e adicionou recursos de segurança para ajudar a fornecer integridade do sistema e do componente.

Os tópicos a seguir nesta seção descrevem problemas básicos com relação à criação de objetos COM:

-   [Objetos e interfaces COM](com-objects-and-interfaces.md)
-   [Usando e implementando IUnknown](using-and-implementing-iunknown.md)
-   [Reutilando objetos](reusing-objects.md)
-   [A biblioteca COM](the-com-library.md)
-   [Gerenciando alocação de memória](managing-memory-allocation.md)

 

 




