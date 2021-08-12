---
title: Trabalhar com sombreadores e recursos de sombreador
description: É hora de aprender a trabalhar com sombreadores e recursos de sombreador no desenvolvimento de seu jogo do Microsoft DirectX para Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf0152ba74dcc8dd1c602b69d854634502c928a0deefe5521bcab8999954049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288546"
---
# <a name="work-with-shaders-and-shader-resources"></a>Trabalhar com sombreadores e recursos de sombreador

É hora de aprender a trabalhar com sombreadores e recursos de sombreador no desenvolvimento de seu jogo do Microsoft DirectX para Windows 8. Vimos como configurar o dispositivo e os recursos gráficos e talvez você até tenha começado a modificar seu pipeline. Agora, vamos ver sombreadores de pixel e vértice.

Se você não estiver familiarizado com as linguagens de sombreador, uma discussão rápida será em ordem. Sombreadores são programas pequenos e de baixo nível que são compilados e executados em estágios específicos no pipeline de gráficos. Sua especialização é operações matemáticas de ponto flutuante muito rápidas. Os programas de sombreador mais comuns são:

-   **Sombreador de vértice**– executado para cada vértice em uma cena. Esse sombreador opera em elementos de buffer de vértice fornecidos pelo aplicativo de chamada e resulta minimamente em um vetor de posição de quatro componentes que será rasterizado em uma posição de pixel.
-   **Sombreador de** pixel — executado para cada pixel em um destino de renderização. Esse sombreador recebe coordenadas rasterizadas de estágios de sombreador anteriores (nos pipelines mais simples, esse seria o sombreador de vértice) e retorna uma cor (ou outro valor de 4 componentes) para essa posição de pixel, que é então escrita em um destino de renderização.

Este exemplo inclui sombreadores de vértice e pixel muito básicos que desenham apenas geometria e sombreadores mais complexos que adicionam cálculos básicos de iluminação.

