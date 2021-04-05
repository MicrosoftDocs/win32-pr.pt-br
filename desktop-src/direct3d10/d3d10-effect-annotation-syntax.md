---
description: Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe a seguir.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Sintaxe de anotação (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826713"
---
# <a name="annotation-syntax-direct3d-10"></a>Sintaxe de anotação (Direct3D 10)

Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe a seguir.



| <Valor do nome do *tipo de dados*   =  ;...; > |
|--------------------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                   | Descrição                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo de dados*<br/> | \[no \] tipo de dados, que inclui qualquer tipo de [HLSL escalar](../direct3dhlsl/dx-graphics-hlsl-scalar.md) , bem como o [tipo de cadeia de caracteres](../direct3dhlsl/dx-graphics-hlsl-scalar.md).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*<br/>                 | \[em \] uma cadeia de caracteres ASCII, que representa o nome da anotação.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valor*<br/>             | \[no \] valor inicial da anotação.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[em \] anotações adicionais (pares nome-valor).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Comentários

Você pode adicionar mais de uma anotação dentro dos colchetes angulares, cada uma separada por um ponto-e-vírgula. As APIs de estrutura de efeito reconhecem as anotações em variáveis globais; todas as outras anotações são ignoradas.

## <a name="example"></a>Exemplo

Aqui estão alguns exemplos.


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe da variável de efeito](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
