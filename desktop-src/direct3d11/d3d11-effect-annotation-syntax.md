---
title: Sintaxe de anotação (Direct3D 11)
description: Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe descrita nesta seção.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1109695f6239708e8f241b796b888b8d494acd7ab806b98c08352dbe3aeaee3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538560"
---
# <a name="annotation-syntax-direct3d-11"></a>Sintaxe de anotação (Direct3D 11)

Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe descrita nesta seção.



| <Valor do *nome* do *tipo de dados*  =  ; *...* ; > |
|----------------------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                   | Descrição                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo de dados*<br/> | \[no \] tipo de dados, que inclui qualquer tipo de [HLSL escalar](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , bem como o [tipo de cadeia de caracteres](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*<br/>                 | \[em \] uma cadeia de caracteres ASCII, que representa o nome da anotação.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valor*<br/>             | \[no \] valor inicial da anotação.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[em \] anotações adicionais (pares nome-valor).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Comentários

Você pode adicionar mais de uma anotação dentro dos colchetes angulares, cada uma separada por um ponto-e-vírgula. As APIs de estrutura de efeito reconhecem as anotações em variáveis globais; todas as outras anotações são ignoradas.

## <a name="example"></a>Exemplo

Veja alguns exemplos.


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

[Formato do efeito](d3d11-effect-format.md)
</dt> <dt>

[Sintaxe da variável de efeito](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

