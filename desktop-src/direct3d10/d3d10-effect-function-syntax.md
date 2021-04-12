---
description: Uma função de efeito é escrita em HLSL e é declarada com a sintaxe a seguir.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Sintaxe da função de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456994"
---
# <a name="effect-function-syntax-direct3d-10"></a>Sintaxe da função de efeito (Direct3D 10)

Uma função de efeito é escrita em HLSL e é declarada com a sintaxe a seguir.

## <a name="syntax"></a>Syntax

 *Função* do ReturnType ( \[ *ArgumentList* \] )

{

<dl> \[ *Instruções* \]
</dl>

};



| Nome         | Descrição                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipoderetorno   | Qualquer [tipo de HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)                                                                                                                                                                                                       |
| FunctionName | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.                                                                                                                                                                                            |
| ArgumentList | Um ou mais argumentos, separados por vírgulas (consulte os [argumentos da função (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).                                                                                                                             |
| Instruções   | Uma ou mais instruções (consulte [instruções (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) que compõem o corpo da função. Se uma função for definida sem um corpo, será considerada um protótipo; e deve ser redefinido com um corpo antes de usar. |



 

Uma função de efeito pode ser um sombreador ou pode simplesmente ser uma função chamada por um sombreador. Uma função é identificada exclusivamente por seu nome, os tipos de seus parâmetros e a plataforma de destino; Portanto, as funções podem ser sobrecarregadas. Qualquer função HLSL válida deve se ajustar a este formato; para obter uma lista mais detalhada de sintaxe para funções HLSL, consulte [funções (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).

## <a name="example"></a>Exemplo

O [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa um sombreador de pixel e um sombreador de vértice. A função de sombreador de pixel é chamada de RenderScenePS e é mostrada abaixo.


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

[Formato do efeito](d3d10-effect-format.md)
</dt> </dl>

 

 
