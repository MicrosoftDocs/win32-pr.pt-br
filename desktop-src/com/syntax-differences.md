---
title: Diferenças de sintaxe
description: A alteração mais aparente à medida que você se move entre linguagens de programação é a alteração na sintaxe.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef58f92bf87d877c2c55a73fe5f717b93c359119e5ca6aa73fc1aeee531d858
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678386"
---
# <a name="syntax-differences"></a>Diferenças de sintaxe

A alteração mais aparente à medida que você se move entre linguagens de programação é a alteração na sintaxe.

Considere o método Add do objeto EnhEvents, mostrado como ele é declarado em três idiomas diferentes.

``` syntax
object.Add(Time As Double, Name As String) As Variant

HRESULT Add(
  double Time, 
  BSTR Name, 
  VARIANT* pVal
);
 
public com.ms.com.Variant Add( 
  double Time, 
  java.lang.String Name
);
 
```

Embora a sintaxe de cada linguagem expresse o método de forma diferente, a funcionalidade é a mesma. Em cada idioma, o método Add pega os parâmetros *Time* e *Name* e retorna um objeto EnhEvent. No exemplo do C++, o método retorna o objeto usando um terceiro parâmetro de saída, *pVal*.

Normalmente, a funcionalidade de um objeto COM é a mesma entre linguagens de programação. Por isso, a documentação de um objeto COM é útil mesmo que o objeto seja documentado em outra linguagem de programação do que a que você está usando. As descrições da funcionalidade, dos parâmetros e dos valores de retorno do objeto são válidas, com poucas exceções, para todos os idiomas.

Para obter informações sobre como converter a sintaxe de um objeto COM em outra linguagem de programação, consulte Traduzindo sintaxe de [objeto COM para linguagens de programação](translating-com-object-syntax-for-programming-languages.md).

As diferenças de sintaxe entre as linguagens de script JavaScript, JScript e VBScript são menos pronunciadas do que as diferenças de sintaxe entre as linguagens de programação mostradas anteriormente. Por exemplo, considere a função quadrada como ela é implementada em cada uma dessas três linguagens de script:

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

Observe que as linguagens de script, ao contrário das linguagens de programação, são fracamente digitados. Em outras palavras, você não precisa especificar o tipo de dados de um parâmetro ou valor de retorno ao declarar uma função. Em vez disso, as variáveis são automaticamente lançadas para o tipo de dados apropriado. No caso do VBScript, todas as variáveis são do mesmo tipo de dados, **Variant**.

A sintaxe javaScript e JScript para quadrado é a mesma. JScript é amplamente compatível com JavaScript. No entanto, JScript inclui alguns objetos que atualmente não são suportados pelo JavaScript, como **ActiveXObject,** **Enumerator**, **Error**, **Global** e **VBArray.** Para obter mais informações sobre esses objetos, consulte [o JScript De referência de linguagem.](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100))

Na superfície, a sintaxe javaScript e JScript é semelhante à sintaxe Java. Essa similaridade é apenas superficial. A linguagem Java foi desenvolvida independentemente do JavaScript e JScript e não está relacionada a nenhum dos dois.

O VBScript, por outro lado, é um subconjunto da linguagem Visual Basic programação. Por isso, a sintaxe do VBScript é um subconjunto da sintaxe Visual Basic e geralmente é intercambiável com Visual Basic sintaxe.

Para obter informações sobre como usar objetos COM em linguagens de script, consulte [Scripts com objetos COM](scripting-with-com-objects.md).

 

 