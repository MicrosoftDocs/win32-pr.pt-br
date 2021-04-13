---
description: Os identificadores fornecem um meio eficiente para referenciar as técnicas, as passagens, as anotações e os parâmetros com ID3DXEffectCompiler ou ID3DXEffect.
ms.assetid: 2494ecf9-88a7-43dc-a75b-ed743b11993a
title: Identificadores (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e0dbbcbbc38685cae7c89b334bfb5458bc8386
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500394"
---
# <a name="handles-direct3d-9"></a>Identificadores (Direct3D 9)

Os identificadores fornecem um meio eficiente para referenciar as técnicas, as passagens, as anotações e os parâmetros com [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) ou [**ID3DXEffect**](id3dxeffect.md). Elas são geradas dinamicamente quando você chama as funções do formulário obter \[ parâmetro de \| função de anotação \| \| técnica \| Pass \] \[ ByName \| BySemantic \| Element \] .

Durante a execução de um programa, a geração de um identificador para o mesmo objeto várias vezes retornará o mesmo identificador de volta a cada vez. Mas não confie no identificador que permanece constante quando você executa o programa várias vezes. Além disso, lembre-se de que os identificadores gerados por diferentes instâncias de [**ID3DXEffect**](id3dxeffect.md) e [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) serão diferentes.

Se você exibir os arquivos de cabeçalho, perceberá que identificadores (D3DXHANDLEs) são tecnicamente ponteiros de cadeia de caracteres.

Os identificadores que você passa para funções como getParameter \[ ByName do \| elemento \| BySemantic \] ou GetAnnotation \[ ByName \] podem estar em três formas da seguinte maneira:

1.  Identificadores que foram retornados por funções como getParameter \[ ByName do \| elemento \| BySemantic \] .
2.  Cadeias de caracteres como myVariable, mytécnicaname ou MyArray \[ 0 \] .
3.  Identificador = **nulo**. Há quatro casos.
    -   Se for um valor de retorno de método, o método não encontrará o identificador.
    -   Se um identificador **nulo** for passado como o primeiro parâmetro do elemento ByName do getParameter \[ \| \| BySemantic \] , a função retornará um parâmetro de nível superior. Por outro lado, se o identificador for não **nulo**, a função retornará um membro de estrutura ou elemento identificado pelo identificador.
    -   Se um identificador **nulo** for passado como o primeiro argumento de ValidateTechnique ou o segundo argumento de IsParameterUsed, a técnica atual será validada.
    -   Se um identificador **nulo** for passado como o primeiro argumento de FindNextValidTechnique, a pesquisa de uma técnica válida começará na primeira técnica do efeito.

Dica de desempenho no início do aplicativo, execute uma passagem de inicialização para gerar identificadores a partir das cadeias de caracteres. Desse ponto em diante, use apenas os identificadores. A passagem de cadeias de caracteres em vez de identificadores gerados é mais lenta.

## <a name="examples"></a>Exemplos

Aqui estão alguns exemplos que usam a \[ técnica obter função de anotação de parâmetro \| \| \| \| Pass \] \[ ByName \| BySemantic do \| elemento \] Functions para gerar identificadores.


```
// Gets handle of second top-level parameter handle in the effect file
h1 = GetParameter(NULL, 1);    

// Gets handle of the third struct member of MyStruct
h2 = GetParameter("MyStruct", 2); 

// Gets handle of the third array element handle of MyArray
h3 = GetParameterElement("MyArray", 2); 

// Gets handle of first member of h1 (that is, the second top-level param)
h4 = GetParameter(h1, 0);    

// Gets handle of MyStruct.Data
h5 = GetParameterByName("MyStruct", "Data");    
// or 
h6 = GetParameterByName(NULL, "MyStruct.Data");    

// Gets handle of MyStruct.Data.SubData
h7 = GetParameterByName("MyStruct.Data", "SubData"); 
// or 
h8 = GetParameterByName(NULL, "MyStruct.Data.SubData");

// Gets handle of fifth annotation of h1 (that is, second top-level param)
h9 = GetAnnotation(h1, 4);    

// Gets handle of MyStruct's annotation, called Author
h10 = GetAnnotationByName("MyStruct", "Author");  
// or
h11 = GetParameterByName(NULL, "MyStruct@Author"); 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



