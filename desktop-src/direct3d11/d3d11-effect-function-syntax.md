---
title: Sintaxe da função de efeito (Direct3D 11)
description: Uma função de efeito é escrita em HLSL e é declarada com a sintaxe descrita nesta seção.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641119"
---
# <a name="effect-function-syntax-direct3d-11"></a>Sintaxe da função de efeito (Direct3D 11)

Uma função de efeito é escrita em HLSL e é declarada com a sintaxe descrita nesta seção.

## <a name="syntax"></a>Syntax

 *Função* do ReturnType ( \[ *ArgumentList* \] )

{

<dl> \[ *Instruções* \]
</dl>

};



| Name         | Descrição                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipoderetorno   | Qualquer [tipo de HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.                                                                                                                                                                                            |
| ArgumentList | Um ou mais argumentos, separados por vírgulas (consulte os [argumentos da função (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).                                                                                                                             |
| Instruções   | Uma ou mais instruções (consulte [instruções (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) que compõem o corpo da função. Se uma função for definida sem um corpo, será considerada um protótipo; e deve ser redefinido com um corpo antes de usar. |



 

Uma função de efeito pode ser um sombreador ou pode simplesmente ser uma função chamada por um sombreador. Uma função é identificada exclusivamente por seu nome, os tipos de seus parâmetros e a plataforma de destino; Portanto, as funções podem ser sobrecarregadas. Qualquer função HLSL válida deve se ajustar a este formato; para obter uma lista mais detalhada de sintaxe para funções HLSL, consulte [funções (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).

## <a name="example"></a>Exemplo

Veja a seguir um exemplo de uma função de sombreador de pixel.


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

[Formato do efeito](d3d11-effect-format.md)
</dt> </dl>

 

 