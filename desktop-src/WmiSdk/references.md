---
description: A palavra-chave de referência MOF descreve um caminho de objeto e é mapeada para um \_ tipo de automação VT BSTR.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Referências (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea004a4d0a1cf160d387b07e9c9d7ac85eaaaf21851bd315ecd1bb4ba6f2b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050454"
---
# <a name="references-wmi"></a>Referências (WMI)

A palavra-chave de **referência** MOF descreve um caminho de objeto e é mapeada para um \_ tipo de automação VT BSTR. O caminho do objeto pode ser um caminho completo para um servidor e namespace, ou um caminho relativo para outro objeto no mesmo namespace. Você pode usar uma palavra-chave de **referência** para vincular duas ou mais classes juntas. O WMI dá suporte a dois tipos de caminhos de objeto, que usam para definir caminhos gerais ou específicos dentro do WMI.

A principal finalidade da palavra chave de **referência** é reduzir o tempo de transporte e a codificação entre objetos que existem inteiramente dentro do repositório WMI. Você também pode usar a palavra chave de **referência** para criar uma associação entre duas classes. Para obter mais informações, consulte [declarando uma classe de associação](declaring-an-association-class.md). Se o item referenciado estiver localizado dentro do mesmo arquivo MOF, use um alias para inicializar o valor de **referência** . Para obter mais informações, consulte [criando um alias](creating-an-alias.md).

> [!Note]  
> Quando uma palavra de chave de **referência** é aplicada a uma propriedade de chave, você pode distinguir referências de objeto pelo valor de cadeia de caracteres do objeto em vez de pelo valor de cancelamento referenciado.

 

O MOF dá suporte ao conceito de um caminho de objeto de tipo fraco e fortemente tipado. Um caminho de objeto de tipo fraco aponta para um objeto de uma classe não especificada e usa a palavra-chave **ref** com a palavra-chave [Object](object.md) . Um objeto fortemente tipado aponta para um objeto de uma classe específica e usa **ref** com o nome da classe. O exemplo a seguir descreve uma referência de **RefToAnyClass** de tipo fraco que pode apontar para qualquer instância de classe ou classe e uma referência de **RefToClassX** que pode apontar apenas para uma classe ou instância **ClassX** :

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

O exemplo a seguir descreve duas instâncias e um objeto de associação que faz referência às instâncias anteriores:

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



