---
description: O uso de vírgulas e pontos-e-vírgulas pode ser o problema de sintaxe mais complexo no formato de arquivo, e esse uso é muito estrito. As vírgulas são usadas para separar membros da matriz; pontos-e-vírgulas encerram cada item de dados.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Uso de vírgulas e ponto e vírgula
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088795"
---
# <a name="use-of-commas-and-semicolons"></a><span data-ttu-id="76ce9-104">Uso de vírgulas e ponto e vírgula</span><span class="sxs-lookup"><span data-stu-id="76ce9-104">Use of Commas and Semicolons</span></span>

<span data-ttu-id="76ce9-105">O uso de vírgulas e pontos-e-vírgulas pode ser o problema de sintaxe mais complexo no formato de arquivo, e esse uso é muito estrito.</span><span class="sxs-lookup"><span data-stu-id="76ce9-105">Using commas and semicolons can be the most complex syntax issue in the file format, and this usage is very strict.</span></span> <span data-ttu-id="76ce9-106">As vírgulas são usadas para separar membros da matriz; pontos-e-vírgulas encerram cada item de dados.</span><span class="sxs-lookup"><span data-stu-id="76ce9-106">Commas are used to separate array members; semicolons terminate each data item.</span></span>

<span data-ttu-id="76ce9-107">Por exemplo, se um modelo for definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="76ce9-107">For example, if a template is defined in the following manner:</span></span>


```
template mytemp {
DWORD myvar;
}
```



<span data-ttu-id="76ce9-108">Em seguida, uma instância desse modelo é semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="76ce9-108">Then an instance of this template looks like the following:</span></span>


```
mytemp dataTemp {
1;
}
```



<span data-ttu-id="76ce9-109">Se um modelo que contém outro modelo for definido da seguinte maneira;</span><span class="sxs-lookup"><span data-stu-id="76ce9-109">If a template containing another template is defined in the following manner;</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



<span data-ttu-id="76ce9-110">Em seguida, uma instância desse modelo é semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="76ce9-110">Then an instance of this template looks like the following:</span></span>


```
container dataContainer {
1.1;
2; 
3;;
}
```



<span data-ttu-id="76ce9-111">Observe que a segunda linha que representa o contêiner MYTEMP dentro tem dois pontos-e-vírgulas no final da linha.</span><span class="sxs-lookup"><span data-stu-id="76ce9-111">Note that the second line that represents the mytemp inside container has two semicolons at the end of the line.</span></span> <span data-ttu-id="76ce9-112">O primeiro ponto e vírgula indica o final do item de dados, aTemp (dentro do contêiner) e o segundo ponto e vírgula indica o final do contêiner.</span><span class="sxs-lookup"><span data-stu-id="76ce9-112">The first semicolon indicates the end of the data item, aTemp (inside container), and the second semicolon indicates the end of the container.</span></span>

<span data-ttu-id="76ce9-113">Se uma matriz for definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="76ce9-113">If an array is defined in the following manner:</span></span>


```
Template mytemp {

array DWORD myvar[3];

}
```



<span data-ttu-id="76ce9-114">Em seguida, uma instância desse é semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="76ce9-114">Then an instance of this looks like the following:</span></span>


```
mytemp aTemp {
1, 2, 3;
}
```



<span data-ttu-id="76ce9-115">No exemplo de matriz, não há necessidade de os itens de dados serem separados por ponto e vírgula porque eles são delineados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="76ce9-115">In the array example, there is no need for the data items to be separated by semicolons because they are delineated by commas.</span></span> <span data-ttu-id="76ce9-116">O ponto e vírgula no final marca o fim da matriz.</span><span class="sxs-lookup"><span data-stu-id="76ce9-116">The semicolon at the end marks the end of the array.</span></span>

<span data-ttu-id="76ce9-117">Considere um modelo que contém uma matriz de itens de dados definidos por um modelo.</span><span class="sxs-lookup"><span data-stu-id="76ce9-117">Consider a template that contains an array of data items defined by a template.</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



<span data-ttu-id="76ce9-118">Uma instância desse seria semelhante ao exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="76ce9-118">An instance of this would look like the following example.</span></span>


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a><span data-ttu-id="76ce9-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76ce9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76ce9-120">Codificação de Texto</span><span class="sxs-lookup"><span data-stu-id="76ce9-120">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



