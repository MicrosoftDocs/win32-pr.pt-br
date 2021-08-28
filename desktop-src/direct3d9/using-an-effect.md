---
description: Esta página mostrará como gerar e usar um efeito.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Usando um efeito (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d240148c8817a3e480099a3ad1acb81bbff60803b0d0a8327e3a77cba681b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856096"
---
# <a name="using-an-effect-direct3d-9"></a>Usando um efeito (Direct3D 9)

Esta página mostrará como gerar e usar um efeito. Os tópicos abordados incluem como:

-   [Criar um efeito](#create-an-effect)
-   [Renderizar um efeito](#render-an-effect)
-   [Usar a semântica para localizar parâmetros de efeito](#use-semantics-to-find-effect-parameters)
-   [Use identificadores para obter e definir parâmetros com eficiência](#use-handles-to-get-and-set-parameters-efficiently)
-   [Adicionar informações de parâmetro com anotações](#add-parameter-information-with-annotations)
-   [Parâmetros de efeito de compartilhamento](#share-effect-parameters)
-   [Compilar um efeito offline](#compile-an-effect-offline)
-   [Melhorar o desempenho com preshaders](#improve-performance-with-preshaders)
-   [Usar blocos de parâmetro para gerenciar parâmetros de efeito](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a>Criar um efeito

Aqui está um exemplo de criação de um efeito obtido do [exemplo BasicHLSL](../directx-sdk--august-2009-.md). O código de criação de efeito para criar um sombreador de depuração é de **OnCreateDevice**:


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



Essa função usa estes argumentos:

-   O dispositivo.
-   O nome do arquivo de efeito.
-   Um ponteiro para uma lista terminada em nulo de \# define, a ser usado ao analisar o sombreador.
-   Um ponteiro opcional para um manipulador de inclusão escrito pelo usuário. O manipulador é chamado pelo processador sempre que ele precisa resolver um \# include.
-   Um sinalizador de compilação de sombreador que fornece as dicas de compilador sobre como o sombreador será usado. As opções incluem:
    -   Ignorando a validação, se os sombreadores bons conhecidos estiverem sendo compilados.
    -   Ignorando a otimização (às vezes usado quando as otimizações tornam a depuração mais difícil).
    -   Solicitando que as informações de depuração sejam incluídas no sombreador para que ele possa ser depurado.
-   O pool de efeitos. Se mais de um efeito usar o mesmo ponteiro de pool de memória, as variáveis globais nos efeitos serão compartilhadas entre si. Se não houver necessidade de compartilhar variáveis de efeito, o pool de memória poderá ser definido como **nulo**.
-   Um ponteiro para o novo efeito.
-   Um ponteiro para um buffer para o qual os erros de validação podem ser enviados. Neste exemplo, o parâmetro foi definido como **nulo** e não é usado.

> [!Note]  
> A partir do SDK de dezembro de 2006, o compilador do DirectX 10 HLSL agora é o compilador padrão no DirectX 9 e no DirectX 10. Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.

 

## <a name="render-an-effect"></a>Renderizar um efeito

A sequência de chamadas para a aplicação do estado de efeito em um dispositivo é:

-   [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) define a técnica ativa.
-   [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) define a passagem ativa.
-   [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) atualiza as alterações em quaisquer chamadas Set na passagem. Isso deve ser chamado antes de qualquer chamada de desenho.
-   [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) termina uma passagem.
-   [**ID3DXEffect:: End**](id3dxeffect--end.md) termina a técnica ativa.

O código de processamento de efeito também é mais simples do que o código de renderização correspondente sem um efeito. Este é o código de renderização com um efeito:


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



O loop render consiste em consultar o efeito para ver quantos passagens ele contém e, em seguida, chamar todos os passos para uma técnica. O loop de renderização pode ser expandido para chamar várias técnicas, cada uma com várias passagens.

## <a name="use-semantics-to-find-effect-parameters"></a>Usar a semântica para localizar parâmetros de efeito

Uma semântica é um identificador que é anexado a um parâmetro de efeito para permitir que um aplicativo pesquise o parâmetro. Um parâmetro pode ter no máximo uma semântica. A semântica está localizada após um sinal de dois-pontos (:) após o nome do parâmetro. Por exemplo:


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



Se você declarou a variável global Effect sem usar uma semântica, ela ficaria assim:


```
float4x4 matWorldViewProj;
```



A interface de efeito pode usar uma semântica para obter um identificador para um parâmetro de efeito específico. Por exemplo, o seguinte retorna o identificador da matriz:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



Além de Pesquisar por nome semântico, a interface de efeito tem muitos outros métodos para pesquisar parâmetros.

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a>Use identificadores para obter e definir parâmetros com eficiência

Os identificadores fornecem um meio eficiente para a referência de parâmetros de efeito, técnicas, passagens e anotações com um efeito. Identificadores (que são do tipo D3DXHANDLE) são ponteiros de cadeia de caracteres. Os identificadores que são transmitidos para funções como GetParameterxxx ou GetAnnotationxxx podem estar em uma das três formas:

-   Um identificador retornado por uma função como GetParameterxxx.
-   Uma cadeia de caracteres que contém o nome do parâmetro, da técnica, da passagem ou da anotação.
-   Um identificador definido como **nulo**.

Este exemplo retorna um identificador para o parâmetro que tem a semântica WORLDVIEWPROJ anexada a ele:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a>Adicionar informações de parâmetro com anotações

As anotações são dados específicos do usuário que podem ser anexados a qualquer técnica, passagem ou parâmetro. Uma anotação é uma maneira flexível de adicionar informações a parâmetros individuais. As informações podem ser lidas e usadas de qualquer forma que o aplicativo escolher. Uma anotação pode ser de qualquer tipo de dados e pode ser adicionada dinamicamente. As declarações de anotação são delimitadas por colchetes angulares. Uma anotação contém:

-   Um tipo de dados.
-   Um nome de variável.
-   Um sinal de igual (=).
-   O valor dos dados.
-   Um ponto e vírgula final (;).

Por exemplo, os dois exemplos anteriores neste documento contêm esta anotação:


```
texture Tex0 < string name = "tiger.bmp"; >;
```



A anotação é anexada ao objeto de textura e especifica o arquivo de textura que deve ser usado para inicializar o objeto de textura. A anotação não inicializa o objeto de textura; ela é simplesmente uma parte das informações do usuário anexadas à variável. Um aplicativo pode ler a anotação com [**ID3DXBaseEffect:: GetAnnotation**](id3dxbaseeffect--getannotation.md) ou [**ID3DXBaseEffect:: GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) para retornar a cadeia de caracteres. As anotações também podem ser adicionadas pelo aplicativo.

Cada anotação:

-   Deve ser numérico ou cadeia de caracteres.
-   Sempre deve ser inicializado com um valor padrão.
-   Pode ser associado com [técnicas e passagens (Direct3D 9)](techniques-and-passes.md) e [parâmetros de efeito](/previous-versions/windows/desktop/ee417539(v=vs.85))de nível superior.
-   Podem ser gravados e lidos com o [**ID3DXEffect**](id3dxeffect.md) ou o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).
-   Pode ser adicionado com [**ID3DXEffect**](id3dxeffect.md).
-   Não pode ser referenciado dentro do efeito.
-   Não pode ter subtipos ou subnotações.

## <a name="share-effect-parameters"></a>Parâmetros de efeito de compartilhamento

Os parâmetros de efeito são todas as variáveis não estáticas declaradas em um efeito. Isso pode incluir variáveis e anotações globais. Os parâmetros de efeito podem ser compartilhados entre diferentes efeitos declarando parâmetros com a palavra-chave "Shared" e, em seguida, criando o efeito com um pool de efeitos.

Um pool de efeitos contém parâmetros de efeito compartilhados. O pool é criado chamando [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), que retorna uma interface [**ID3DXEffectPool**](id3dxeffectpool.md) . A interface pode ser fornecida como uma entrada para qualquer uma das funções D3DXCreateEffectxxx quando um efeito é criado. Para que um parâmetro seja compartilhado entre vários efeitos, o parâmetro deve ter o mesmo nome, tipo e semântica em cada um dos efeitos compartilhados.


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



Efeitos que compartilham parâmetros devem usar o mesmo dispositivo. Isso é imposto para impedir o compartilhamento de parâmetros dependentes do dispositivo (como sombreadores ou texturas) em diferentes dispositivos. Os parâmetros são excluídos do pool sempre que os efeitos que contêm os parâmetros compartilhados são liberados. Se os parâmetros de compartilhamento não forem necessários, forneça **NULL** para o pool de efeitos quando um efeito for criado.

Os efeitos clonados usam o mesmo pool de efeitos que o efeito do qual são clonados. A clonagem de um efeito faz uma cópia exata de um efeito, incluindo variáveis globais, técnicas, passagens e anotações.

## <a name="compile-an-effect-offline"></a>Compilar um efeito offline

Você pode compilar um efeito em tempo de execução com [**D3DXCreateEffect**](d3dxcreateeffect.md), ou você pode compilar um efeito offline usando a ferramenta de compilador de linha de comando fxc.exe. O efeito no [exemplo CompiledEffect](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contém um sombreador de vértice, um sombreador de pixel e uma técnica:


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



Usando a [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para compilar o sombreador para vs \_ 1 \_ 1 gerou as seguintes instruções do sombreador de assembly:


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a>Melhorar o desempenho com preshaders

Um preshadr é uma técnica para aumentar a eficiência do sombreador ao calcular previamente as expressões de sombreador de constantes. O compilador de efeito recebe automaticamente as computações de sombreador do corpo de um sombreador e as executa na CPU antes do sombreador em execução. Consequentemente, os preshaders só funcionam com efeitos. Por exemplo, essas duas expressões podem ser avaliadas fora do sombreador antes de ser executada.


```
mul(World,mul(View, Projection));
sin(time)
```



As computações de sombreador que podem ser movidas são aquelas associadas a parâmetros uniformes; ou seja, os cálculos não são alterados para cada vértice ou pixel. Se você estiver usando efeitos, o compilador de efeito gerará e executará automaticamente um preshader para você; Não há sinalizadores a serem habilitados. Os preshaders podem reduzir o número de instruções por sombreador e também podem reduzir o número de registros constantes consumidos por um sombreador.

Imagine o compilador de efeito como um tipo de compilador com vários processadores porque ele compila o código do sombreador para dois tipos de processadores: uma CPU e uma GPU. Além disso, o compilador de efeito foi projetado para mover o código da GPU para a CPU e, portanto, melhorar o desempenho do sombreador. Isso é muito semelhante a extrair uma expressão estática para fora de um loop. Um sombreador que transforma a posição do espaço do mundo para o espaço de projeção e copia coordenadas de textura se pareceria com isso em HLSL:


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



O uso da [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para compilar o sombreador para vs \_ 1 \_ 1 gera as seguintes instruções de assembly:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Isso usa aproximadamente 14 slots e consome 9 registros constantes. Com um preshadr, o compilador move as expressões estáticas para fora do sombreador e para o preshadr. O mesmo sombreador ficaria assim com um preshadr:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Um efeito executa um preshadr logo antes de executar um sombreador. O resultado é a mesma funcionalidade com maior desempenho de sombreador porque o número de instruções que precisam ser executadas (para cada vértice ou pixel dependendo do tipo de sombreador) foi reduzido. Além disso, menos registros constantes são consumidos pelo sombreador como resultado das expressões estáticas que estão sendo movidas para o preshadr. Isso significa que os sombreadores anteriormente limitados pelo número de registros constantes que eles necessitam podem agora ser compilados porque exigem menos registros constantes. É razoável esperar uma melhoria de desempenho de 5 por cento e 20% dos preshaders.

Tenha em mente que as constantes de entrada são diferentes das constantes de saída em um preshadr. A saída C1 não é igual à entrada C1 Register. Gravar em um registro constante em um preshadr realmente grava no slot de entrada (constante) do sombreador correspondente.


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



A instrução CMP acima lerá o valor C1 do preshadr, enquanto a instrução Mul será gravada nos registros do sombreador de hardware a serem usados pelo sombreador de vértice.

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a>Usar blocos de parâmetro para gerenciar parâmetros de efeito

Os blocos de parâmetro são blocos de alterações de estado de efeito. Um bloco de parâmetro pode registrar alterações de estado, para que elas possam ser aplicadas posteriormente com uma única chamada. Crie um bloco de parâmetro chamando [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md):


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



O bloco de parâmetro salva quatro alterações aplicadas pelas chamadas à API. Chamar [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md) começa a registrar as alterações de estado. [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md) para de adicionar as alterações ao bloco de parâmetro e retorna um identificador. O identificador será usado ao chamar [**ID3DXEffect:: ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).

No [exemplo de EffectParam](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), o bloco de parâmetro é aplicado na sequência de renderização:


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



O bloco de parâmetro define o valor de todas as quatro alterações de estado logo antes de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) é chamado. Os blocos de parâmetro são uma maneira útil de definir várias alterações de estado com uma única chamada à API.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Effect](effects.md)
</dt> </dl>

 

 
