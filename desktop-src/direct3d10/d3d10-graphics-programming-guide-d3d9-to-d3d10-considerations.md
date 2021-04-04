---
description: A página a seguir fornece uma descrição básica das principais diferenças entre o Direct3D 9 e o Direct3D 10. A estrutura de tópicos a seguir fornece uma visão geral para ajudar os desenvolvedores com a experiência do Direct3D 9 a explorar e relacionar-se com o Direct3D 10.
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: Considerações do Direct3D 9 para o Direct3D 10 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467ceefe7784a9b408bb36c8bed13217cb6de7c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646280"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Considerações do Direct3D 9 para o Direct3D 10 (Direct3D 10)

A página a seguir fornece uma descrição básica das principais diferenças entre o Direct3D 9 e o Direct3D 10. A estrutura de tópicos a seguir fornece uma visão geral para ajudar os desenvolvedores com a experiência do Direct3D 9 a explorar e relacionar-se com o Direct3D 10.

Embora as informações neste tópico comparem o Direct3D 9 com o Direct3D 10, porque o Direct3D 11 se baseia nos aprimoramentos feitos no Direct3D 10 e no 10,1, você também precisa dessas informações para migrar do Direct3D 9 para o Direct3D 11. Para obter informações sobre como se mover além do Direct3D 10 para o Direct3D 11, consulte [migrando para o Direct3D 11](../direct3d11/d3d11-programming-guide-migrating.md).

