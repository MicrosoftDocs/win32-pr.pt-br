---
title: Sintaxe de fluxo horizontal
description: Um sombreador Geometry com fluxo horizontal é declarado com uma sintaxe específica.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43980d79d9c338a965d7ab2f2ceb008411d9713dec935d953dd5a1854c40465b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096386"
---
# <a name="stream-out-syntax"></a>Sintaxe de fluxo horizontal

Um sombreador Geometry com fluxo horizontal é declarado com uma sintaxe específica. Este tópico descreve a sintaxe do. No tempo de execução do efeito, essa sintaxe será convertida em uma chamada para [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).

## <a name="construct-syntax"></a>Sintaxe de construção


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| Nome                   | Descrição                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Opcional. Uma cadeia de caracteres ASCI que identifica exclusivamente o nome de uma variável de sombreador de geometria com fluxo de saída. Isso é opcional porque ConstructGSWithSO pode ser colocado diretamente em uma chamada SetGeometryShader ou BindInterfaces. |
| **ShaderVar**          | Uma variável de sombreador de geometria ou de sombreador de vértice.                                                                                                                                                                               |
| **OutputDecl0**        | Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 0 são transmitidas. Veja abaixo a sintaxe.                                                                                                                                 |



 

Esta é a sintaxe definida em arquivos FX \_ 4 \_ 0. Observe que nos \_ \_ sombreadores GS 4 0 e vs \_ x, há apenas um fluxo de dados. O sombreador resultante produzirá um fluxo para a unidade de streaming e a unidade do rasterizador.


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| Nome                   | Descrição                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Opcional. Uma cadeia de caracteres ASCI que identifica exclusivamente o nome de uma variável de sombreador de geometria com fluxo de saída. Isso é opcional porque ConstructGSWithSO pode ser colocado diretamente em uma chamada SetGeometryShader ou BindInterfaces. |
| **ShaderVar**          | Uma variável de sombreador de geometria ou de sombreador de vértice.                                                                                                                                                                               |
| **OutputDecl0**        | Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 0 são transmitidas. Veja abaixo a sintaxe.                                                                                                                                 |
| **OutputDecl1**        | Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 1 são transmitidas. Veja abaixo a sintaxe.                                                                                                                                 |
| **OutputDecl2**        | Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 2 são transmitidas. Veja abaixo a sintaxe.                                                                                                                                 |
| **OutputDecl3**        | Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 3 são transmitidas. Veja abaixo a sintaxe.                                                                                                                                 |
| **RasterizedStream**   | Um inteiro que especifica qual fluxo será enviado ao rasterizador.                                                                                                                                                         |



 

Observe que \_ \_ os sombreadores GS 5 0 podem definir até quatro fluxos de dados. O sombreador resultante produzirá uma transmissão para a unidade de saída de fluxo para cada declaração de saída não **nula** e uma transmitirá a unidade rasterizadora.

## <a name="stream-out-declaration-syntax"></a>Sintaxe de declaração de saída de fluxo


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| Nome              | Descrição                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| **Buffer**        | Opcional. Um número inteiro, 0 <= buffer < 4, especificando o fluxo de buffer de saída ao qual o valor será acessado. |
| **Semântico**      | Uma cadeia de caracteres, junto com SemanticIndex, especificando qual valor deve ser impresso.                                 |
| **SemanticIndex** | Opcional. O índice associado à semântica.                                                         |
| **Mascara**          | Opcional. Uma máscara de componente, que indica os componentes do valor a serem gerados.                       |



 

Há uma semântica especial, rotulada "$SKIP", que indica uma semântica vazia, deixando a memória correspondente no buffer de saída de fluxo inalterado. A semântica de $SKIP não pode ter um SemanticIndex, mas pode ter uma máscara.

A declaração de saída do fluxo inteiro pode ser **nula**.

## <a name="example"></a>Exemplo


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




