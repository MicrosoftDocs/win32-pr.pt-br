---
title: Diferenças de sintaxe
description: A alteração mais aparente à medida que você se move entre linguagens de programação é a alteração na sintaxe.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454373"
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

Embora a sintaxe de cada linguagem expresse o método de forma diferente, a funcionalidade é a mesma. Em cada idioma, o método Add usa os parâmetros *time* e *Name* e retorna um objeto EnhEvent. No exemplo de C++, o método retorna o objeto usando um terceiro parâmetro de saída, *PVal*.

Normalmente, a funcionalidade de um objeto COM é a mesma em linguagens de programação. Por isso, a documentação de um objeto COM é útil mesmo se o objeto estiver documentado em outra linguagem de programação do que a que você está usando. As descrições da funcionalidade, dos parâmetros e dos valores de retorno do objeto são, com poucas exceções, válidas para todos os idiomas.

Para obter informações sobre como converter a sintaxe de um objeto COM em outra linguagem de programação, consulte [convertendo sintaxe de objeto com para linguagens de programação](translating-com-object-syntax-for-programming-languages.md).

As diferenças de sintaxe entre as linguagens de script JavaScript, JScript e VBScript são menos pronunciadas do que as diferenças de sintaxe entre as linguagens de programação mostradas anteriormente. Por exemplo, considere a função Square, pois ela é implementada em cada uma dessas três linguagens de script:

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

Observe que as linguagens de script, ao contrário das linguagens de programação, são digitadas de forma fraca. Em outras palavras, você não precisa especificar o tipo de dados de um parâmetro ou valor de retorno ao declarar uma função. Em vez disso, as variáveis são automaticamente convertidas para o tipo de dados apropriado. No caso do VBScript, todas as variáveis são do mesmo tipo de dados, **Variant**.

A sintaxe JavaScript e JScript para Square é a mesma. O JScript é amplamente compatível com o JavaScript. No entanto, o JScript inclui alguns objetos que não têm suporte no momento pelo JavaScript, como o **ActiveXObject**, o **enumerador**, o **erro**, o **global** e o **VBArray**. Para obter mais informações sobre esses objetos, consulte a [referência da linguagem JScript](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).

Na superfície, a sintaxe JavaScript e JScript é semelhante à sintaxe Java. Essa similaridade é apenas superficial. A linguagem Java foi desenvolvida independentemente do JavaScript e do JScript e não está relacionada a ambos.

O VBScript, por outro lado, é um subconjunto da linguagem de programação de Visual Basic. Por isso, a sintaxe do VBScript é um subconjunto da sintaxe Visual Basic e geralmente é intercambiável com Visual Basic sintaxe.

Para obter informações sobre como usar objetos COM em linguagens de script, consulte [scripts com objetos com](scripting-with-com-objects.md).

 

 