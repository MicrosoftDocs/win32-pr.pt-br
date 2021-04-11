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
# <a name="use-of-commas-and-semicolons"></a>Uso de vírgulas e ponto e vírgula

O uso de vírgulas e pontos-e-vírgulas pode ser o problema de sintaxe mais complexo no formato de arquivo, e esse uso é muito estrito. As vírgulas são usadas para separar membros da matriz; pontos-e-vírgulas encerram cada item de dados.

Por exemplo, se um modelo for definido da seguinte maneira:


```
template mytemp {
DWORD myvar;
}
```



Em seguida, uma instância desse modelo é semelhante ao seguinte:


```
mytemp dataTemp {
1;
}
```



Se um modelo que contém outro modelo for definido da seguinte maneira;


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



Em seguida, uma instância desse modelo é semelhante ao seguinte:


```
container dataContainer {
1.1;
2; 
3;;
}
```



Observe que a segunda linha que representa o contêiner MYTEMP dentro tem dois pontos-e-vírgulas no final da linha. O primeiro ponto e vírgula indica o final do item de dados, aTemp (dentro do contêiner) e o segundo ponto e vírgula indica o final do contêiner.

Se uma matriz for definida da seguinte maneira:


```
Template mytemp {

array DWORD myvar[3];

}
```



Em seguida, uma instância desse é semelhante ao seguinte:


```
mytemp aTemp {
1, 2, 3;
}
```



No exemplo de matriz, não há necessidade de os itens de dados serem separados por ponto e vírgula porque eles são delineados por vírgulas. O ponto e vírgula no final marca o fim da matriz.

Considere um modelo que contém uma matriz de itens de dados definidos por um modelo.


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



Uma instância desse seria semelhante ao exemplo a seguir.


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação de Texto](text-encoding.md)
</dt> </dl>

 

 



