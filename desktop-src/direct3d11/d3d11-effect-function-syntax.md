---
title: Sintaxe da função Effect (Direct3D 11)
description: Uma função de efeito é escrita em HLSL e é declarada com a sintaxe descrita nesta seção.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 945f7104d44947f37af71ce664dd99ff64362062b1d42af62af2054538bacb52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046614"
---
# <a name="effect-function-syntax-direct3d-11"></a>Sintaxe da função Effect (Direct3D 11)

Uma função de efeito é escrita em HLSL e é declarada com a sintaxe descrita nesta seção.

## <a name="syntax"></a>Syntax

*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )

{

<dl> \[ *Instruções* \]
</dl>

};



| Nome         | Descrição                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipoderetorno   | Qualquer [tipo HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.                                                                                                                                                                                            |
| Argumentlist | Um ou mais argumentos, separados por vírgulas (consulte [Argumentos de função (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).                                                                                                                             |
| Instruções   | Uma ou mais instruções (consulte [Instruções (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) que comem o corpo da função. Se uma função for definida sem um corpo, ela será considerada um protótipo; e devem ser redefinidos com um corpo antes do uso. |



 

Uma função de efeito pode ser um sombreador ou simplesmente uma função chamada por um sombreador. Uma função é identificada exclusivamente por seu nome, os tipos de seus parâmetros e a plataforma de destino; portanto, as funções podem ser sobrecarregadas. Qualquer função HLSL válida deve se ajustar a esse formato; para obter uma lista mais detalhada de sintaxe para funções HLSL, consulte [Funções (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).

## <a name="example"></a>Exemplo

A seguir está um exemplo de uma função de sombreador de pixel.


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de efeito](d3d11-effect-format.md)
</dt> </dl>

 

 