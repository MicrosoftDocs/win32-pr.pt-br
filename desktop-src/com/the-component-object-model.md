---
title: O Component Object Model
description: O Component Object Model
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786a4bef59401877f642273ba7a97756232ac083
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635081"
---
# <a name="the-component-object-model"></a>O Component Object Model

O Microsoft Component Object Model (COM) é um sistema independente de plataforma, distribuído e orientado a objeto para a criação de componentes de software binários que podem interagir. O COM é a tecnologia básica para OLE (documentos compostos) da Microsoft, ActiveX (componentes habilitados para Internet), bem como outros.

Para entender COM (e, portanto, todas as tecnologias baseadas em COM), é crucial entender que não é uma linguagem orientada a objeto, mas sim um padrão. O COM não especifica como um aplicativo deve ser estruturado; os detalhes de idioma, estrutura e implementação são deixados para o desenvolvedor do aplicativo. Em vez disso, COM especifica um modelo de objeto e requisitos de programação que habilitam objetos COM (também chamados de componentes COM ou, às vezes, simplesmente *objetos*) para interagir com outros objetos. Esses objetos podem estar dentro de um único processo, em outros processos e podem até mesmo estar em computadores remotos. Eles podem ser escritos em linguagens diferentes, e podem ser estruturalmente bastante diferentes, e é por isso que COM é conhecido como um *padrão binário*; um padrão que se aplica depois que um programa é convertido em código de computador binário.

O único requisito de linguagem para o COM é que o código é gerado em uma linguagem que pode criar estruturas de ponteiros e, explícita ou implicitamente, chamar funções por meio de ponteiros. Linguagens orientadas a objeto, como C++ e Smalltalk, fornecem mecanismos de programação que simplificam a implementação de objetos COM, mas linguagens como C, Java e VBScript podem ser usadas para criar e usar objetos COM.

COM define a natureza essencial de um objeto COM. Em geral, um objeto de software é composto de um conjunto de dados e as funções que manipulam os dados. Um objeto COM é aquele no qual o acesso aos dados de um objeto é obtido exclusivamente por meio de um ou mais conjuntos de funções relacionadas. Esses conjuntos de funções são chamados de *interfaces* e as funções de uma interface são chamadas de *métodos*. Além disso, COM requer que a única maneira de obter acesso aos métodos de uma interface é por meio de um ponteiro para a interface.

Além de especificar o padrão de objeto binário básico, COM define determinadas interfaces básicas que fornecem funções comuns a todas as tecnologias baseadas em COM, e fornece um pequeno número de funções que todos os componentes exigem. O COM também define como os objetos funcionam juntos em um ambiente distribuído e adicionou recursos de segurança para ajudar a fornecer a integridade do sistema e do componente.

Os tópicos a seguir nesta seção descrevem os problemas de COM básicos relacionados à criação de objetos COM:

-   [Objetos e interfaces COM](com-objects-and-interfaces.md)
-   [Usando e implementando IUnknown](using-and-implementing-iunknown.md)
-   [Reutilizando objetos](reusing-objects.md)
-   [A biblioteca COM](the-com-library.md)
-   [Gerenciando a alocação de memória](managing-memory-allocation.md)

 

 




