---
description: 'Ao criar uma instância com objetos inseridos, execute as seguintes tarefas:'
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Criando objetos inseridos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2e54e16005669ebd77b0bc08e5d3174f7aa5fadee2a47477920e91aaa2ae155b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464166"
---
# <a name="creating-embedded-objects"></a>Criando objetos inseridos

Ao criar uma instância com objetos inseridos, execute as seguintes tarefas:

-   Você deve declarar um objeto inserido como fortemente digitado ou fracamente digitado.

    Um objeto fortemente digitado aponta para um objeto de uma classe específica e usa o nome da classe. Um objeto fracamente digitado aponta para um objeto de uma classe não especificada e usa a palavra-chave **object.** Ambos os objetos são mapeados para **o tipo VT \_ UNKNOWN.**

-   Você pode usar **NULL** para o valor padrão de objetos e caminhos inseridos em inicializações e declarações.
-   Ao incorporar um caminho de objeto, não coloque espaço em branco entre os elementos do caminho inserido. Por exemplo, o caminho do objeto "Class1Index=3;" não contém espaço entre o nome da propriedade "Class1index" e o valor que está sendo atribuído, que é "3".

A declaração de classe a seguir mostra como declarar objetos inseridos fortemente digitados e fracamente digitados.

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

Os exemplos a seguir descrevem como declarar objetos inseridos dentro de uma declaração de classe.

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

O exemplo a seguir descreve a inicialização de uma propriedade que é um objeto fortemente digitado e outra propriedade que é uma matriz de objetos de tipo fraco.

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



