---
description: A página a seguir fornece um contorno básico das principais diferenças entre o Direct3D 9 e o Direct3D 10. A delineada abaixo fornece algumas informações para ajudar os desenvolvedores com a experiência do Direct3D 9 a explorar e se relacionar com o Direct3D 10.
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: Considerações do Direct3D 9 para Direct3D 10 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6c2dac7da24184bb5cc6a78f8e7d391c7d0f8b7000107915ba5a606188dcf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120006"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Considerações do Direct3D 9 para Direct3D 10 (Direct3D 10)

A página a seguir fornece um contorno básico das principais diferenças entre o Direct3D 9 e o Direct3D 10. A delineada abaixo fornece algumas informações para ajudar os desenvolvedores com a experiência do Direct3D 9 a explorar e se relacionar com o Direct3D 10.

Embora as informações neste tópico comparem o Direct3D 9 com o Direct3D 10, pois o Direct3D 11 se baseia nas melhorias feitas no Direct3D 10 e 10.1, você também precisa dessa informação para migrar do Direct3D 9 para o Direct3D 11. Para obter informações sobre como ir além do Direct3D 10 para o Direct3D 11, consulte [Migrando para o Direct3D 11](../direct3d11/d3d11-programming-guide-migrating.md).

-   [Visão geral das principais alterações estruturais no Direct3D 10](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [Remoção da função fixa](#removal-of-fixed-function)
    -   [Validação de tempo de criação de objeto de dispositivo](#device-object-creation-time-validation)
-   [Abstrações/separação do mecanismo](/windows)
    -   [Remoção direta de dependências do Direct3D 9](#direct-removal-of-direct3d-9-dependencies)
-   [Truques para resolver rapidamente problemas de build do aplicativo](#tricks-for-quickly-resolving-application-build-issues)
    -   [Substituindo tipos direct3D 9](#overriding-direct3d-9-types)
    -   [Resolvendo problemas de link](#resolving-link-issues)
    -   [Simulando CAPs de dispositivo](#simulating-device-caps)
-   [Condução da API do Direct3D 10](#driving-the-direct3d-10-api)
    -   [Criação de recursos](#resource-creation)
    -   [Exibições](#views)
    -   [Acesso a recursos estáticos versus dinâmicos](#static-versus-dynamic-resource-access)
    -   [Efeitos do Direct3D 10](#direct3d-10-effects)
    -   [HLSL sem efeitos](#hlsl-without-effects)
    -   [Compilação do sombreador](#shader-compilation)
    -   [Criação de recursos de sombreador](#creation-of-shader-resources)
    -   [Interface da camada de reflexão do sombreador](#shader-reflection-layer-interface)
    -   [Layouts do assembler de entrada – Sombreador de vértice/vinculação de fluxo de entrada](/windows)
    -   [Impacto da remoção de código inocupado do sombreador](#impact-of-shader-dead-code-removal)
    -   [Exemplo de estrutura de entrada do sombreador de vértice](#vertex-shader-input-structure-example)
    -   [Criação de objeto de estado](#state-object-creation)
-   [Portando texturas](#porting-textures)
    -   [Formatos de arquivo com suporte](#file-formats-supported)
    -   [Mapeamento de formatos de textura](#mapping-texture-formats)
-   [Sombreadores de portação](#porting-shaders)
    -   [Sombreadores do Direct3D 10 são autores em HLSL](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [Assinaturas e vinculação do sombreador](#shader-signatures-and-linkage)
    -   [Vinculações do Estágio do Sombreador HLSL](#hlsl-shader-stage-linkages)
    -   [Buffers constantes](#constant-buffers)
    -   [Planos de clipe de usuário em HLSL no nível de recurso 9 e superior](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Diferenças adicionais do Direct3D 10 a ser assistida](#additional-direct3d-10-differences-to-watch-for)
    -   [Inteiros como Entrada](#integers-as-input)
    -   [Cursores de mouse](#mouse-cursors)
    -   [Mapeando o Texels para pixels no Direct3D 10](#mapping-texels-to-pixels-in-direct3d-10)
    -   [Alterações de comportamento de contagem de referência](#reference-counting-behavior-changes)
    -   [Nível cooperativo de teste](#test-cooperative-level)
    -   [Stretchrect](#stretchrect)
-   [Diferenças adicionais do Direct3D 10.1](#additional-direct3d-101-differences)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>Visão geral das principais alterações estruturais no Direct3D 10

-   [Remoção da função fixa](#removal-of-fixed-function)
-   [Validação de tempo de criação de objeto de dispositivo](#device-object-creation-time-validation)

O processo de renderização usando o dispositivo Direct3D 10 é estruturalmente semelhante ao Direct3D 9.

-   Definir uma origem de fluxo de vértice
-   Definir layout de entrada no Direct3D 10 (definir declaração de fluxo de vértice no Direct3D 9)
-   Declarar topologia primitiva
-   Definir texturas
-   Definir objetos de estado
-   Definir sombreadores
-   Draw

A [**chamada Draw**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) une as operações; a ordenação de chamadas antes da chamada draw é arbitrária. As principais diferenças no design da API do Direct3D 10 são as seguinte:

-   Remoção da função fixa
-   Remoção de bits CAPS – o conjunto de recursos base do Direct3D 10 é garantido
-   Gerenciamento mais estrito de: acesso a recursos, estado do dispositivo, constantes de sombreador, vinculação de sombreador (entradas e saídas para sombreadores) entre estágios
-   As alterações de nome do ponto de entrada de API refletem o uso da memória de GPU virtual (Map() em vez de Lock()).
-   Uma camada de depuração pode ser adicionada ao dispositivo no momento da criação
-   A topologia primitiva agora é um estado explícito (separado da [**chamada Draw)**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw)
-   Constantes de sombreador explícitas agora são armazenadas em buffers constantes
-   A produção do sombreador é feita inteiramente em HLSL. O compilador HLSL agora reside na DLL primária do Direct3D 10.
-   Novo estágio programável – o sombreador de geometria
-   Remoção de BeginScene()/EndScene()
-   Funcionalidade 2D comum, foco e gerenciamento de adaptador implementada em um novo componente: DXGI

### <a name="removal-of-fixed-function"></a>Remoção da função fixa

Às vezes, é surpreendente que, mesmo em um mecanismo direct3D 9 que explora totalmente o pipeline programável, ainda haja várias áreas que dependem do pipeline de função fixa (FF). As áreas mais comuns geralmente estão relacionadas à renderização alinhada de espaço na tela para a interface do usuário. É por esse motivo que é provável que você precise criar um sombreador de emulação FF ou um conjunto de sombreadores que fornecem os comportamentos de substituição necessários.

Esta documentação contém um white paper que contém fontes de sombreador de substituição para os comportamentos de FF mais comuns (consulte Exemplo de [EMU de função fixa).](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) Algum comportamento de pixel de função fixa, incluindo teste alfa, foi movido para sombreadores.

### <a name="device-object-creation-time-validation"></a>Validação de tempo de criação de objeto de dispositivo

O pipeline do Direct3D 10 foi reprojetado desde o início em hardware e software com a principal intenção de reduzir a sobrecarga da CPU (em tempo de desenho). Para reduzir os custos, todos os tipos de dados do dispositivo foram atribuídos a um objeto com métodos de criação explícitos fornecidos pelo próprio dispositivo. Isso habilita a validação de dados estrita no momento da criação do objeto, em vez de durante a chamada draw, como geralmente acontece com o Direct3D 9.

## <a name="engine-abstractions--separation"></a>Abstrações/separação do mecanismo

Aplicativos, incluindo Jogos, que desejam dar suporte ao Direct3D 9 e direct3D 10 precisam ter as camadas de renderização abstraídos do restante da base de código. Há muitas maneiras de conseguir isso, mas a chave para todas elas é o design da camada de abstração para o dispositivo Direct3D de nível inferior. Todos os sistemas devem se comunicar com o hardware por meio da camada comum, que foi projetada para fornecer recursos de GPU e gerenciamento de tipos de baixo nível.

### <a name="direct-removal-of-direct3d-9-dependencies"></a>Remoção direta de dependências do Direct3D 9

Ao portar bases de código grandes e testadas anteriormente, é importante minimizar a quantidade de alterações de código para aquelas que são absolutamente necessárias para preservar os comportamentos testados anteriormente no código. As práticas recomendadas incluem a documentação clara em que os itens mudam usando comentários. Geralmente, é útil ter um padrão de comentário para esse trabalho que habilita a navegação rápida pela base de código.

Veja a seguir uma lista de exemplos de comentários padrão de bloco de linha única/início que podem ser usados para esse trabalho.



| Item                                                                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>Direct3D 10 REMOVIDO<br/>                     | Use isso em que linhas/blocos de código são removidos<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>O Direct3D 10 PRECISA DE ATUALIZAÇÃO<br/> | Ele ajuda a adicionar observações adicionais ao comentário NEED UPDATE que sugere qual API de trabalho/nova deve ser usada para visitas posteriores ao código para conversão de comportamento. O uso intenso de assert(**false**) também deve ser usado em que \\ \\ o Direct3D 10 NEEDS UPDATE ocorre para garantir que você não execute código errant sem saber<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 CHANGED<br/>                     | Áreas em que ocorreram alterações importantes devem ser mantidas para referência futura, mas comentadas<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>Direct3D 10 END<br/>                                     | Qualificador de bloco de código final<br/>                                                                                                                                                                                                                                                                                            |



 

Para várias linhas de origem, você também deve usar o estilo \* C//comments, mas adicionar os comentários de início/término relevantes \* em torno dessas áreas.

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>Truques para resolver rapidamente problemas de build do aplicativo

-   [Substituindo tipos direct3D 9](#overriding-direct3d-9-types)
-   [Resolvendo problemas de link](#resolving-link-issues)
-   [Simulando CAPs de dispositivo](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>Substituindo tipos direct3D 9

Pode ser útil inserir um arquivo de header de alto nível que contém definições de tipo/substituições para tipos base do Direct3D 9 que não têm mais suporte pelos headers do Direct3D 10. Isso ajudará você a minimizar a quantidade de alterações no código e nas interfaces em que há um mapeamento direto de um tipo Direct3D 9 para o tipo Direct3D 10 recém-definido. Essa abordagem também é útil para manter os comportamentos de código juntos em um arquivo de origem. Nesse caso, é uma boa ideia definir tipos de versão neutras/geralmente nomeados que descrevem constructos comuns usados para renderização e abrangem ainda as APIs direct3D 9 e Direct3D 10. Por exemplo:


```
#if defined(D3D9)
typedef IDirect3DIndexBuffer9   IDirect3DIndexBuffer;
typedef IDirect3DVertexBuffer9  IDirect3DVertexBuffer;
#else //D3D10
typedef ID3D10Buffer            IDirect3DIndexBuffer;
typedef ID3D10Buffer            IDirect3DVertexBuffer
#endif
```



Outros exemplos específicos do Direct3D 10 incluem:


```
typedef ID3D10TextureCube   IDirect3DCubeTexture;
typedef ID3D10Texture3D     IDirect3DVolumeTexture;
typedef D3D10_VIEWPORT      D3DVIEWPORT;
typedef ID3D10VertexShader  IDirect3DVertexShader;
typedef ID3D10PixelShader   IDirect3DPixelShader;
```



### <a name="resolving-link-issues"></a>Resolvendo problemas de link

É aconselhável desenvolver aplicativos Direct3D 10 e Windows Vista usando a versão mais recente do Microsoft Visual Studio. No entanto, é possível criar um aplicativo Windows Vista que depende do Direct3D 10 usando a versão anterior de 2003 do Visual Studio. O Direct3D 10 é um componente de plataforma do Windows Vista que tem dependências (assim como no SDK da plataforma Server 2003 SP1) na seguinte biblioteca: BufferOverflowU.lib é necessário para resolver quaisquer problemas de vinculador de verificação de segurança \_ de buffer.

### <a name="simulating-device-caps"></a>Simulando CAPs de dispositivo

Muitos aplicativos contêm áreas de código que dependem da disponibilidade de dados CAPS do dispositivo. Resolver isso substituindo a enumeração de dispositivo e forçando o CAPS do dispositivo a valores sensíveis. Planeje visitar as áreas em que há dependências no CAPS posteriormente para remoção completa do CAPS sempre que possível.

## <a name="driving-the-direct3d-10-api"></a>Condução da API do Direct3D 10

Esta seção se concentra nas alterações de comportamento causadas pela API do Direct3D 10.

-   [Criação de recursos](#resource-creation)
-   [Exibições](#views)
-   [Acesso a recursos estáticos versus dinâmicos](#static-versus-dynamic-resource-access)
-   [Efeitos do Direct3D 10](#direct3d-10-effects)
-   [HLSL sem efeitos](#hlsl-without-effects)
-   [Compilação do sombreador](#shader-compilation)
-   [Criação de recursos de sombreador](#creation-of-shader-resources)
-   [Interface da camada de reflexão do sombreador](#shader-reflection-layer-interface)
-   [Layouts do assembler de entrada – Sombreador de vértice/vinculação de fluxo de entrada](/windows)
-   [Impacto da remoção de código inocupado do sombreador](#impact-of-shader-dead-code-removal)
-   [Exemplo de estrutura de entrada do sombreador de vértice](#vertex-shader-input-structure-example)
-   [Criação de objeto de estado](#state-object-creation)

### <a name="resource-creation"></a>Criação de recursos

A API do Direct3D 10 criou recursos como tipos de buffer genéricos que têm sinalizadores de ligação específicos de acordo com o uso planejado. Esse ponto de design foi escolhido para facilitar o acesso quase onipresente de recursos no Pipeline para cenários como renderização em um buffer de vértice e, em seguida, desenhar instantaneamente os resultados sem interromper a CPU. O exemplo a seguir demonstra a alocação de buffers de vértice e buffer de índice em que você pode ver que a descrição do recurso difere apenas pelos sinalizadores de vinculação de recurso de GPU.

A API do Direct3D 10 forneceu métodos auxiliares de textura para criar explicitamente recursos de tipo de textura, mas como você pode imaginar, essas são realmente funções auxiliares.

-   CreateTexture2D()
-   CreateTextureCube()
-   CreateTexture3D()

Ao direcionar o Direct3D 10, é provável que você queira alocar mais itens durante o tempo de criação de recursos do que você está acostumado com o Direct3D 9. Isso se tornará mais aparente com a criação de buffers de destino de renderização e texturas em que você também precisa criar uma exibição para acessar o buffer e definir o recurso no dispositivo.

[Tutorial 1: Noções básicas do Direct3D 10](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> O Direct3D 10 e versões posteriores do Direct3D estendem o formato de arquivo DDS para dar suporte a novos formatos DXGI, matrizes de textura e matrizes de mapa de cubo. Para obter mais informações sobre a extensão de formato de arquivo DDS, consulte o Guia [de Programação para DDS](../direct3ddds/dx-graphics-dds-pguide.md).

 

### <a name="views"></a>Exibições

Uma exibição é uma interface especificamente digitada para dados armazenados em um buffer de pixel. Um recurso pode ter várias exibições alocadas ao mesmo tempo e esse recurso é realçado na amostra Renderização de Passagem Única para Cubemap contida neste SDK.

[Página Guia do Programador no Acesso a Recursos](d3d10-graphics-programming-guide-resources-access-views.md)

[Exemplo de CubeMap](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>Acesso a recursos estáticos versus dinâmicos

Para melhor desempenho, os aplicativos devem particionar o uso de dados em termos da natureza estática versus dinâmica dos dados. O Direct3D 10 foi projetado para aproveitar essa abordagem e, como tal, as regras de acesso para recursos foram significativamente reforçadas em relação ao Direct3D 9. Para recursos estáticos, o ideal é preencher o recurso com seus dados durante o tempo de criação. Se o mecanismo tiver sido projetado em torno do ponto de design Criar, Bloquear, Preencher, Desbloquear do Direct3D 9, você poderá adiar a população de Criar tempo usando um recurso de preparação e o método UpdateSubResource na interface de recurso.

### <a name="direct3d-10-effects"></a>Efeitos do Direct3D 10

O uso do sistema direct3D 10 Effects está fora do escopo deste artigo. O sistema foi escrito para aproveitar ao máximo os benefícios de arquitetura que o Direct3D 10 oferece. Consulte a [seção Efeitos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md) para obter mais detalhes sobre seu uso.

### <a name="hlsl-without-effects"></a>HLSL sem efeitos

O pipeline do Sombreador Direct3D 10 pode ser orientado sem o uso do sistema direct3D 10 Effects. Observe que, nessa instância, todos os buffers constantes, sombreador, amostrador e associação de textura devem ser gerenciados pelo próprio aplicativo. Confira o link de exemplo e as seções a seguir deste documento para obter mais detalhes:

[Exemplo de HLSL sem efeitos](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>Compilação do sombreador

O compilador HLSL do Direct3D 10 traz aprimoramentos para a definição de linguagem HLSL e, portanto, tem a capacidade de operar em dois modos. Para suporte completo de funções intrínsecas de estilo Direct3D 9 e semântica, a compilação deve ser invocada usando o sinalizador MODO DE COMPATIBILIDADE, que pode ser especificado por compilação.

A semântica da linguagem HLSL específica do modelo de sombreador 4.0 e as funções intrínsecas do Direct3D 10 podem ser encontradas [em HLSL.](../direct3dhlsl/dx-graphics-hlsl.md) As principais alterações na sintaxe do Direct3D 9 HLSL para aproveitar ao máximo estão na área de acesso à textura. A nova sintaxe é a única forma compatível com o compilador fora do modo de compatibilidade.

> [!Note]  
> As APIs do tipo de compilador Direct3D [**10 ( D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader) e [**D3D10CompileEffectFromMemory**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)) são fornecidas pelos runtimes Direct3D 10, 10.1 e 11 executados no Windows Vista e posterior. As APIs do tipo de compilador Direct3D 10 têm a mesma funcionalidade que o compilador HLSL enviado no SDK do DirectX (dezembro de 2006). Esse compilador HLSL não dá suporte aos perfis do Direct3D 10.1 \_ (versus 4 \_ 1, ps \_ 4 \_ 1, gs \_ 4 \_ 1, fx \_ \_ 4 1) e não tem várias otimizações e melhorias. Você pode obter um compilador HLSL que dá suporte aos perfis do Direct3D 10.1 da versão mais recente herdada do [SDK do DirectX.](/previous-versions/windows/apps/hh452744(v=win.10)) Para obter informações sobre o SDK do DirectX herdado, consulte [Onde está o SDK do DirectX?](../directx-sdk--august-2009-.md). Você pode obter o compilador de linha de comando Fxc.exe HLSL mais recente e as APIs [D3DCompiler](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) do SDK do Windows.

 

### <a name="creation-of-shader-resources"></a>Criação de recursos de sombreador

A criação de instâncias de sombreador compiladas fora do sistema Direct3D 10 Effects é feita de maneira muito semelhante ao Direct3D 9, no entanto, no Direct3D 10, é importante manter a assinatura de Entrada do Sombreador para uso posterior. A assinatura é retornada por padrão como parte do blob do sombreador, mas pode ser extraída para reduzir os requisitos de memória, se necessário. Para obter mais detalhes, [consulte Usando sombreadores no Direct3D 10](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

### <a name="shader-reflection-layer-interface"></a>Interface da camada de reflexão do sombreador

A camada de reflexão do sombreador é a interface pela qual as informações sobre os requisitos do sombreador podem ser obtidas. Isso é particularmente útil ao criar vinculações de Assembly de Entrada (veja abaixo) em que talvez seja necessário percorrer os requisitos de entrada do sombreador para garantir que você está fornecendo a estrutura de entrada correta para o sombreador. Você pode criar uma instância da interface da camada de reflexão ao mesmo tempo que criar uma instância de um sombreador compilado.

A camada de reflexão do sombreador substitui métodos D3DX9 que fornecem funcionalidade semelhante. Por [**exemplo, IsParameterUsed**](../direct3d9/id3dxeffect--isparameterused.md) é substituído pelo [**método GetDesc.**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc)

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>Layouts do assembler de entrada – Sombreador de vértice/vinculação de fluxo de entrada

O IA (Assembler de Entrada) substitui a Declaração de Fluxo de Vértice de estilo Direct3D 9 e sua estrutura de descrição é muito semelhante na forma. A principal diferença que a IA traz é que o objeto de layout ia criado deve mapear diretamente para um formato específico de assinatura de entrada do sombreador. O objeto de mapeamento criado para vincular o fluxo de entrada ao sombreador pode ser usado em qualquer número de sombreadores em que a assinatura de entrada do sombreador corresponde à do sombreador usado para criar o Layout de Entrada.

Para melhor conduzir o pipeline com dados estáticos, considere as permutações do formato de fluxo de entrada para possíveis assinaturas de entrada do sombreador e crie as instâncias de objeto de layout de IA o mais cedo possível e reutilize-as sempre que possível.

### <a name="impact-of-shader-dead-code-removal"></a>Impacto da remoção de código inocupado do sombreador

A seção a seguir detalha uma diferença significativa entre o Direct3D 9 e o Direct3D 10 que provavelmente exigirá tratamento cuidadoso no código do mecanismo. Sombreadores que contêm expressões condicionais geralmente têm determinados caminhos de código removidos como parte do processo de compilação. No Direct3D 9, dois tipos de entradas podem ser removidos (marcados para remoção) quando não são usadas: entradas de assinatura (como o exemplo abaixo) e entradas constantes. Se o final do buffer constante contiver entradas nãousadas, a declaração de tamanho no sombreador refletirá o tamanho do buffer constante sem as entradas nãoutiladas no final. Ambos os tipos de entradas permanecem em assinaturas ou buffers constantes Direct3D 10 com uma exceção especial no caso de entradas constantes nãoutiladas no final de um buffer constante. Isso pode ter um impacto no mecanismo ao lidar com sombreadores grandes e criar layouts de entrada. Elementos que são removidos por otimizações de código inoportunar no compilador ainda devem ser declarados na estrutura de entrada. O exemplo a seguir demonstra este:

### <a name="vertex-shader-input-structure-example"></a>Exemplo de estrutura de entrada do sombreador de vértice


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* A remoção de código morto do Direct3D 9 removeria a declaração no sombreador devido à remoção condicional de código inocupado


```
float4x4  g_WorldViewProjMtx;
static const bool g_bLightMapped = false; // define a compile time constant

VS_INPUT main(VS_INPUT i) 
{
    VS_INPUT o;
    o.pos = mul( i.pos, g_WorldViewProjMtx);
    o.uv1 = i.uv1;
    if ( g_bLightMapped )
    {
        o.uv2 = i.uv2;
    }
    return o;
}
```



Ou você pode tornar ainda mais óbvio que a constante é uma constante de tempo de compilação com a seguinte declaração:


```
#define LIGHT_MAPPED false
```



No exemplo acima, em Direct3D 9, o elemento uv2 seria removido devido a otimizações de código inove no compilador. Em Direct3D 10, o código inoportuário ainda será removido, mas o layout do assembler de entrada do sombreador requer a definição dos dados de entrada para existir. A camada de reflexão do sombreador fornece os meios para lidar com essa situação de maneira genérica, na qual você pode percorrer os requisitos de entrada do sombreador e garantir que forneça uma descrição completa do Fluxo de Entrada para o mapeamento de assinatura do sombreador.

Aqui está um exemplo de função para detectar a existência de um nome semântico/índice em uma assinatura de função:


```
// Returns true if the SemanticName / SemanticIndex is used in the input signature.
// pReflector is a previously acquired shader reflection interface.
bool IsSignatureElementExpected(ID3D10ShaderReflection *pReflector, const LPCSTR SemanticName, UINT SemanticIndex)
{
    D3D10_SHADER_DESC               shaderDesc;
    D3D10_SIGNATURE_PARAMETER_DESC  paramDesc;

    Assert(pReflector);
    Assert(SemanticName);

    pReflector->GetDesc(&shaderDesc);

    for (UINT k=0; k<shaderDesc.InputParameters; k++)
    {
        pReflector->GetInputParameterDesc( k, &paramDesc);
        if (wcscmp( SemanticName, paramDesc.SemanticName)==0 && paramDesc.SemanticIndex == SemanticIndex) 
            return true;
    }

    return false;
}
```



### <a name="state-object-creation"></a>Criação de objeto de estado

Ao portar o código do mecanismo, pode ajudar a usar inicialmente um conjunto padrão de objetos de estado e desabilitar todas as configurações de estado de renderização/estado de textura do dispositivo Direct3D 9. Isso causará artefatos de renderização, mas é a maneira mais rápida de deixar tudo em funcionamento. Posteriormente, você pode construir um sistema de gerenciamento de objetos de estado que pode usar uma chave composta para habilitar a reutilização máxima do número de objetos de estado que estão sendo usados.

## <a name="porting-textures"></a>Portando texturas

### <a name="file-formats-supported"></a>Formatos de arquivo com suporte

As funções **D3DXxxCreateXXX** e **D3DXxxSaveXXX** que criam ou salvam uma textura de ou em um arquivo gráfico (por exemplo, [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)) suportam um conjunto diferente de formatos de arquivo no Direct3D 10 do que no Direct3D 9:



| Formato de arquivo | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| .bmp        | x          | x           |
| .jpg        | x          | x           |
| .tga        | x          |             |
| .png        | x          | x           |
| .dds        | x          | x           |
| .ppm        | x          |             |
| .dib        | x          |             |
| .hdr        | x          |             |
| .pfm        | x          |             |
| .tiff       |            | x           |
| .gif        |            | x           |
| .tif        |            | x           |



 

Para obter detalhes, compare as enumerações [**\_ FILEFORMAT do**](../direct3d9/d3dximage-fileformat.md) Direct3D 9 D3DXIMAGE com as enumerações [**D3DX10 \_ IMAGE FILE \_ \_ FORMAT**](d3dx10-image-file-format.md) para Direct3D 10.

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8. Para processamento de arquivo de textura, recomendamos que você use [DirectXTex](https://github.com/Microsoft/DirectXTex).

 

### <a name="mapping-texture-formats"></a>Mapeamento de formatos de textura

A tabela a seguir mostra o mapeamento de formatos de textura do Direct3D 9 para o Direct3D 10. Qualquer conteúdo em formatos não disponíveis no DXGI precisará ser convertido por rotinas de utilitário.



| Formato do Direct3D 9                   | Formato Direct3D 10                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ UNKNOWN                     | FORMATO DXGI \_ \_ DESCONHECIDO                                                                                                                                                                                                                                |
| D3DFMT \_ R8G8B8                      | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A8R8G8B8                    | FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM & FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM \_ SRGB                                                                                                                                                                                 |
| D3DFMT \_ X8R8G8B8                    | FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM & FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM \_ SRGB                                                                                                                                                                                 |
| D3DFMT \_ R5G6B5                      | FORMATO DXGI \_ \_ B5G6R5 \_ UNORM;                                                                                                                                                                                                                         |
| D3DFMT \_ X1R5G5B5                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A1R5G5B5                    | FORMATO DXGI \_ \_ B5G5R5A1 \_ UNORM;                                                                                                                                                                                                                       |
| D3DFMT \_ A4R4G4B4                    | FORMATO DXGI \_ \_ B4G4R4A4 \_ UNORM;                                                                                                                                                                                                                       |
| D3DFMT \_ R3G3B2                      | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A8                          | FORMATO DXGI \_ \_ A8 \_ UNORM                                                                                                                                                                                                                              |
| D3DFMT \_ A8R3G3B2                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ X4R4G4B4                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A2B10G10R10                 | FORMATO DXGI \_ \_ R10G10B10A2                                                                                                                                                                                                                            |
| D3DFMT \_ A8B8G8R8                    | FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM & FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB                                                                                                                                                                                  |
| D3DFMT \_ X8B8G8R8                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ G16R16                      | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DFMT \_ A2R10G10B10                 | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A16B16G16R16                | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DFMT \_ A8P8                        | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ L8                          | DXGI \_ FORMAT \_ R8 UNORM Observação: use .r swizzle no sombreador para duplicar vermelho para outros componentes para obter \_ o comportamento D3D9.                                                                                                                                    |
| D3DFMT \_ A8L8                        | DXGI \_ FORMAT \_ R8G8 UNORM Observação: use swizzle .rrrg no sombreador para duplicar vermelho e mover verde para os componentes alfa para obter o comportamento \_ D3D9.                                                                                                            |
| D3DFMT \_ A4L4                        | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ V8U8                        | FORMATO DXGI \_ \_ R8G8 \_ SNORM                                                                                                                                                                                                                            |
| D3DFMT \_ L6V5U5                      | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ X8L8V8U8                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ Q8W8V8U8                    | FORMATO DXGI \_ \_ R8G8B8A8 \_ SNORM                                                                                                                                                                                                                        |
| D3DFMT \_ V16U16                      | FORMATO DXGI \_ \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DFMT \_ W11V11U10                   | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A2W10V10U10                 | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ UYVY                        | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | DXGI \_ FORMAT \_ G8R8 G8B8 UNORM (em DX9, os dados foram escalados para cima em \_ 255,0f, mas isso pode ser tratado no código do \_ sombreador).                                                                                                                                   |
| D3DFMT \_ YUY2                        | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | DXGI \_ FORMAT \_ R8G8 B8G8 UNORM (no DX9, os dados foram escalados para cima em \_ 255,0f, mas isso pode ser tratado no código do \_ sombreador).                                                                                                                                   |
| D3DFMT \_ DXT1                        | FORMATO DXGI \_ \_ BC1 \_ UNORM & FORMATO DXGI \_ \_ BC1 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT2                        | FORMATO DXGI \_ \_ BC1 \_ UNORM & FORMATO DXGI \_ \_ BC1 \_ UNORM \_ SRGB Observação: DXT1 e DXT2 são os mesmos de uma perspectiva de API/hardware... A única diferença era "alfa pré-ultado", que pode ser acompanhado por um aplicativo e não precisa de um formato separado. |
| D3DFMT \_ DXT3                        | FORMATO DXGI \_ \_ BC2 \_ UNORM & FORMATO DXGI \_ \_ BC2 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT4                        | FORMATO DXGI \_ \_ BC2 \_ UNORM & FORMATO DXGI \_ \_ BC2 \_ UNORM \_ SRGB Observação: DXT3 e DXT4 são os mesmos de uma perspectiva de API/hardware... A única diferença era "alfa pré-ultado", que pode ser acompanhado por um aplicativo e não precisa de um formato separado. |
| D3DFMT \_ DXT5                        | FORMATO DXGI \_ \_ BC3 \_ UNORM & FORMATO DXGI \_ \_ BC3 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ LOCKABLE | FORMATO DXGI \_ \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32                         | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D15S1                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D24S8                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X8                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X4S4                     | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D16                         | FORMATO DXGI \_ \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32F \_ LOCKABLE              | DXGI \_ FORMAT \_ D32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ D24FS8                      | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ S1D15                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ S8D24                       | FORMATO DXGI \_ \_ D24 \_ UNORM \_ S8 \_ UINT                                                                                                                                                                                                                   |
| D3DFMT \_ X8D24                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ X4S4D24                     | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ L16                         | DXGI \_ FORMAT \_ R16 UNORM Observação: use .r swizzle no sombreador para duplicar vermelho para outros componentes para obter o \_ comportamento D3D9.                                                                                                                                   |
| D3DFMT \_ INDEX16                     | FORMATO DXGI \_ \_ R16 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ INDEX32                     | FORMATO DXGI \_ \_ R32 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ Q16W16V16U16                | FORMATO DXGI \_ \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DFMT \_ MULTI2 \_ ARGB8               | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ R16F                        | DXGI \_ FORMAT \_ R16 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G16R16F                     | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A16B16G16R16F               | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ R32F                        | DXGI \_ FORMAT \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G32R32F                     | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A32B32G32R32F               | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ CxV8U8                      | Não disponível                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT1                 | DXGI \_ FORMAT \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DDECLTYPE \_ FLOAT2                 | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT3                 | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                                                                                                                                                                                                       |
| D3DDECLTYPE \_ FLOAT4                 | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | Não disponível                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ UBYTE4                 | DXGI FORMAT R8G8B8A8 UINT Observação: o sombreador obtém valores UINT, mas se floats integrais no estilo \_ \_ \_ Direct3D 9 são necessários (0,0f, 1,0f... 255.f), o UINT pode ser convertido apenas em float32 no sombreador.                                                               |
| D3DDECLTYPE \_ SHORT2                 | \_DXGI FORMAT R16G16 SINT Observação: o sombreador obtém valores SINT, mas se floats integrais no estilo \_ Direct3D 9 são necessários, o SINT pode ser convertido apenas em \_ float32 no sombreador.                                                                                       |
| D3DDECLTYPE \_ SHORT4                 | DXGI \_ FORMAT \_ R16G16B16A16 SINT Observação: o sombreador obtém valores SINT, mas se floats integrais do estilo Direct3D 9 são necessários, o SINT pode ser convertido apenas em \_ float32 no sombreador.                                                                                 |
| D3DDECLTYPE \_ UBYTE4N                | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ SHORT2N                | FORMATO DXGI \_ \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ SHORT4N                | FORMATO DXGI \_ \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ USHORT2N               | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ USHORT4N               | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ UDEC3                  | Não disponível                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ DEC3N                  | Não disponível                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | FORMATO DXGI \_ \_ BC4 \_ UNORM                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | FORMATO DXGI \_ \_ BC5 \_ UNORM                                                                                                                                                                                                                             |



 

O MeioDXGI 1.1, que está incluído no runtime do Direct3D 11, inclui formatos BGRA. No entanto, o suporte para esses formatos é opcional para dispositivos Direct3D 10 e 10.1 com drivers implementados no WDDM (Modelo de Driver de Exibição) do Windows Windows Vista (WDDM 1.0). Considere usar DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM. Como alternativa, você pode criar seu dispositivo com o SUPORTE A [**\_ \_ \_ BGRA \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) CREATE DEVICE para garantir que você só dá suporte a computadores com o runtime do Direct3D 11.0 e um driver WDDM 1.1 ou superior instalado.

Os formatos 5:6:5 e 5:5:5:1 definidos pelo 1.0 definiam 5:6:5:1, mas não tinham suporte no runtime direct3D 10.x ou Direct3D 11.0. Opcionalmente, esses formatos têm suporte com o DXGI 1.2 no runtime do DirectX 11.1, que é necessário para adaptadores de vídeo de nível de recurso 11.1 e WDDM 1.2 (modelo de driver de exibição começando com o Windows 8) e já tem suporte em níveis de recurso 10level9.

ÕesDXGI 1.2 introduziu o formato 4:4:4:4. Opcionalmente, esse formato tem suporte no runtime do DirectX 11.1, que é necessário para adaptadores de vídeo de nível de recurso 11.1 e drivers WDDM 1.2 e já tem suporte em níveis de recursos 10level9.

Para formatos descompactados, o DXGI limitou o suporte para padrões de formato de pixel arbitrário; todos os formatos descompactados devem ser do tipo RGBA. Isso pode exigir o swizzling dos formatos de pixel de ativos existentes, que recomendamos que você compute como uma passagem de pré-processo offline sempre que possível.

## <a name="porting-shaders"></a>Sombreadores de portação

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Sombreadores do Direct3D 10 são autores em HLSL

O Direct3D 10 limita o uso da linguagem de assembly somente para fins de depuração, portanto, todos os sombreadores de assembly escritos manualmente usados no Direct3D 9 precisarão ser convertidos em HLSL.

### <a name="shader-signatures-and-linkage"></a>Assinaturas e vinculação do sombreador

Discutimos os requisitos de vinculação do Assembly de Entrada às assinaturas de entrada do sombreador de vértice anteriormente neste documento (veja acima). Observe que o runtime do Direct3D 10 também melhorou os requisitos para o estágio de vinculação entre sombreadores. Essa alteração afetará as fontes do sombreador em que a associação entre estágios pode não ter sido totalmente descrita em Direct3D 9. Por exemplo:


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* VS desfeito – Vinculação PS – embora o sombreador de pixel possa não estar interessado na matriz completa, a vinculação deve especificar o float4x3 completo.

Observe que a semântica de vinculação entre estágios deve corresponder exatamente no entanto, as entradas dos estágios de destino podem ser um prefixo dos valores que estão sendo produzidos. No exemplo acima, o sombreador de pixel pode ter position e texcoord1 como as únicas entradas, mas não poderia ter a posição e o texcoord2 como as únicas entradas devido às restrições de ordenação.

### <a name="hlsl-shader-stage-linkages"></a>Vinculações do Estágio do Sombreador HLSL

A vinculação entre sombreadores pode ocorrer em qualquer um dos seguintes pontos no pipeline:

-   Assembler de entrada para sombreador de vértice
-   Sombreador de vértice para sombreador de pixel
-   Sombreador de vértice para sombreador geometry
-   Sombreador de vértice para saída de fluxo
-   Sombreador de geometria para sombreador de pixel
-   Sombreador de geometria para transmitir

### <a name="constant-buffers"></a>Buffers constantes

Para facilitar a portação do conteúdo do Direct3D 9, uma abordagem inicial para o gerenciamento constante fora do sistema effects pode envolver a criação de um único buffer constante que contém todas as constantes necessárias. É importante para o desempenho ordenar constantes em buffers pela frequência esperada de atualização. Essa organização reduzirá a quantidade de conjuntos de constantes redundantes para um mínimo.

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Planos de clipe de usuário em HLSL no nível de recurso 9 e superior

A partir do Windows 8, você pode usar o atributo de função [](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md) **clipplanes** em uma declaração de função HLSL em vez de [SV \_ ClipDistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) para fazer com que o sombreador funcione no nível [do](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) recurso 9 x, bem como no nível de \_ recurso 10 e superior. Para obter mais informações, consulte [Planos de clipe de usuário no hardware de nível de recurso 9.](../direct3dhlsl/user-clip-planes-on-10level9.md)

## <a name="additional-direct3d-10-differences-to-watch-for"></a>Diferenças adicionais do Direct3D 10 a ser assistida

### <a name="integers-as-input"></a>Inteiros como Entrada

No Direct3D 9, não havia suporte de hardware real para tipos de dados inteiros, no entanto, o hardware direct3D 10 dá suporte a tipos inteiros explícitos. Se você tiver dados de ponto flutuante no buffer de vértice, deverá ter uma entrada float. Caso contrário, um tipo inteiro será a representação de padrão de bit do valor de ponto flutuante. Um tipo inteiro não é permitido para uma entrada de sombreador de pixel, a menos que o valor seja marcado para nenhuma interpolação (consulte [Modificadores de interpolação](../direct3dhlsl/dx-graphics-hlsl-struct.md)).

### <a name="mouse-cursors"></a>Cursores de mouse

Nas versões anteriores do Windows, as rotinas de cursor de mouse GDI padrão não funcionaam corretamente em todos os dispositivos exclusivos de tela inteira. As APIs [**SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties), [**ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)e [**SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) foram adicionadas para lidar com esses casos. Como Windows versão do Vista da GDI compreende totalmente as superfícies [DXGI,](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md) não há necessidade dessa API especializada de cursor de mouse, portanto, não há nenhum equivalente ao Direct3D 10. Em vez disso, os aplicativos Direct3D 10 devem usar as [rotinas de cursor](../menurc/cursors.md) de mouse GDI padrão para cursores de mouse.

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>Mapeando o Texels para pixels no Direct3D 10

No Direct3D 9, os centros de texel e os centros de pixel tinham uma distância de meia unidade (consulte Mapeando [diretamente os texels para pixels (Direct3D 9)](../direct3d9/directly-mapping-texels-to-pixels.md)). No Direct3D 10, os centros de texel já estão em meia unidade, portanto, não há necessidade de deslocar as coordenadas de vértice.

A renderização de quads de tela inteira é mais direta com o Direct3D 10. Os quads de tela inteira devem ser definidos no clipspace (-1,1) e simplesmente passados pelo sombreador de vértice sem alterações. Dessa forma, não há necessidade de recarregar o buffer de vértice toda vez que a resolução da tela muda e não há nenhum trabalho extra no sombreador de pixel para manipular as coordenadas de textura.

### <a name="reference-counting-behavior-changes"></a>Alterações de comportamento de contagem de referência

Ao contrário das versões anteriores do Direct3D, as várias funções Set não conterão uma referência aos objetos de dispositivos. Isso significa que o aplicativo deve garantir que ele mantém uma referência no objeto desde que ele gostaria que esse objeto fosse vinculado ao pipeline. Quando a contagem de referência do objeto cair para zero, o objeto será desaconsudido do pipeline à medida que ele for destruído. Esse estilo de manter referência também é conhecido como retém de referência fraca, portanto, cada local de vinculação no objeto Dispositivo contém uma referência fraca para a interface/objeto. A menos que explicitamente mencionado de outra forma, esse comportamento deve ser presumido para todos os métodos Set. Sempre que a destruição de um objeto faz com que um ponto de vinculação seja definido como **NULL** out, a Camada de Depuração emitirá um aviso. Observe que as chamadas para os métodos Get do dispositivo, como [**OMGetRenderTargets,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) aumentarão a contagem de referência de objetos que estão sendo retornados.

### <a name="test-cooperative-level"></a>Nível cooperativo de teste

A funcionalidade do [**TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) da API do Direct3D 9 é análoga à configuração do [DXGI \_ PRESENT \_ TEST](../direct3ddxgi/dxgi-present.md) ao chamar [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present).

### <a name="stretchrect"></a>Stretchrect

Uma função semelhante ao método [**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) do Direct3D 9 não está disponível no Direct3D 10 e 10.1. Para copiar superfícies de recurso, use [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Para operações de reizing, renderizar em uma textura usando a filtragem de textura. Para converter superfícies MSAA em superfícies não MSAA, use [**ID3D10Device::ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource).

## <a name="additional-direct3d-101-differences"></a>Diferenças adicionais do Direct3D 10.1

Windows O Vista com Service Pack 1 (SP1) incluiu uma atualização secundária para Direct3D 10 e Direct3D 10.1, que expôs os seguintes recursos de hardware adicionais:

-   Sombreadores de MSAA por exemplo
-   Read-back de profundidade da MSAA
-   Modos de mesclagem independentes por destino de renderização
-   Matrizes de mapa de cubo
-   Renderizar para formatos compactados em bloco (BC)

A atualização do Direct3D 10.1 adicionou suporte para as novas interfaces a seguir, que são derivadas de interfaces existentes:

-   [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)
-   [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)
-   [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1)

A atualização do Direct3D 10,1 também incluiu as seguintes estruturas adicionais:

-   [**D3D10 \_ render \_ \_ DESC1 Blend de destino \_**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)
-   [**D3D10 \_ Blend \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)
-   [**\_DESC1 da \_ exibição de recursos do SOMBREAdor d3d10 \_ \_**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)

A API do Direct3D 10,1 inclui um novo conceito chamado nível de recurso. Esse conceito significa que você pode usar a API do Direct3D 10,1 para conduzir o Direct3D 10,0 ([**d3d10 de \_ recurso de \_ nível \_ 10 \_ 0**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) ou o hardware do Direct3D 10,1 ([**nível de recurso do d3d10 \_ \_ \_ 10 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)). Como a API do Direct3D 10,1 é derivada das interfaces do Direct3D 10, os aplicativos podem criar um dispositivo Direct3D 10,1 e, em seguida, usá-lo como um dispositivo do Direct3D 10,0, exceto onde novos recursos específicos do 10,1 são necessários (desde que o nível de recurso do **\_ \_ nível \_ 10 \_ 1 do recurso d3d10** esteja presente e ofereça suporte a esses recursos).

> [!Note]  
> Os dispositivos Direct3D 10,1 podem usar os perfis de 10,0 HLSL Shader existentes (vs \_ 4 \_ 0, PS \_ 4 \_ 0, GS \_ 4 \_ 0) e os novos perfis 10,1 (vs \_ 4 \_ 1, PS \_ 4 \_ 1, GS \_ 4 \_ 1) com instruções e recursos adicionais do HLSL.

 

o Windows 7 continha uma pequena atualização para a API do direct3d 10,1 que está incluída no tempo de execução do direct3d 11. Esta atualização adiciona suporte para os seguintes níveis de recurso:

-   [**Nível de recurso do D3D10 \_ \_ \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**Nível de recurso do D3D10 \_ \_ \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**Nível de recurso do D3D10 \_ \_ \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

Windows 7 também adicionou suporte ao Direct3D 10,1 para [Windows plataforma de rasterização avançada (WARP)](../direct3darticles/directx-warp.md). Você pode especificar um driver de detorção usando o [**\_ tipo de driver d3d10 \_ \_ Warp**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

Para obter mais informações sobre o Direct3D 10,1, consulte [recursos do direct3d 10,1](d3d10-graphics-programming-guide-10-1.md) e a enumeração do [**\_ recurso d3d10 \_ LEVEL1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
