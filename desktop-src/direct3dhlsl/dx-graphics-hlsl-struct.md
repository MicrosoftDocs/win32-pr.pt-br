---
title: Tipo de struct
description: Tipo de struct
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Tipo de struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b050a60911212a550433c5cc961a12ea52209b268330739c2f73158bf8fe1063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068136"
---
# <a name="struct-type"></a>Tipo de struct

Use a sintaxe a seguir para declarar uma estrutura usando HLSL.

*nome* do struct { \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *MemberName*;     ... };



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*
</dt> <dd>

Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da estrutura.

</dd> <dt>

<span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]
</dt> <dd>

Modificador opcional que especifica um tipo de interpolação. Consulte [Comentários](#remarks) para obter detalhes.

</dd> <dt>

<span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Tipo* \[ de *R* x *C*\]
</dt> <dd>

O tipo de membro com um tamanho de matriz de coluna (*C*) de linha opcional (*R*) x. Uma estrutura contém pelo menos um elemento; Se ele contiver mais de um elemento, os elementos serão todos do mesmo tipo. O número de linhas e colunas são inteiros sem sinal entre 1 e 4, inclusive.

</dd> <dt>

<span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*
</dt> <dd>

Uma cadeia de caracteres ASCII que identifica exclusivamente o nome do membro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um modificador de interpolação pode ser especificado em qualquer membro da estrutura ou em um argumento para uma função de sombreador de pixel. Se um modificador aparecer em ambos os locais, o modificador externo (o modificador de argumento do sombreador de pixel) ultrapassará o modificador interno (o modificador de estrutura).

Ao compilar um sombreador ou um efeito, o compilador do sombreador empacota os membros da estrutura de acordo com [as regras de empacotamento HLSL](dx-graphics-hlsl-packing-rules.md).

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a>Modificadores de interpolação introduzidos no modelo de sombreador 4

As saídas de sombreador de vértice que são usadas para entradas de sombreador de pixel são interpoladas linearmente para obter valores por pixel durante a rasterização. Para definir o método de interpolação, use qualquer um dos valores a seguir, que têm suporte no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) ou posterior. O modificador é ignorado em qualquer saída de sombreador de vértice que não seja usada como entrada de sombreador de pixel.



| Modificador de interpolação | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **linear**             | Interpolação entre entradas de sombreador; **linear** é o valor padrão se nenhum modificador de interpolação for especificado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **centróide**           | Interpolação entre exemplos que estão em algum lugar dentro da área coberta do pixel (isso pode exigir extrapolação de pontos de extremidade de um centro de pixel). A amostragem de centróide pode melhorar a suavização se um pixel for parcialmente coberto (mesmo que o pixel Center não esteja coberto). O modificador de **centróide** deve ser combinado com o modificador **linear** ou **noperspective** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **nointerpolação**    | Não interpolar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **noperspective**      | Não execute a correção de perspectiva durante a interpolação. O modificador **noperspective** pode ser combinado com o modificador de **centróide** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Nova**             | **Disponível no modelo do sombreador 4,1 e posterior** Interpolação no local de exemplo em vez de no pixel Center. Isso faz com que o sombreador de pixel seja executado por amostra em vez de por pixel. Outra maneira de fazer com que a execução por amostra seja ter uma entrada com [ \_ SAMPLEINDEX de VA semântica](dx-graphics-hlsl-semantics.md), que indica o exemplo atual. Somente as entradas com **amostra** especificada (ou entrada de SAMPLEINDEX de VA \_ ) diferem entre invocações de sombreador no pixel, enquanto outras entradas que não especificam modificadores (por exemplo, se você misturar modificadores em diferentes entradas) ainda são interpoladas no pixel Center. A invocação do sombreador de pixel e o teste de profundidade/estêncil ocorrem para cada amostra coberta no pixel. Isso às vezes é conhecido como *Superamostragem*. Por outro lado, na ausência de invocação de frequência de exemplo, conhecida como *multiamostral*, o sombreador de pixel é invocado uma vez por pixel, independentemente de quantas amostras são cobertas, enquanto o teste de profundidade/estêncil ocorre na frequência de amostragem. Ambos os modos fornecem anti-aliasing de borda equivalente. No entanto, a Superamostragem fornece melhor qualidade de sombreamento invocando o sombreador de pixel com mais frequência.<br/> |



 

<dl> 1. Ao usar um tipo int/uint, a única opção válida é **nointerpolation**.  
</dl>

Os modificadores de interpolação podem ser aplicados aos membros da estrutura ou aos [argumentos da função](dx-graphics-hlsl-function-parameters.md), ou ambos.

## <a name="examples"></a>Exemplos

Aqui estão algumas declarações de estrutura de exemplo.


```
struct struct1
{
  int    a;
}
```



Essa declaração inclui uma matriz.


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



Essa declaração inclui um modificador de interpolação.


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





