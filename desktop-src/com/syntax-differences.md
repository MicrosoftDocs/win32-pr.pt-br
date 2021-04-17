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
# <a name="syntax-differences"></a><span data-ttu-id="9c285-103">Diferenças de sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c285-103">Syntax Differences</span></span>

<span data-ttu-id="9c285-104">A alteração mais aparente à medida que você se move entre linguagens de programação é a alteração na sintaxe.</span><span class="sxs-lookup"><span data-stu-id="9c285-104">The most apparent change as you move between programming languages is the change in syntax.</span></span>

<span data-ttu-id="9c285-105">Considere o método Add do objeto EnhEvents, mostrado como ele é declarado em três idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="9c285-105">Consider the EnhEvents object's Add method, shown as it is declared in three different languages.</span></span>

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

<span data-ttu-id="9c285-106">Embora a sintaxe de cada linguagem expresse o método de forma diferente, a funcionalidade é a mesma.</span><span class="sxs-lookup"><span data-stu-id="9c285-106">Although the syntax of each language expresses the method differently, the functionality is the same.</span></span> <span data-ttu-id="9c285-107">Em cada idioma, o método Add usa os parâmetros *time* e *Name* e retorna um objeto EnhEvent.</span><span class="sxs-lookup"><span data-stu-id="9c285-107">In each language, the Add method takes the parameters *Time* and *Name* and returns an EnhEvent object.</span></span> <span data-ttu-id="9c285-108">No exemplo de C++, o método retorna o objeto usando um terceiro parâmetro de saída, *PVal*.</span><span class="sxs-lookup"><span data-stu-id="9c285-108">In the C++ example, the method returns the object by using a third, output parameter, *pVal*.</span></span>

<span data-ttu-id="9c285-109">Normalmente, a funcionalidade de um objeto COM é a mesma em linguagens de programação.</span><span class="sxs-lookup"><span data-stu-id="9c285-109">Typically, the functionality of a COM object is the same across programming languages.</span></span> <span data-ttu-id="9c285-110">Por isso, a documentação de um objeto COM é útil mesmo se o objeto estiver documentado em outra linguagem de programação do que a que você está usando.</span><span class="sxs-lookup"><span data-stu-id="9c285-110">Because of this, documentation for a COM object is useful even if the object is documented in another programming language than the one you are using.</span></span> <span data-ttu-id="9c285-111">As descrições da funcionalidade, dos parâmetros e dos valores de retorno do objeto são, com poucas exceções, válidas para todos os idiomas.</span><span class="sxs-lookup"><span data-stu-id="9c285-111">The descriptions of the object's functionality, parameters, and return values are, with few exceptions, valid for all languages.</span></span>

<span data-ttu-id="9c285-112">Para obter informações sobre como converter a sintaxe de um objeto COM em outra linguagem de programação, consulte [convertendo sintaxe de objeto com para linguagens de programação](translating-com-object-syntax-for-programming-languages.md).</span><span class="sxs-lookup"><span data-stu-id="9c285-112">For information about how to convert the syntax of a COM object to another programming language, see [Translating COM Object Syntax for Programming Languages](translating-com-object-syntax-for-programming-languages.md).</span></span>

<span data-ttu-id="9c285-113">As diferenças de sintaxe entre as linguagens de script JavaScript, JScript e VBScript são menos pronunciadas do que as diferenças de sintaxe entre as linguagens de programação mostradas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9c285-113">The syntax differences among the scripting languages JavaScript, JScript, and VBScript are less pronounced than the syntax differences among the programming languages shown preceding.</span></span> <span data-ttu-id="9c285-114">Por exemplo, considere a função Square, pois ela é implementada em cada uma dessas três linguagens de script:</span><span class="sxs-lookup"><span data-stu-id="9c285-114">For example, consider the square function as it is implemented in each of these three scripting languages:</span></span>

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

<span data-ttu-id="9c285-115">Observe que as linguagens de script, ao contrário das linguagens de programação, são digitadas de forma fraca.</span><span class="sxs-lookup"><span data-stu-id="9c285-115">Notice that the scripting languages, unlike the programming languages, are weakly typed.</span></span> <span data-ttu-id="9c285-116">Em outras palavras, você não precisa especificar o tipo de dados de um parâmetro ou valor de retorno ao declarar uma função.</span><span class="sxs-lookup"><span data-stu-id="9c285-116">In other words, you do not have to specify the data type of a parameter or return value when you declare a function.</span></span> <span data-ttu-id="9c285-117">Em vez disso, as variáveis são automaticamente convertidas para o tipo de dados apropriado.</span><span class="sxs-lookup"><span data-stu-id="9c285-117">Instead, the variables are automatically cast to the appropriate data type.</span></span> <span data-ttu-id="9c285-118">No caso do VBScript, todas as variáveis são do mesmo tipo de dados, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="9c285-118">In the case of VBScript, all variables are of the same data type, **Variant**.</span></span>

<span data-ttu-id="9c285-119">A sintaxe JavaScript e JScript para Square é a mesma.</span><span class="sxs-lookup"><span data-stu-id="9c285-119">The JavaScript and JScript syntax for square is the same.</span></span> <span data-ttu-id="9c285-120">O JScript é amplamente compatível com o JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9c285-120">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="9c285-121">No entanto, o JScript inclui alguns objetos que não têm suporte no momento pelo JavaScript, como o **ActiveXObject**, o **enumerador**, o **erro**, o **global** e o **VBArray**.</span><span class="sxs-lookup"><span data-stu-id="9c285-121">However, JScript includes some objects not currently supported by JavaScript, such as **ActiveXObject**, **Enumerator**, **Error**, **Global**, and **VBArray**.</span></span> <span data-ttu-id="9c285-122">Para obter mais informações sobre esses objetos, consulte a [referência da linguagem JScript](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="9c285-122">For more information about these objects, see the [JScript Language Reference](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span></span>

<span data-ttu-id="9c285-123">Na superfície, a sintaxe JavaScript e JScript é semelhante à sintaxe Java.</span><span class="sxs-lookup"><span data-stu-id="9c285-123">On the surface, JavaScript and JScript syntax resembles Java syntax.</span></span> <span data-ttu-id="9c285-124">Essa similaridade é apenas superficial.</span><span class="sxs-lookup"><span data-stu-id="9c285-124">This similarity is only superficial.</span></span> <span data-ttu-id="9c285-125">A linguagem Java foi desenvolvida independentemente do JavaScript e do JScript e não está relacionada a ambos.</span><span class="sxs-lookup"><span data-stu-id="9c285-125">The Java language was developed independently from both JavaScript and JScript and is not related to either.</span></span>

<span data-ttu-id="9c285-126">O VBScript, por outro lado, é um subconjunto da linguagem de programação de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9c285-126">VBScript, on the other hand, is a subset of the Visual Basic programming language.</span></span> <span data-ttu-id="9c285-127">Por isso, a sintaxe do VBScript é um subconjunto da sintaxe Visual Basic e geralmente é intercambiável com Visual Basic sintaxe.</span><span class="sxs-lookup"><span data-stu-id="9c285-127">Because of this, VBScript syntax is a subset of Visual Basic syntax and is often interchangeable with Visual Basic syntax.</span></span>

<span data-ttu-id="9c285-128">Para obter informações sobre como usar objetos COM em linguagens de script, consulte [scripts com objetos com](scripting-with-com-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9c285-128">For information on using COM objects in scripting languages, see [Scripting with COM Objects](scripting-with-com-objects.md).</span></span>

 

 