-   [Visão geral das principais alterações estruturais no Direct3D 10](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [Remoção da função fixa](#removal-of-fixed-function)
    -   [Validação do tempo de criação do objeto do dispositivo](#device-object-creation-time-validation)
-   [Abstrações/separação do mecanismo](/windows)
    -   [Remoção direta de dependências do Direct3D 9](#direct-removal-of-direct3d-9-dependencies)
-   [Truques para resolver rapidamente problemas de compilação de aplicativos](#tricks-for-quickly-resolving-application-build-issues)
    -   [Substituindo tipos de Direct3D 9](#overriding-direct3d-9-types)
    -   [Resolvendo problemas de link](#resolving-link-issues)
    -   [Simulando CAPs de dispositivo](#simulating-device-caps)
-   [Conduzindo a API do Direct3D 10](#driving-the-direct3d-10-api)
    -   [Criação de recursos](#resource-creation)
    -   [Exibições](#views)
    -   [Acesso a recursos estáticos versus dinâmicos](#static-versus-dynamic-resource-access)
    -   [Efeitos do Direct3D 10](#direct3d-10-effects)
    -   [HLSL sem efeitos](#hlsl-without-effects)
    -   [Compilação de sombreador](#shader-compilation)
    -   [Criação de recursos de sombreador](#creation-of-shader-resources)
    -   [Interface da camada de reflexo do sombreador](#shader-reflection-layer-interface)
    -   [Layouts do assembler de entrada-sombreador de vértice/vínculo de fluxo de entrada](/windows)
    -   [Impacto da remoção do código morto do sombreador](#impact-of-shader-dead-code-removal)
    -   [Exemplo de estrutura de entrada do sombreador de vértice](#vertex-shader-input-structure-example)
    -   [Criação de objeto de estado](#state-object-creation)
-   [Texturas portadoras](#porting-textures)
    -   [Formatos de arquivo com suporte](#file-formats-supported)
    -   [Mapeando formatos de textura](#mapping-texture-formats)
-   [Portando sombreadores](#porting-shaders)
    -   [Os sombreadores do Direct3D 10 são criados no HLSL](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [Assinaturas e vinculação de sombreador](#shader-signatures-and-linkage)
    -   [Ligações de estágio do sombreador HLSL](#hlsl-shader-stage-linkages)
    -   [Buffers de constantes](#constant-buffers)
    -   [Planos de corte do usuário no HLSL no nível de recurso 9 e superior](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Diferenças adicionais do Direct3D 10 a serem observadas](#additional-direct3d-10-differences-to-watch-for)
    -   [Inteiros como entrada](#integers-as-input)
    -   [Cursores do mouse](#mouse-cursors)
    -   [Mapeando texels para pixels no Direct3D 10](#mapping-texels-to-pixels-in-direct3d-10)
    -   [Alterações de comportamento de contagem de referência](#reference-counting-behavior-changes)
    -   [Testar nível de cooperação](#test-cooperative-level)
    -   [StretchRect](#stretchrect)
-   [Diferenças adicionais do Direct3D 10,1](#additional-direct3d-101-differences)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>Visão geral das principais alterações estruturais no Direct3D 10

-   [Remoção da função fixa](#removal-of-fixed-function)
-   [Validação do tempo de criação do objeto do dispositivo](#device-object-creation-time-validation)

O processo de renderização usando o dispositivo Direct3D 10 é estruturalmente semelhante ao Direct3D 9.

-   Definir uma origem de fluxo de vértice
-   Definir layout de entrada no Direct3D 10 (definir declaração de fluxo de vértice no Direct3D 9)
-   Declarar topologia primitiva
-   Definir texturas
-   Definir objetos de estado
-   Definir sombreadores
-   Draw

A chamada [**draw**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) une as operações; a ordenação de chamadas antes da chamada de desenho é arbitrária. As principais diferenças no design de API do Direct3D 10 são as seguintes:

-   Remoção da função fixa
-   Remoção de bits de CAPS-o conjunto de recursos base do Direct3D 10 é garantido
-   Gerenciamento estrito de: acesso a recursos, estado do dispositivo, constantes do sombreador, vínculo do sombreador (entradas e saídas para sombreadores) entre os estágios
-   As alterações de nome do ponto de entrada da API refletem o uso da memória de GPU virtual (MAP () em vez de Lock ()).
-   Uma camada de depuração pode ser adicionada ao dispositivo no momento da criação
-   A topologia primitiva agora é um estado explícito (separado da chamada de [**desenho**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) )
-   As constantes do sombreador explícito agora são armazenadas em buffers constantes
-   A criação de sombreador é feita inteiramente no HLSL. O compilador HLSL agora reside na DLL principal do Direct3D 10.
-   Nova fase programável – o sombreador Geometry
-   Remoção de BeginScene ()/EndScene ()
-   Funcionalidade comum de gerenciamento de adaptador e 2D implementada em um novo componente: DXGI

### <a name="removal-of-fixed-function"></a>Remoção da função fixa

Às vezes, é surpreendente que, mesmo em um mecanismo do Direct3D 9 que explora totalmente o pipeline programável, permaneça uma série de áreas que dependem do pipeline de função fixa (FF). As áreas mais comuns geralmente estão relacionadas à renderização alinhada pelo espaço de tela para a interface do usuário. É por esse motivo que você provavelmente precisará criar um sombreador de emulação de FF ou um conjunto de sombreadores que forneçam os comportamentos de substituição necessários.

Esta documentação contém uma white paper que contém fontes de sombreador de substituição para os comportamentos de FF mais comuns (consulte a [função fixa de exemplo de Emu](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx)). Um comportamento de pixel de função fixa, incluindo o teste alfa, foi movido para os sombreadores.

### <a name="device-object-creation-time-validation"></a>Validação do tempo de criação do objeto do dispositivo

O pipeline do Direct3D 10 foi reprojetado desde o início em hardware e software com uma intenção primária para reduzir a sobrecarga da CPU (no momento do desenho). Para reduzir os custos, todos os tipos de dados do dispositivo foram atribuídos a um objeto com métodos de criação explícitos fornecidos pelo próprio dispositivo. Isso permite a validação de dados estrita no momento da criação do objeto em vez de durante a chamada de desenho, como geralmente faz com o Direct3D 9.

## <a name="engine-abstractions--separation"></a>Abstrações/separação do mecanismo

Os aplicativos, incluindo jogos, que desejam dar suporte ao Direct3D 9 e ao Direct3D 10 precisam ter as camadas de renderização resumidas do restante da base de código. Há várias maneiras de conseguir isso, mas a chave para todos eles é o design da camada de abstração para o dispositivo Direct3D de nível inferior. Todos os sistemas devem se comunicar com o hardware por meio da camada comum, que foi projetada para fornecer recursos de GPU e gerenciamento de tipo de baixo nível.

### <a name="direct-removal-of-direct3d-9-dependencies"></a>Remoção direta de dependências do Direct3D 9

Ao portar bases de código grandes, testadas anteriormente, é importante minimizar a quantidade de alterações de código para aquelas que são absolutamente necessárias para preservar os comportamentos testados anteriormente no código. As práticas recomendadas incluem a documentação clara de onde os itens mudam usando comentários. Geralmente, é útil ter um comentário padrão para esse trabalho, o que permite a navegação rápida por meio da base de código.

Veja a seguir um exemplo de lista de comentários de linha única/início de bloco padrão que podem ser usados para esse trabalho.



| Item                                                                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>Direct3D 10 removido<br/>                     | Use este local onde as linhas/blocos de código são removidos<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>O Direct3D 10 precisa de atualização<br/> | Ele ajuda a adicionar mais observações ao comentário de atualização necessário, que sugere qual trabalho/nova API deve ser usada para visitas posteriores ao código para conversão de comportamento. O uso pesado de Assert (**false**) também deve ser usado em que o \\ \\ Direct3D 10 precisa de atualização para garantir que você não execute o código errônea<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 alterado<br/>                     | As áreas em que as alterações principais ocorreram devem ser mantidas para referência futura, mas comentadas<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>FIM do Direct3D 10<br/>                                     | Qualificador de bloco de código end<br/>                                                                                                                                                                                                                                                                                            |



 

Para várias linhas de origem, você deve usar o estilo C/ \* \* /comentários também, mas adicionar os comentários de início/término relevantes em relação a essas áreas.

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>Truques para resolver rapidamente problemas de compilação de aplicativos

-   [Substituindo tipos de Direct3D 9](#overriding-direct3d-9-types)
-   [Resolvendo problemas de link](#resolving-link-issues)
-   [Simulando CAPs de dispositivo](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>Substituindo tipos de Direct3D 9

Pode ser útil inserir um arquivo de cabeçalho de alto nível contendo definições/substituições de tipos de base do Direct3D 9 que não têm mais suporte nos cabeçalhos do Direct3D 10. Isso o ajudará a minimizar a quantidade de alterações no código e nas interfaces em que há um mapeamento direto de um tipo Direct3D 9 para o tipo Direct3D 10 definido recentemente. Essa abordagem também é útil para manter comportamentos de código juntos em um arquivo de origem. Nesse caso, é uma boa ideia definir os tipos de versão neutro/geralmente nomeados que descrevem construções comuns usadas para renderização, mas que abrangem as APIs do Direct3D 9 e do Direct3D 10. Por exemplo:


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

É aconselhável desenvolver aplicativos do Direct3D 10 e do Windows Vista usando a versão mais recente do Microsoft Visual Studio. No entanto, é possível criar um aplicativo do Windows Vista que dependa do Direct3D 10 usando a versão 2003 anterior do Visual Studio. O Direct3D 10 é um componente de plataforma do Windows Vista que tem dependências (como com o SDK da plataforma do Server 2003 SP1) na seguinte biblioteca: BufferOverflowU. lib é necessário para resolver quaisquer \_ problemas do vinculador da verificação de segurança do buffer.

### <a name="simulating-device-caps"></a>Simulando CAPs de dispositivo

Muitos aplicativos contêm áreas de código que dependem dos dados de CAPS do dispositivo estarem disponíveis. Contorne isso substituindo a enumeração do dispositivo e forçando os limites do dispositivo a valores razoáveis. Planeje visitar novamente as áreas em que há dependências em CAPS mais tarde para remoção completa de CAPS sempre que possível.

## <a name="driving-the-direct3d-10-api"></a>Conduzindo a API do Direct3D 10

Esta seção se concentra nas alterações de comportamento causadas pela API do Direct3D 10.

-   [Criação de recursos](#resource-creation)
-   [Exibições](#views)
-   [Acesso a recursos estáticos versus dinâmicos](#static-versus-dynamic-resource-access)
-   [Efeitos do Direct3D 10](#direct3d-10-effects)
-   [HLSL sem efeitos](#hlsl-without-effects)
-   [Compilação de sombreador](#shader-compilation)
-   [Criação de recursos de sombreador](#creation-of-shader-resources)
-   [Interface da camada de reflexo do sombreador](#shader-reflection-layer-interface)
-   [Layouts do assembler de entrada-sombreador de vértice/vínculo de fluxo de entrada](/windows)
-   [Impacto da remoção do código morto do sombreador](#impact-of-shader-dead-code-removal)
-   [Exemplo de estrutura de entrada do sombreador de vértice](#vertex-shader-input-structure-example)
-   [Criação de objeto de estado](#state-object-creation)

### <a name="resource-creation"></a>Criação de recursos

A API do Direct3D 10 projetou recursos como tipos de buffer genéricos que têm sinalizadores de ligação específicos de acordo com o uso planejado. Esse ponto de design foi escolhido para facilitar o acesso quase onipresente de recursos no pipeline para cenários como renderização em um buffer de vértice e, em seguida, desenhar instantaneamente os resultados sem interromper a CPU. O exemplo a seguir demonstra a alocação de buffers de vértice e o buffer de índice em que você pode ver que a descrição do recurso difere apenas pelos sinalizadores de ligação de recursos de GPU.

A API do Direct3D 10 forneceu métodos auxiliares de textura para criar explicitamente recursos de tipo de textura, mas como você pode imaginar, essas são funções realmente auxiliares.

-   CreateTexture2D()
-   CreateTextureCube()
-   CreateTexture3D()

Ao direcionar o Direct3D 10, é provável que você queira alocar mais itens durante o tempo de criação do recurso do que você está acostumado com o Direct3D 9. Isso ficará mais aparente com a criação de buffers de destino de renderização e texturas em que você também precisa criar uma exibição para acessar o buffer e definir o recurso no dispositivo.

[Tutorial 1: Noções básicas do Direct3D 10](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> O Direct3D 10 e versões posteriores do Direct3D estendem o formato de arquivo DDS para dar suporte a novos formatos de DXGI, matrizes de textura e matrizes de mapa de cubo. Para obter mais informações sobre a extensão de formato de arquivo DDS, consulte o [Guia de programação para DDS](../direct3ddds/dx-graphics-dds-pguide.md).

 

### <a name="views"></a>Exibições

Uma exibição é uma interface especificamente digitada para os dados armazenados em um buffer de pixel. Um recurso pode ter várias exibições alocadas a ele de uma vez e esse recurso é realçado na amostra de passagem única para cubemap contida neste SDK.

[Página guia de programadores sobre acesso a recursos](d3d10-graphics-programming-guide-resources-access-views.md)

[Exemplo de CubeMap](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>Acesso a recursos estáticos versus dinâmicos

Para obter um melhor desempenho, os aplicativos devem particionar seu uso de dados em termos da natureza estática versus dinâmica dos dados. O Direct3D 10 foi projetado para aproveitar essa abordagem e, como tal, as regras de acesso para os recursos foram significativamente reforçadas no Direct3D 9. Para recursos estáticos, o ideal é que você preencha o recurso com seus dados durante o tempo de criação. Se o mecanismo tiver sido projetado em relação ao ponto de design criar, bloquear, preencher e desbloquear do Direct3D 9, você poderá adiar a população do tempo de criação usando um recurso de preparo e o método UpdateSubResource na interface de recurso.

### <a name="direct3d-10-effects"></a>Efeitos do Direct3D 10

O uso do sistema de efeitos do Direct3D 10 está fora do escopo deste artigo. O sistema foi escrito para aproveitar ao máximo os benefícios arquitetônicos que o Direct3D 10 oferece. Consulte a seção [Effects (Direct3D 10)](d3d10-graphics-programming-guide-effects.md) para obter mais detalhes sobre seu uso.

### <a name="hlsl-without-effects"></a>HLSL sem efeitos

O pipeline do sombreador do Direct3D 10 pode ser orientado sem o uso do sistema de efeitos do Direct3D 10. Observe que, nessa instância, todas as associações de buffer constante, sombreador, amostra e textura devem ser gerenciadas pelo próprio aplicativo. Consulte o link de exemplo e as seguintes seções deste documento para obter mais detalhes:

[Exemplo de HLSL sem efeitos](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>Compilação de sombreador

O compilador Direct3D 10 HLSL traz aprimoramentos para a definição de linguagem HLSL e, portanto, tem a capacidade de operar em 2 modos. Para obter suporte completo de semântica e funções intrínsecas do estilo Direct3D 9, a compilação deve ser chamada usando o sinalizador modo de compatibilidade que pode ser especificado por compilação.

A semântica de linguagem HLSL específica do sombreador 4,0 e as funções intrínsecas para o Direct3D 10 podem ser encontradas em [HLSL](../direct3dhlsl/dx-graphics-hlsl.md). Alterações importantes na sintaxe do Direct3D 9 HLSL para obter o maior aviso de estão na área de acesso de textura. A nova sintaxe é o único Formulário suportado pelo compilador fora do modo de compatibilidade.

> [!Note]  
> As APIs do tipo de compilador do Direct3D 10 ([**D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader) e [**D3D10CompileEffectFromMemory**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)) são fornecidas pelos tempos de execução do Direct3D 10, 10,1 e 11 que são executados no Windows Vista e versões posteriores. As APIs do tipo de compilador do Direct3D 10 têm a mesma funcionalidade que o compilador do HLSL enviado no SDK do DirectX (dezembro de 2006). Este compilador do HLSL não dá suporte aos perfis do Direct3D 10,1 (vs \_ 4 \_ 1, PS \_ 4 \_ 1, GS \_ 4 \_ 1, FX \_ 4 \_ 1) e não tem um número de otimizações e aprimoramentos. Você pode obter um compilador HLSL que dá suporte aos perfis do Direct3D 10,1 da versão mais recente do [SDK do DirectX](/previous-versions/windows/apps/hh452744(v=win.10))herdado. Para obter informações sobre o SDK do DirectX herdado, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md). Você pode obter o mais recente HLSL Fxc.exe compilador de linha de comando e APIs [D3DCompiler](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) da SDK do Windows.

 

### <a name="creation-of-shader-resources"></a>Criação de recursos de sombreador

A criação de instâncias de sombreador compiladas fora do sistema de efeitos do Direct3D 10 é feita de maneira muito semelhante ao Direct3D 9 no entanto, no Direct3D 10, é importante manter a assinatura de entrada do sombreador para uso posterior. A assinatura é retornada por padrão como parte do blob do sombreador, mas pode ser extraída para reduzir os requisitos de memória, se necessário. Para obter mais detalhes, consulte [usando sombreadores no Direct3D 10](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

### <a name="shader-reflection-layer-interface"></a>Interface da camada de reflexo do sombreador

A camada de reflexo do sombreador é a interface pela qual as informações sobre os requisitos do sombreador podem ser obtidas. Isso é particularmente útil ao criar ligações de assembly de entrada (veja abaixo), em que talvez seja necessário percorrer os requisitos de entrada do sombreador para garantir que você esteja fornecendo a estrutura de entrada correta para o sombreador. Você pode criar uma instância da interface da camada de reflexão ao mesmo tempo que cria uma instância de um sombreador compilado.

A camada de reflexo do sombreador substitui os métodos D3DX9 que fornecem funcionalidade semelhante. Por exemplo, [**IsParameterUsed**](../direct3d9/id3dxeffect--isparameterused.md) é substituído pelo método [**GetDesc**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc) .

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>Layouts do assembler de entrada-sombreador de vértice/vínculo de fluxo de entrada

O Assembler de entrada (IA) substitui a declaração de fluxo de vértice do estilo Direct3D 9 e sua estrutura de descrição é muito semelhante no formato. A principal diferença que o IA traz é que o objeto de layout IA criado deve ser mapeado diretamente para um formato específico de assinatura de entrada de sombreador. O objeto de mapeamento criado para vincular o fluxo de entrada ao sombreador pode ser usado em qualquer número de sombreadores em que a assinatura de entrada do sombreador corresponda à do sombreador usado para criar o layout de entrada.

Para impulsionar melhor o pipeline com dados estáticos, você deve considerar as permutas do formato de fluxo de entrada para possíveis assinaturas de entrada de sombreador e criar as instâncias de objeto de layout IA o mais cedo possível e reutilizá-las sempre que possível.

### <a name="impact-of-shader-dead-code-removal"></a>Impacto da remoção do código morto do sombreador

A seção a seguir detalha uma diferença significativa entre o Direct3D 9 e o Direct3D 10, que provavelmente exigirá tratamento cuidadoso no código do mecanismo. Os sombreadores que contêm expressões condicionais geralmente têm determinados caminhos de código removidos como parte do processo de compilação. No Direct3D 9, dois tipos de entradas podem ser removidos (marcados para remoção) quando não utilizados: entradas de assinatura (como o exemplo abaixo) e entradas de constante. Se o final do buffer constante contiver entradas não utilizadas, a declaração de tamanho no sombreador refletirá o tamanho do buffer constante sem as entradas não utilizadas no final. Esses dois tipos de entradas permanecem em assinaturas ou em buffers de constantes Direct3D 10 com uma exceção especial no caso de entradas constantes não utilizadas no final de um buffer constante. Isso pode ter um impacto no mecanismo ao lidar com sombreadores grandes e a criação de layouts de entrada. Elementos que são removidos por otimizações de código inativo no compilador ainda devem ser declarados na estrutura de entrada. O exemplo a seguir demonstra este:

### <a name="vertex-shader-input-structure-example"></a>Exemplo de estrutura de entrada do sombreador de vértice


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* A remoção do código morto do Direct3D 9 removeria a declaração no sombreador devido à remoção do código morto condicional


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



Ou você poderia tornar ainda mais óbvio que a constante é uma constante de tempo de compilação com a seguinte declaração:


```
#define LIGHT_MAPPED false
```



No exemplo acima, sob o Direct3D 9, o elemento UV2 seria removido devido a otimizações de código inativo no compilador. No Direct3D 10, o código inativo ainda será removido, mas o layout do assembler de entrada do sombreador exige a definição dos dados de entrada para existir. A camada de reflexo do sombreador fornece os meios para lidar com essa situação de maneira genérica em que você pode percorrer os requisitos de entrada do sombreador e garantir que você forneça uma descrição completa do fluxo de entrada para o mapeamento de assinatura do sombreador.

Aqui está uma função de exemplo para detectar a existência de um nome/índice semântico em uma assinatura de função:


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

Ao portar o código do mecanismo, ele pode ajudar a usar inicialmente um conjunto padrão de objetos de estado e desabilitar todas as configurações de estado de renderização/estado de textura do dispositivo Direct3D 9. Isso causará artefatos de renderização, mas é a maneira mais rápida de colocar tudo em funcionamento. Posteriormente, você pode construir um sistema de gerenciamento de objetos de estado que pode usar uma chave composta para habilitar a reutilização máxima do número de objetos de estado que estão sendo usados.

## <a name="porting-textures"></a>Texturas portadoras

### <a name="file-formats-supported"></a>Formatos de arquivo com suporte

As funções **D3DXxxCreateXXX** e **D3DXxxSaveXXX** que criam ou salvam uma textura de ou para um arquivo gráfico (por exemplo, [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)) dão suporte a um conjunto diferente de formatos de arquivo no Direct3D 10 do que faziam no Direct3D 9:



| Formato de arquivo | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| .bmp        | x          | x           |
| .jpg        | x          | x           |
| .tga        | x          |             |
| .png        | x          | x           |
| .dds        | x          | x           |
| . ppm        | x          |             |
| .dib        | x          |             |
| . HDR        | x          |             |
| . PFM        | x          |             |
| .tiff       |            | x           |
| .gif        |            | x           |
| .tif        |            | x           |



 

Para obter detalhes, compare as enumerações de [**\_ FileFormat**](../direct3d9/d3dximage-fileformat.md) do Direct3D 9 D3DXIMAGE com as enumerações de [**\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md) para o Direct3D 10.

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8. Para o processamento de arquivo de textura, recomendamos que você use [DirectXTex](https://github.com/Microsoft/DirectXTex).

 

### <a name="mapping-texture-formats"></a>Mapeando formatos de textura

A tabela a seguir mostra o mapeamento de formatos de textura do Direct3D 9 para o Direct3D 10. Qualquer conteúdo em formatos não disponível em DXGI precisará ser convertido por rotinas de utilitário.



| Formato do Direct3D 9                   | Formato do Direct3D 10                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ desconhecido                     | \_formato dxgi \_ desconhecido                                                                                                                                                                                                                                |
| D3DFMT \_ R8G8B8                      | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A8R8G8B8                    | \_Formato dxgi \_ B8G8R8A8 \_ UNORM & dxgi \_ \_ B8G8R8A8 \_ UNORM \_ sRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ X8R8G8B8                    | \_Formato dxgi \_ B8G8R8X8 \_ UNORM & dxgi \_ \_ B8G8R8X8 \_ UNORM \_ sRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ R5G6B5                      | \_Formato dxgi \_ B5G6R5 \_ UNORM ²                                                                                                                                                                                                                         |
| D3DFMT \_ X1R5G5B5                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A1R5G5B5                    | \_Formato dxgi \_ B5G5R5A1 \_ UNORM ²                                                                                                                                                                                                                       |
| D3DFMT \_ A4R4G4B4                    | \_Formato dxgi \_ B4G4R4A4 \_ UNORM ³                                                                                                                                                                                                                       |
| D3DFMT \_ R3G3B2                      | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ a8                          | \_Formato dxgi \_ a8 \_ UNORM                                                                                                                                                                                                                              |
| D3DFMT \_ A8R3G3B2                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ X4R4G4B4                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A2B10G10R10                 | \_R10G10B10A2 de formato dxgi \_                                                                                                                                                                                                                            |
| D3DFMT \_ A8B8G8R8                    | \_Formato dxgi \_ R8G8B8A8 \_ UNORM & dxgi \_ \_ R8G8B8A8 \_ UNORM \_ sRGB                                                                                                                                                                                  |
| D3DFMT \_ X8B8G8R8                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ G16R16                      | \_Formato dxgi \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DFMT \_ A2R10G10B10                 | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A16B16G16R16                | \_Formato dxgi \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DFMT \_ A8P8                        | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | Não disponível                                                                                                                                                                                                                                        |
| \_L8 D3DFMT                          | \_ \_ \_ UNORM de R8 de formato dxgi Observação: use. r swizzle no sombreador para duplicar vermelho para outros componentes para obter o comportamento de d3d9.                                                                                                                                    |
| D3DFMT \_ A8L8                        | \_Formato dxgi \_ R8G8 \_ UNORM Observação: Use swizzle. rrrg no sombreador para duplicar vermelho e mover verde para os componentes alfa para obter o comportamento de d3d9.                                                                                                            |
| D3DFMT \_ A4L4                        | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ V8U8                        | \_Formato dxgi \_ R8G8 \_ SNORM                                                                                                                                                                                                                            |
| D3DFMT \_ L6V5U5                      | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ X8L8V8U8                    | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ Q8W8V8U8                    | \_Formato dxgi \_ R8G8B8A8 \_ SNORM                                                                                                                                                                                                                        |
| D3DFMT \_ V16U16                      | \_Formato dxgi \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DFMT \_ W11V11U10                   | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ A2W10V10U10                 | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ UYVY                        | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | \_Formato dxgi \_ G8R8 \_ G8B8 \_ UNORM (no DX9 os dados foram escalados verticalmente por 255.0 f, mas isso pode ser tratado no código do sombreador).                                                                                                                                   |
| D3DFMT \_ YUY2                        | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | \_Formato dxgi \_ R8G8 \_ B8G8 \_ UNORM (no DX9 os dados foram escalados verticalmente por 255.0 f, mas isso pode ser tratado no código do sombreador).                                                                                                                                   |
| D3DFMT \_ DXT1                        | \_Formato dxgi \_ BC1 \_ UNORM & dxgi \_ \_ BC1 \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT2                        | \_Formato dxgi \_ BC1 \_ UNORM & \_ formato dxgi \_ BC1 \_ UNORM \_ sRGB Observação: DXT1 e DXT2 são os mesmos de uma perspectiva de API/hardware... somente a diferença era ' pré-multiplicada Alfa ', que pode ser rastreada por um aplicativo e não precisa de um formato separado. |
| D3DFMT \_ DXT3                        | \_Formato dxgi \_ BC2 \_ UNORM & dxgi \_ \_ BC2 \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT4                        | \_Formato dxgi \_ BC2 \_ UNORM & \_ formato dxgi \_ BC2 \_ UNORM \_ sRGB Observação: DXT3 e DXT4 são os mesmos de uma perspectiva de API/hardware... somente a diferença era ' pré-multiplicada Alfa ', que pode ser rastreada por um aplicativo e não precisa de um formato separado. |
| D3DFMT \_ DXT5                        | \_Formato dxgi \_ BC3 \_ UNORM & dxgi \_ \_ BC3 \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ bloqueáveis | \_Formato dxgi \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32                         | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D15S1                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D24S8                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X8                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X4S4                     | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ D16                         | \_Formato dxgi \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32F \_ bloqueáveis              | \_ \_ Float D32 de formato dxgi \_                                                                                                                                                                                                                             |
| D3DFMT \_ D24FS8                      | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ S1D15                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ S8D24                       | \_Formato dxgi \_ D24 \_ UNORM \_ S8 \_ uint                                                                                                                                                                                                                   |
| D3DFMT \_ X8D24                       | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ X4S4D24                     | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ L16                         | \_Formato dxgi \_ R16 \_ UNORM Observação: use. r swizzle no sombreador para duplicar vermelho para outros componentes para obter o comportamento de d3d9.                                                                                                                                   |
| D3DFMT \_ INDEX16                     | \_Formato dxgi \_ R16 \_ uint                                                                                                                                                                                                                              |
| D3DFMT \_ INDEX32                     | \_Formato dxgi \_ R32 \_ uint                                                                                                                                                                                                                              |
| D3DFMT \_ Q16W16V16U16                | \_Formato dxgi \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DFMT \_ Multi2 \_ ARGB8               | Não disponível                                                                                                                                                                                                                                        |
| D3DFMT \_ R16F                        | \_ \_ Float R16 de formato dxgi \_                                                                                                                                                                                                                             |
| D3DFMT \_ G16R16F                     | \_ \_ Float R16G16 de formato dxgi \_                                                                                                                                                                                                                          |
| D3DFMT \_ A16B16G16R16F               | \_ \_ Float R16G16B16A16 de formato dxgi \_                                                                                                                                                                                                                    |
| D3DFMT \_ R32F                        | \_ \_ Float R32 de formato dxgi \_                                                                                                                                                                                                                             |
| D3DFMT \_ G32R32F                     | \_ \_ Float R32G32 de formato dxgi \_                                                                                                                                                                                                                          |
| D3DFMT \_ A32B32G32R32F               | \_ \_ Float R32G32B32A32 de formato dxgi \_                                                                                                                                                                                                                    |
| D3DFMT \_ CxV8U8                      | Não disponível                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT1                 | \_ \_ Float R32 de formato dxgi \_                                                                                                                                                                                                                             |
| D3DDECLTYPE \_ FLOAT2                 | \_ \_ Float R32G32 de formato dxgi \_                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT3                 | \_ \_ Float R32G32B32 de formato dxgi \_                                                                                                                                                                                                                       |
| D3DDECLTYPE \_ FLOAT4                 | \_ \_ Float R32G32B32A32 de formato dxgi \_                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | Não disponível                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ UBYTE4                 | \_Formato dxgi \_ R8G8B8A8 \_ uint Observação: o sombreador obtém valores uint, mas se os floats integral de estilo Direct3D 9 forem necessários (0,0 f, 1,0 f... 255. f), UINT pode ser convertido apenas em float32 no sombreador.                                                               |
| D3DDECLTYPE \_ SHORT2                 | \_Formato dxgi \_ R16G16 \_ Santo Observação: o sombreador obtém valores de Santo, mas se os floats integral de estilo Direct3D 9 forem necessários, Sint só poderá ser convertido em float32 no sombreador.                                                                                       |
| D3DDECLTYPE \_ SHORT4                 | \_Formato dxgi \_ R16G16B16A16 \_ Santo Observação: o sombreador obtém valores de Santo, mas se os floats integral de estilo Direct3D 9 forem necessários, Sint só poderá ser convertido em float32 no sombreador.                                                                                 |
| D3DDECLTYPE \_ UBYTE4N                | \_Formato dxgi \_ R8G8B8A8 \_ UNORM                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ SHORT2N                | \_Formato dxgi \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ SHORT4N                | \_Formato dxgi \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ USHORT2N               | \_Formato dxgi \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ USHORT4N               | \_Formato dxgi \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ UDEC3                  | Não disponível                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ DEC3N                  | Não disponível                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | \_ \_ Float R16G16 de formato dxgi \_                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | \_ \_ Float R16G16B16A16 de formato dxgi \_                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | \_Formato dxgi \_ BC4 \_ UNORM                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | \_Formato dxgi \_ BC5 \_ UNORM                                                                                                                                                                                                                             |



 

¹ DXGI 1,1, que está incluído no tempo de execução do Direct3D 11, inclui formatos BGRA. No entanto, o suporte para esses formatos é opcional para dispositivos Direct3D 10 e 10,1 com drivers que são implementados para o Windows Display Driver Model (WDDM) para Windows Vista (WDDM 1,0). Considere usar o \_ formato dxgi \_ R8G8B8A8 \_ UNORM em vez disso. Como alternativa, você pode criar seu dispositivo com o [**d3d10 \_ Create \_ Device \_ BGRA \_ support**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) para garantir que você só dê suporte a computadores com o tempo de execução do Direct3D 11,0 e um Driver WDDM 1,1 ou superior instalado.

os formatos 5:6:5 e 5:5:5:1 definidos pelo ² DXGI 1,0, mas não têm suporte do tempo de execução do Direct3D 10. x ou Direct3D 11,0. Opcionalmente, há suporte para esses formatos com DXGI 1,2 no tempo de execução do DirectX 11,1, que é necessário para os drivers de nível de vídeo 11,1 e WDDM 1,2 (modelo de driver de vídeo a partir do Windows 8) e que já têm suporte nos níveis de recursos do 10level9.

³ DXGI 1,2 introduziu o formato 4:4:4:4. Esse formato tem suporte opcional no tempo de execução do DirectX 11,1, que é necessário para os adaptadores de vídeo 11,1 de nível de recurso e drivers do WDDM 1,2 e que já têm suporte nos níveis de recursos do 10level9.

Para formatos não compactados, DXGI limitou o suporte para padrões de formato de pixel arbitrários; todos os formatos descompactados devem ser do tipo RGBA. Isso pode exigir swizzling de formatos de pixel de ativos existentes, que recomendamos que você calcule como uma passagem de pré-processamento offline sempre que possível.

## <a name="porting-shaders"></a>Portando sombreadores

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Os sombreadores do Direct3D 10 são criados no HLSL

O Direct3D 10 limita o uso da linguagem de assembly apenas para fins de depuração. portanto, qualquer um dos sombreadores de assembly escritos em mãos usados no Direct3D 9 precisará ser convertido em HLSL.

### <a name="shader-signatures-and-linkage"></a>Assinaturas e vinculação de sombreador

Discutimos os requisitos para vinculação de assembly de entrada a assinaturas de entrada de sombreador de vértice anteriormente neste documento (veja acima). Observe que o tempo de execução do Direct3D 10 também reforçava os requisitos de vinculação de estágio para estágio entre sombreadores. Essa alteração afetará as fontes do sombreador em que a associação entre os estágios pode não ter sido totalmente descrita no Direct3D 9. Por exemplo:


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* Vínculo VS-PS quebrado – embora o sombreador de pixel possa não estar interessado na matriz completa, a ligação deve especificar o float4x3 completo.

Observe que a semântica de vinculação entre os estágios deve corresponder exatamente no entanto, as entradas de estágios de destino podem ser um prefixo dos valores que estão sendo gerados. No exemplo acima, o sombreador de pixel poderia ter position e texcoord1 como as únicas entradas, mas não podia ter position e texcoord2 como as únicas entradas devido às restrições de ordenação.

### <a name="hlsl-shader-stage-linkages"></a>Ligações de estágio do sombreador HLSL

O vínculo entre sombreadores pode ocorrer em qualquer um dos seguintes pontos no pipeline:

-   Assembler de entrada para sombreador de vértice
-   Sombreador de vértice para sombreador de pixel
-   Sombreador de vértice para sombreador de geometria
-   Sombreador de vértice para saída de fluxo
-   Sombreador de geometria para sombreador de pixel
-   Sombreador de geometria para streaming

### <a name="constant-buffers"></a>Buffers de constantes

Para facilitar a portabilidade do conteúdo do Direct3D 9, uma abordagem inicial para o gerenciamento constante fora do sistema de efeitos pode envolver a criação de um único buffer de constante contendo todas as constantes necessárias. É importante que o desempenho ordene constantes em buffers pela frequência de atualização esperada. Essa organização reduzirá a quantidade de conjuntos de constantes redundantes para um mínimo.

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Planos de corte do usuário no HLSL no nível de recurso 9 e superior

A partir do Windows 8, você pode usar o atributo de função **clipplanes** em uma [declaração de função](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md) HLSL em vez de [VA \_ ClipDistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) para fazer com que o sombreador funcione no [nível de recurso](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, bem como no nível de recurso 10 e superior. Para obter mais informações, consulte os [planos de corte do usuário no hardware nível 9 do recurso](../direct3dhlsl/user-clip-planes-on-10level9.md).

## <a name="additional-direct3d-10-differences-to-watch-for"></a>Diferenças adicionais do Direct3D 10 a serem observadas

### <a name="integers-as-input"></a>Inteiros como entrada

No Direct3D 9, não havia nenhum suporte de hardware real para tipos de dados inteiros, no entanto, o hardware do Direct3D 10 dá suporte a tipos de inteiros explícitos. Se você tiver dados de ponto flutuante em seu buffer de vértice, deverá ter uma entrada float. Caso contrário, um tipo inteiro será a representação de padrão de bit do valor de ponto flutuante. Um tipo inteiro não é permitido para uma entrada de sombreador de pixel, a menos que o valor esteja marcado para nenhuma interpolação (consulte [modificadores de interpolação](../direct3dhlsl/dx-graphics-hlsl-struct.md)).

### <a name="mouse-cursors"></a>Cursores do mouse

Nas versões anteriores do Windows, as rotinas de cursor do mouse GDI padrão não operavam corretamente em todos os dispositivos de tela inteira. As APIs [**Setcursorproperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties), [**excursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)e [**SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) foram adicionadas para lidar com esses casos. Como a versão do GDI do Windows Vista compreende totalmente as superfícies [dxgi](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md) , não há necessidade dessa API especializada do cursor do mouse para que não haja nenhum equivalente do Direct3D 10. Em vez disso, os aplicativos do Direct3D 10 devem usar as [rotinas de cursor do mouse GDI](../menurc/cursors.md) padrão para cursores do mouse.

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>Mapeando texels para pixels no Direct3D 10

No Direct3D 9, os Texel centers e os centros de pixel eram uma metade de distância (veja [mapeamento direto de texels para pixels (Direct3D 9)](../direct3d9/directly-mapping-texels-to-pixels.md)). No Direct3D 10, os Texel centers já estão em meia-unidades, portanto, não há necessidade de deslocar as coordenadas de vértice.

A renderização de quatro processadores de tela inteira é mais direta com o Direct3D 10. Os quatro processadores de tela inteira devem ser definidos em clipspace (-1, 1) e simplesmente passados pelo sombreador de vértice sem alterações. Dessa forma, não há necessidade de recarregar o buffer de vértice sempre que a resolução da tela for alterada e não houver nenhum trabalho extra no sombreador de pixel para manipular as coordenadas de textura.

### <a name="reference-counting-behavior-changes"></a>Alterações de comportamento de contagem de referência

Ao contrário das versões anteriores do Direct3D, as várias funções de conjunto não terão uma referência aos objetos de dispositivos. Isso significa que o aplicativo deve garantir que ele tenha uma referência no objeto, desde que ele queira que o objeto esteja associado ao pipeline. Quando a contagem de referência do objeto cai para zero, o objeto será desassociado do pipeline conforme ele for destruído. Esse estilo de referência que mantém também é conhecido como uma chamada de referência fraca, portanto, cada local de ligação no objeto do dispositivo mantém uma referência fraca à interface/objeto. A menos que explicitamente mencionado de outra forma, esse comportamento deve ser assumido para todos os métodos definidos. Sempre que a destruição de um objeto fizer com que um ponto de ligação seja definido como **nulo** , a camada de depuração emitirá um aviso. Observe que as chamadas para métodos get de dispositivo, como [**OMGetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) , aumentarão a contagem de referência dos objetos que estão sendo retornados.

### <a name="test-cooperative-level"></a>Testar nível de cooperação

A funcionalidade da API do Direct3D 9 [**TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) é análoga à definição do [ \_ \_ teste de presença de dxgi](../direct3ddxgi/dxgi-present.md) ao chamar [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present).

### <a name="stretchrect"></a>StretchRect

Uma função semelhante ao método [**IDirect3DDevice9:: StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) do Direct3D 9 não está disponível no Direct3D 10 e 10,1. Para copiar superfícies de recursos, use [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Para operações de redimensionamento, renderize em uma textura usando a filtragem de textura. Para converter superfícies de MSAA em superfícies não MSAA, use [**ID3D10Device:: ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource).

## <a name="additional-direct3d-101-differences"></a>Diferenças adicionais do Direct3D 10,1

O Windows Vista com Service Pack 1 (SP1) incluiu uma pequena atualização para o Direct3D 10 e o Direct3D 10,1, que expôs os seguintes recursos de hardware adicionais:

-   Sombreadores por amostra de MSAA
-   Leitura de profundidade de MSAA
-   Modos de mesclagem independentes por destino de renderização
-   Matrizes do mapa do cubo
-   Renderizar para formatos compactados de bloco (BC)

A atualização do Direct3D 10,1 adicionou suporte para as novas interfaces a seguir, que são derivadas de interfaces existentes:

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

 

O Windows 7 continha uma pequena atualização para a API do Direct3D 10,1 que está incluída no tempo de execução do Direct3D 11. Esta atualização adiciona suporte para os seguintes níveis de recurso:

-   [**Nível de recurso do D3D10 \_ \_ \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**Nível de recurso do D3D10 \_ \_ \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**Nível de recurso do D3D10 \_ \_ \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

O Windows 7 também adicionou suporte ao Direct3D 10,1 para a [plataforma de rasterização avançada do Windows (Warp)](../direct3darticles/directx-warp.md). Você pode especificar um driver de detorção usando o [**\_ tipo de driver d3d10 \_ \_ Warp**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

Para obter mais informações sobre o Direct3D 10,1, consulte [recursos do direct3d 10,1](d3d10-graphics-programming-guide-10-1.md) e a enumeração do [**\_ recurso d3d10 \_ LEVEL1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
