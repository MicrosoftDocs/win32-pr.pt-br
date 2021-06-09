---
title: Usando sombreadores no Direct3D 10
description: Usando sombreadores no Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0d6212851e4603aac4db7ec85dd20714dc87774
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826284"
---
# <a name="using-shaders-in-direct3d-10"></a>Usando sombreadores no Direct3D 10

O pipeline tem três estágios de sombreador e cada um é programado com um sombreador HLSL. Todos os sombreadores do Direct3D 10 são escritos em HLSL, direcionando o modelo de sombreador 4.


Diferenças entre o Direct3D 9 e o Direct3D 10:

- Ao contrário dos modelos de sombreador do Direct3D 9 que poderiam ser criados em uma linguagem de assembly intermediária, os sombreadores do modelo do sombreador 4,0 são criados apenas no HLSL. A compilação offline de sombreadores em um código de bytes de consumo de dispositivo ainda tem suporte e é recomendada para a maioria dos cenários.



 

Este exemplo usa apenas um sombreador de vértice. Como todos os sombreadores são criados a partir do principal sombreador comum, aprender a usar um sombreador de vértice é muito semelhante a usar um sombreador ou uma geometria de pixel.

Depois de criar um sombreador HLSL (Este exemplo usa o HLSLWithoutFX de sombreador de vértice. VSH), será necessário prepará-lo para o estágio de pipeline específico que o usará. Para fazer isso, você precisa:

-   [Compilar um sombreador](#compile-a-shader)
-   [Criar um objeto de sombreador](#create-a-shader-object)
-   [Definir o objeto do sombreador](#set-the-shader-object)
-   [Repetir para todos os 3 estágios de sombreador](#repeat-for-all-3-shader-stages)

Essas etapas precisam ser repetidas para cada sombreador no pipeline.

## <a name="compile-a-shader"></a>Compilar um sombreador

A primeira etapa é compilar o sombreador para verificar se você códigou as instruções HLSL corretamente. Isso é feito chamando D3D10CompileShader e fornecendo-o com vários parâmetros, conforme mostrado aqui:


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



Essa função usa os seguintes parâmetros:

-   O nome do arquivo (e o comprimento da cadeia de caracteres de nome em bytes) que contém o sombreador. Este exemplo usa um sombreador de vértice somente (no arquivo HLSLWithoutFX. VSH em que a extensão de arquivo. VSH é uma abreviação do sombreador de vértice).
-   O nome da função de sombreador. Este exemplo compila um sombreador de vértice da função Ripple que usa uma única entrada e retorna uma struct de saída (a função é do exemplo HLSLWithoutFX):
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   Um ponteiro para todas as macros usadas pelo sombreador. Use \_ \_ a macro do sombreador d3d10 para ajudar a definir suas macros; basta criar uma cadeia de caracteres de nome que contenha todos os nomes de macro (com cada nome separado por um espaço) e uma cadeia de caracteres de definição (com cada corpo de macro separado por um espaço). As duas cadeias de caracteres precisam ser terminadas em nulo.
-   Um ponteiro para qualquer outro arquivo que você precise incluir para obter os sombreadores a serem compilados. Isso usa a interface ID3D10Include que tem dois métodos implementados pelo usuário: abrir e fechar. Para fazer isso funcionar, você precisará implementar o corpo dos métodos Open e close; no método Open, adicione o código que você usaria para abrir qualquer um dos arquivos de inclusão desejados, na função fechar, adicione o código para fechar os arquivos quando terminar de usá-los.
-   O nome da função de sombreador a ser compilada. Este sombreador compila a função Ripple.
-   O perfil do sombreador a ser direcionado durante a compilação. Como você pode compilar uma função em um vértice, geometria ou sombreador de pixel, o perfil informa ao compilador qual tipo de sombreador e qual modelo de sombreador comparar o código.
-   Sinalizadores do compilador do sombreador. Esses sinalizadores informam ao compilador quais informações devem ser colocadas na saída compilada e como você deseja que o código de saída seja otimizado: para velocidade, para depuração etc. Consulte [constantes de efeito (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) para obter uma lista dos sinalizadores disponíveis. O exemplo contém algum código que você pode usar para definir os valores de sinalizador do compilador para seu projeto – isso é principalmente uma pergunta se você deseja ou não gerar informações de depuração.
-   Um ponteiro para o buffer que contém o código de sombreador compilado. O buffer também contém qualquer informação de tabela de depuração e símbolo inserida solicitada pelos sinalizadores do compilador.
-   Um ponteiro para um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação, que são as mesmas mensagens que você veria na saída de depuração se estivesse executando o depurador durante a compilação do sombreador. **NULL** é um valor aceitável quando você não deseja que os erros sejam retornados a um buffer.

Se o sombreador for compilado com êxito, um ponteiro para o código do sombreador será retornado como uma interface ID3D10Blob. Ele é chamado de interface de blob porque o ponteiro é para um local na memória composto por uma matriz de DWORD. A interface é fornecida para que você possa obter um ponteiro para o sombreador compilado que será necessário na próxima etapa.

A partir do SDK de dezembro de 2006, o compilador do DirectX 10 HLSL agora é o compilador padrão no DirectX 9 e no DirectX 10. Confira [ferramenta de compilador de efeito](/windows/desktop/direct3dtools/fxc) para obter detalhes.

### <a name="get-a-pointer-to-a-compiled-shader"></a>Obter um ponteiro para um sombreador compilado

Vários métodos de API exigem um ponteiro para um sombreador compilado. Esse argumento é geralmente chamado de *pShaderBytecode* porque aponta para um sombreador compilado representado como uma sequência de códigos de bytes. Para obter um ponteiro para um sombreador compilado, primeiro compile o sombreador chamando [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) ou uma função semelhante. Se a compilação for bem-sucedida, o sombreador compilado será retornado em uma interface [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) . Por fim, use o método [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) para retornar o ponteiro.

## <a name="create-a-shader-object"></a>Criar um objeto de sombreador

Depois que o sombreador for compilado, chame CreateVertexShader para criar o objeto Shader:


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



Para criar o objeto Shader, passe o ponteiro para o sombreador compilado em CreateVertexShader. Como você teve que compilar o sombreador com êxito primeiro, essa chamada quase certamente será aprovada, a menos que você tenha um problema de memória em seu computador.

Você pode criar quantos objetos de sombreador desejar e simplesmente manter os ponteiros para eles. Esse mesmo mecanismo funciona para os sombreadores de geometria e pixel, supondo que você corresponda aos perfis de sombreador (quando você chama o método Compile) para os nomes de interface (quando você chama o método Create).

## <a name="set-the-shader-object"></a>Definir o objeto do sombreador

A última etapa é definir o sombreador para o estágio do pipeline. Como há três estágios de sombreador no pipeline, você precisará fazer três chamadas à API, uma para cada estágio.


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



A chamada para VSSetShader usa o ponteiro para o sombreador de vértice criado na etapa 1. Isso define o sombreador no dispositivo. O estágio do sombreador de vértice agora é inicializado com seu código de sombreador de vértice, tudo o que resta é inicializar qualquer variável de sombreador.

## <a name="repeat-for-all-3-shader-stages"></a>Repetir para todos os 3 estágios de sombreador

Repita esse mesmo conjunto de etapas para criar qualquer sombreador de pixel ou vértice ou até mesmo um sombreador de geometria que produz o sombreador de pixel.

## <a name="related-topics"></a>Tópicos Relacionados

[Compilar um sombreador](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

