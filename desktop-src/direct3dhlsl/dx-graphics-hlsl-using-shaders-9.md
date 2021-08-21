---
title: Usando sombreadores no Direct3D 9
description: Usando sombreadores no Direct3D 9
ms.assetid: 8d8f5124-fbf3-4af5-8399-43ba28aa6eb9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1ef04c14682aa6e763222fd0c8db0e2eedf33abf747da97a16b2b1621e1c42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119740"
---
# <a name="using-shaders-in-direct3d-9"></a>Usando sombreadores no Direct3D 9

-   [Compilando um sombreador para hardware específico](#compiling-a-shader-for-specific-hardware)
-   [Inicializando constantes do sombreador](#initializing-shader-constants)
-   [Associando um parâmetro de sombreador a um registro específico](#binding-a-shader-parameter-to-a-particular-register)
-   [Renderizando um sombreador programável](#rendering-a-programmable-shader)
-   [Depurando sombreadores](#debugging-shaders)
-   [Tópicos relacionados](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a>Compilando um sombreador para hardware específico

Os sombreadores foram adicionados primeiro ao Microsoft DirectX no DirectX 8,0. Nesse momento, várias máquinas virtuais de sombreador foram definidas, cada uma correspondendo aproximadamente a um processador gráfico específico produzido pelos principais fornecedores de gráficos 3D. Para cada um desses computadores de sombreador virtual, uma linguagem de assembly foi projetada. Os programas escritos nos modelos de sombreador (nomes vs \_ 1 \_ e PS \_ 1 \_ 1-PS \_ 1 \_ 4) eram relativamente curtos e geralmente eram escritos por desenvolvedores diretamente na linguagem de assembly apropriada. O aplicativo passaria esse código de linguagem de assembly legível por humanos para a biblioteca D3DX usando [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) e obteria uma representação binária do sombreador que, por sua vez, seria passado usando [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) ou [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader). Para obter mais detalhes, consulte o Software Development Kit (SDK).

A situação no Direct3D 9 é semelhante. Um aplicativo passa um sombreador HLSL para D3DX usando [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) e obtém de volta uma representação binária do sombreador compilado que, por sua vez, é passado para o Microsoft Direct3D usando [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) ou [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader). O tempo de execução não sabe nada sobre HLSL, apenas os modelos de sombreador de assembly binário. Isso é bom porque significa que o compilador HLSL pode ser atualizado independentemente do tempo de execução do Direct3D. Você também pode compilar sombreadores offline usando [FXC](/windows/desktop/direct3dtools/fxc).

Além do desenvolvimento do compilador HLSL, o Direct3D 9 também introduziu os modelos de sombreamento de nível de assembly para expor a funcionalidade da última geração de hardware de gráficos. Os desenvolvedores de aplicativos podem trabalhar no assembly para esses novos modelos (vs \_ 2 \_ 0, vs \_ 3 \_ 0, PS \_ 2 \_ 0, PS \_ 3 \_ 0), mas esperamos que a maioria dos desenvolvedores mude para o HLSL para o desenvolvimento de sombreador.

É claro que a capacidade de escrever um programa HLSL para expressar um determinado algoritmo de sombreamento não permite que ele seja executado automaticamente em um determinado hardware. Um aplicativo chama D3DX para compilar um sombreador no código de assembly binário com [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader). Uma das limitações com esse ponto de entrada é um parâmetro que define quais dos modelos de nível de assembly (ou destinos de compilação) o compilador HLSL deve usar para expressar o código final do sombreador. Se um aplicativo estiver fazendo a compilação do sombreador HLSL em tempo de execução (em oposição ao tempo de compilação ou offline), o aplicativo poderá examinar os recursos do dispositivo Direct3D e selecionar o destino de compilação para corresponder. Se o algoritmo expresso no sombreador HLSL for muito complexo para ser executado no destino de compilação selecionado, ocorrerá uma falha na compilação. Isso significa que, embora HLSL seja um grande benefício para o desenvolvimento de sombreador, ele não libera os desenvolvedores da realidade de enviar jogos para um público-alvo com dispositivos gráficos de diferentes recursos. Como desenvolvedor de jogos, você ainda precisa gerenciar uma abordagem em camadas para seus visuais; Isso significa escrever melhores sombreadores para placas gráficas mais compatíveis e escrever versões mais básicas para cartões mais antigos. No entanto, com HLSL bem escrito, essa carga pode ser facilitouda de forma significativa.

Em vez de Compilar sombreadores HLSL usando o D3DX na máquina do cliente no momento da carga do aplicativo ou no primeiro uso, muitos desenvolvedores optam por compilar seu sombreador de HLSL para código de assembly binário antes que eles sejam entregues. Isso mantém seu código-fonte HLSL longe dos olhos curiosos e também garante que todos os sombreadores que seus aplicativos serão executados terão passado pelo seu processo de controle de qualidade interno. Um utilitário conveniente para a compilação de sombreadores offline é o [FXC](/windows/desktop/direct3dtools/fxc). Essa ferramenta tem várias opções que você pode usar para compilar o código para o destino de compilação especificado. Estudar a saída desmontada pode ser muito educativo durante o desenvolvimento se você quiser otimizar seus sombreadores ou, geralmente, conhecer os recursos da máquina do sombreador virtual em um nível mais detalhado. Essas opções são resumidas abaixo:

## <a name="initializing-shader-constants"></a>Inicializando constantes do sombreador

As constantes do sombreador estão contidas na tabela de constantes. Isso pode ser acessado com a interface [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) . As variáveis de sombreador global podem ser inicializadas no código do sombreador. Eles são inicializados em tempo de execução chamando [**setpadrões**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults).

## <a name="binding-a-shader-parameter-to-a-particular-register"></a>Associando um parâmetro de sombreador a um registro específico

O compilador atribuirá automaticamente os registros a variáveis globais. O compilador atribuiria o ambiente para o registro de amostra S0, SparkleNoise para o registro de amostra S1 e k \_ s para o registro constante C0 (supondo que nenhuma outra amostra ou registro constante já foi atribuído) para as três seguintes variáveis globais:


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



Também é possível associar variáveis a um registro específico. Para forçar o compilador a atribuir a um registro específico, use a seguinte sintaxe:


```
register(RegisterName)
```



em que Registrname é o nome do registro específico. Os exemplos a seguir demonstram a sintaxe de atribuição de Registro específica, em que o ambiente de amostra será associado ao registro de amostra S1, SparkleNoise será associado ao registro de amostra S0 e k \_ s serão associados a C12 de registro constante:


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a>Renderizando um sombreador programável

Um sombreador é renderizado definindo o sombreador atual no dispositivo, inicializando as constantes do sombreador, informando ao dispositivo de onde os dados de entrada variados são provenientes e, finalmente, Renderizando os primitivos. Cada um deles pode ser feito chamando os seguintes métodos, respectivamente:

-   [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [**Setstreaming**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [**DrawPrimitive**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a>Depurando sombreadores

a extensão do DirectX para Microsoft Visual Studio .net fornece um depurador HLSL totalmente integrado dentro do ambiente de desenvolvimento integrado (IDE) do Visual Studio .net. para se preparar para a depuração de sombreador, você deve instalar as ferramentas certas em seu computador (consulte [depurando sombreadores no Visual Studio (Direct3D 9)](dx-graphics-hlsl-debug-visual-studio.md)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 