Programas de sombreador são escritos em HLSL (Microsoft High Level Shader Language). A sintaxe HLSL se parece muito com C, mas sem os ponteiros. Programas de sombreador devem ser muito compactos e eficientes. Se o sombreador for compilado com muitas instruções, ele não poderá ser executado e um erro será retornado. (Observe que o número exato de instruções permitidas faz parte do [nível de recurso direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)

No Direct3D, os sombreadores não são compilados em tempo de executar; eles são compilados quando o restante do programa é compilado. Quando você compila seu aplicativo com o Microsoft Visual Studio 2013, os arquivos HLSL são compilados em arquivos CSO (.cso) que seu aplicativo deve carregar e colocar na memória da GPU antes do desenho. Certifique-se de incluir esses arquivos CSO com seu aplicativo ao empacotá-lo; eles são ativos, assim como malhas e texturas.

## <a name="understand-hlsl-semantics"></a>Entender a semântica HLSL

É importante levar algum tempo para discutir a semântica HLSL antes de continuarmos, pois elas geralmente são um ponto de confusão para novos desenvolvedores do Direct3D. Semântica HLSL são cadeias de caracteres que identificam um valor passado entre o aplicativo e um programa de sombreador. Embora eles possam ser uma variedade de cadeias de caracteres possíveis, a melhor prática é usar uma cadeia de caracteres como ou que `POSITION` `COLOR` indique o uso. Atribua essas semânticas ao construir um buffer constante ou layout de entrada. Você também pode adicionar um número de 0 a 7 à semântica, o que permite usar Registros separados para valores semelhantes. Por exemplo: COLOR0, COLOR1, COLOR2...

Semântica prefixada com "SV" são semânticas de valor do sistema que são escritas pelo programa de sombreador; o próprio jogo (em execução na CPU) não pode \_ modificá-los.  Normalmente, essas semânticas contêm valores que são entradas ou saídas de outro estágio de sombreador no pipeline de gráficos ou que são gerados inteiramente pela GPU.

Além disso, a semântica tem comportamentos diferentes quando são usados para especificar a entrada ou `SV_` saída de um estágio de sombreador. Por exemplo, (saída) contém os dados de vértice transformados durante o estágio do sombreador de vértice e ( entrada ) contém os valores de posição de pixel que foram interpolados pela GPU durante o estágio de `SV_POSITION` `SV_POSITION` rasterização.

Aqui estão algumas semânticas comuns de HLSL:

-   `POSITION`(*n*) para dados de buffer de vértice. `SV_POSITION` fornece uma posição de pixel para o sombreador de pixel e não pode ser gravado pelo seu jogo.
-   `NORMAL`(*n*) para dados normais fornecidos pelo buffer de vértice.
-   `TEXCOORD`(*n*) para dados de coordenada UV de textura fornecidos a um sombreador.
-   `COLOR`(n) para dados de cor RGBA fornecidos a um sombreador. Observe que ele é tratado de forma idêntica para coordenar dados, incluindo a interpolação do valor durante a rasterização; a semântica simplesmente ajuda a identificar que são dados de cores.
-   `SV_Target`\[n \] para escrever de um sombreador de pixel para uma textura de destino ou outro buffer de pixel.

Veremos alguns exemplos de semântica HLSL ao analisarmos o exemplo.

## <a name="read-from-the-constant-buffers"></a>Leitura dos buffers constantes

Qualquer sombreador poderá ler de um buffer constante se esse buffer estiver anexado ao estágio como um recurso. Neste exemplo, somente o sombreador de vértice recebe um buffer constante.

O buffer constante é declarado em dois locais: no código C++ e nos arquivos HLSL correspondentes que o acessarão.

Veja como o struct de buffer constante é declarado no código C++.


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



Ao declarar a estrutura para o buffer constante em seu código C++, verifique se todos os dados estão alinhados corretamente ao longo dos limites de 16 byte. A maneira mais fácil de fazer isso é usar tipos [DirectXMath,](/windows/desktop/dxmath/directxmath-portal) como **XMFLOAT4** ou **XMFLOAT4X4,** como visto no código de exemplo. Você também pode proteger contra buffers desalinhados declarando uma declaração estática:


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



Essa linha de código causará um erro no tempo de compilação se **ConstantBufferStruct** não estiver alinhado com 16 byte. Para obter mais informações sobre o alinhamento e o empacotamento de buffer constantes, consulte [Regras de empacotamento para variáveis constantes.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules)

Agora, veja como o buffer constante é declarado no sombreador de vértice HLSL.


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



Todos os buffers – constante, textura, amostra ou outros – devem ter um registro definido para que a GPU possa acessá-los. Cada estágio do sombreador permite até 15 buffers constantes e cada buffer pode conter até 4.096 variáveis constantes. A sintaxe de declaração register-usage é a seguinte:

-   **b:** _\#_ um registro para um buffer constante (**cbuffer**).
-   **t:** _\#_ um registro para um buffer de textura (**tbuffer**).
-   **s:** _\#_ um registro para um amostrador. (Um exemplo define o comportamento de busca para os texels no recurso de textura.)

Por exemplo, o HLSL para um sombreador de pixel pode levar uma textura e um exemplo como entrada com uma declaração como esta.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

É de sua responsabilidade atribuir buffers constantes aos registros – ao configurar o pipeline, você anexa um buffer constante ao mesmo slot ao qual você o atribuiu no arquivo HLSL. Por exemplo, no tópico anterior, a chamada para [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indica '0' para o primeiro parâmetro. Isso informa ao Direct3D para anexar o recurso de buffer constante para registrar 0, que corresponde à atribuição do buffer para **registrar(b0)** no arquivo HLSL.

## <a name="read-from-the-vertex-buffers"></a>Leitura dos buffers de vértice

O buffer de vértice fornece os dados de triângulo para os objetos de cena para os sombreador de vértice. Assim como no buffer constante, o struct do buffer de vértice é declarado no código C++, usando regras de empacotamento semelhantes.


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



Não há nenhum formato padrão para dados de vértice no Direct3D 11. Em vez disso, definimos nosso próprio layout de dados de vértice usando um descritor; os campos de dados são definidos usando uma matriz de [**estruturas D3D11 \_ INPUT ELEMENT \_ \_ DESC.**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) Aqui, mostramos um layout de entrada simples que descreve o mesmo formato de vértice que o struct anterior:


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



Se você adicionar dados ao formato de vértice ao modificar o código de exemplo, atualize também o layout de entrada ou o sombreador não poderá interpretá-lo. Você pode modificar o layout de vértice desta forma:


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



Nesse caso, você modificaria a definição de layout de entrada da seguinte forma.


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



Cada uma das definições de elemento de layout de entrada é prefixada com uma cadeia de caracteres, como "POSITION" ou "NORMAL"— que é a semântica que discutimos anteriormente neste tópico. É como um identificador que ajuda a GPU a identificar esse elemento ao processar o vértice. Escolha nomes comuns e significativos para seus elementos de vértice.

Assim como no buffer constante, o sombreador de vértice tem uma definição de buffer correspondente para elementos de vértice de entrada. (É por isso que fornecemos uma referência ao recurso de sombreador de vértice ao criar o layout de entrada – o Direct3D valida o layout de dados por vértice com o struct de entrada do sombreador.) Observe como a semântica é a mesma entre a definição de layout de entrada e essa declaração de buffer HLSL. No `COLOR` entanto, tem um "0" anexado a ele. Não é necessário adicionar o 0 se você tiver apenas um elemento declarado no layout, mas é uma boa prática adicioná-lo caso você opte por adicionar mais elementos de `COLOR` cor no futuro.


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a>Passar dados entre sombreadores

Os sombreadores levam tipos de entrada e retornam tipos de saída de suas funções principais após a execução. Para o sombreador de vértice definido na seção anterior, o tipo de entrada era a estrutura INPUT do VS e definimos um layout de entrada correspondente e \_ o struct do C++. Uma matriz desse struct é usada para criar um buffer de vértice no **método CreateCube.**

O sombreador de vértice retorna uma estrutura input PS, que deve conter minimamente a posição final do vértice de 4 componentes \_ (float4). Esse valor de posição deve ter a semântica do valor do sistema, , declarada para que a GPU tenha os dados necessários para `SV_POSITION` executar a próxima etapa de desenho. Observe que não há uma correspondência 1:1 entre a saída do sombreador de vértice e a entrada do sombreador de pixel; O sombreador de vértice retorna uma estrutura para cada vértice que ele recebe, mas o sombreador de pixel é executado uma vez para cada pixel. Isso porque os dados por vértice passam primeiro pelo estágio de rasterização. Este estágio decide quais pixels "cobrem" a geometria que você está desenhando, calcula dados interpolados por vértice para cada pixel e, em seguida, chama o sombreador de pixel uma vez para cada um desses pixels. A interpolação é o comportamento padrão ao rasterizar valores de saída e é essencial, em particular, para o processamento correto de dados de vetor de saída (vetores claros, normais por vértice e tangentes e outros).


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a>Revisar o sombreador de vértice

O sombreador de vértice de exemplo é muito simples: pegue um vértice (posição e cor), transforme a posição das coordenadas do modelo em coordenadas projetadas de perspectiva e retorne-a (juntamente com a cor) para o rasterizador. Observe que o valor de cor é interpolado à direita junto com os dados de posição, fornecendo um valor diferente para cada pixel, embora o sombreador de vértice não tenha realizado cálculos no valor da cor.


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



Um sombreador de vértice mais complexo, como um que configura os vértices de um objeto para sombreamento Phong, pode ser mais parecido com isso. Nesse caso, estamos aproveitando o fato de que os vetores e normais são interpolados para aproximar uma superfície de aparência suave.

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a>Revisar o sombreador de pixel

Esse sombreador de pixel neste exemplo é possivelmente a quantidade mínima absoluta de código que você pode ter em um sombreador de pixel. Ele pega os dados de cores de pixel interpolados gerados durante a rasterização e os retorna como saída, em que eles serão gravados em um destino de renderização. Que entediante!


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



A parte importante é a `SV_TARGET` semântica de valor do sistema no valor de retorno. Ele indica que a saída deve ser gravada no destino de renderização primário, que é o buffer de textura fornecido para a cadeia de permuta para exibição. Isso é necessário para sombreadores de pixel-sem os dados de cor do sombreador de pixel, o Direct3D não teria nada para ser exibido!

Um exemplo de um sombreador de pixel mais complexo para executar o sombreamento Phong pode ser semelhante a este. Como os vetores e os normais foram interpolados, não precisamos calculá-los por pixel. No entanto, precisamos renormalize-los devido a como funciona a interpolação; Conceitualmente, precisamos "girar" gradualmente o vetor a partir da direção no vértice A até a direção no vértice B, mantendo seu comprimento — a interpolação wheras, em vez disso, corta uma linha reta entre os dois pontos de extremidade de vetor.

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

Em outro exemplo, o sombreador de pixel usa seus próprios buffers de constante que contêm informações de luz e material. O layout de entrada no sombreador de vértice seria expandido para incluir dados normais, e a saída do sombreador de vértice deve incluir vetores transformados para o vértice, a luz e o vértice normal no sistema de coordenadas de exibição.

Se você tiver buffers de textura e amostras com registros atribuídos (**t** e **s**, respectivamente), poderá acessá-los no sombreador de pixel também.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

Os sombreadores são ferramentas muito poderosas que podem ser usadas para gerar recursos de procedimentos como mapas de sombra ou texturas de ruído. Na verdade, as técnicas avançadas exigem que você considere as texturas de forma mais abstrata, não como elementos visuais, mas como buffers. Eles contêm dados como informações de altura ou outros dados que podem ser amostrados no sombreador de pixel final aprovado ou nesse quadro específico como parte de uma passagem de efeitos de vários estágios. Várias amostras é uma ferramenta poderosa e o backbone de muitos efeitos visuais modernos.

## <a name="next-steps"></a>Próximas etapas

Espero que você esteja familiarizado com o DirectX 11at esse ponto e esteja pronto para começar a trabalhar em seu projeto. Aqui estão alguns links para ajudar a responder a outras perguntas que você pode ter sobre desenvolvimento com DirectX e C++:

-   [Desenvolvendo jogos](/previous-versions/windows/apps/hh452744(v=win.10))
-   [usar as ferramentas de Visual Studio para a programação de jogos DirectX](/previous-versions/windows/apps/dn166877(v=win.10))
-   [Desenvolvimento de jogos DirectX e demonstrativos de exemplo](/previous-versions/windows/apps/hh465149(v=win.10))
-   [Recursos de programação de jogos adicionais](/previous-versions/windows/apps/dn194515(v=win.10))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhar com recursos do dispositivo DirectX](work-with-dxgi.md)
</dt> <dt>

[Entender o pipeline de renderização do Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 