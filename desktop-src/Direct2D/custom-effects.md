---
title: Efeitos personalizados
description: Mostra como escrever seus próprios efeitos personalizados usando HLSL padrão.
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084870"
---
# <a name="custom-effects"></a>Efeitos personalizados

O [Direct2D](./direct2d-portal.md) é fornecido com uma biblioteca de efeitos que executam uma variedade de operações de imagem comuns. Consulte o tópico sobre [efeitos internos](built-in-effects.md) para obter a lista completa de efeitos. Para a funcionalidade que não pode ser obtida com os efeitos internos, o Direct2D permite que você escreva seus próprios efeitos personalizados usando o [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)padrão. Você pode usar esses efeitos personalizados junto com os efeitos internos fornecidos com o Direct2D.

Para ver exemplos de um efeito completo de pixel, vértice e sombreador de computação, consulte o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

Neste tópico, mostramos as etapas e os conceitos necessários para projetar e criar um efeito personalizado repleto de recursos.

## <a name="introduction-what-is-inside-an-effect"></a>Introdução: o que está dentro de um efeito?

![diagrama de efeito de sombra drop.](images/custom-effects1.png)

Conceitualmente, um efeito [Direct2D](./direct2d-portal.md) executa uma tarefa de geração de imagens, como alterar o brilho, saturação uma imagem ou, como mostrado acima, criando uma sombra. Para o aplicativo, eles são simples. Eles podem aceitar zero ou mais imagens de entrada, expor várias propriedades que controlam sua operação e gerar uma única imagem de saída.

Há quatro partes diferentes de um efeito personalizado pelo qual um autor de efeito é responsável:

1.  Interface de efeito: a interface de efeito define conceitualmente como um aplicativo interage com um efeito personalizado (como quantas entradas o efeito aceita e quais propriedades estão disponíveis). A interface de efeito gerencia um grafo de transformação, que contém as operações de geração de imagens reais.
2.  Grafo de transformação: cada efeito cria um grafo de transformação interno composto por transformações individuais. Cada transformação representa uma única operação de imagem. O efeito é responsável por vincular essas transformações em um grafo para executar o efeito de imagem pretendido. Um efeito pode adicionar, remover, modificar e reordenar transformações em resposta a alterações nas propriedades externas do efeito.
3.  Transformação: uma transformação representa uma única operação de imagem. Sua principal finalidade é alojar os sombreadores que são executados para cada pixel de saída. Para esse fim, é responsável por calcular o novo tamanho de sua imagem de saída com base na lógica em seus sombreadores. Ele também deve calcular em qual área de sua imagem de entrada os sombreadores precisam ler para renderizar a região de saída solicitada.
4.  Sombreador: um sombreador é executado em relação à entrada da transformação na GPU (ou CPU se a renderização de software for especificada quando o aplicativo criar o dispositivo Direct3D). Os sombreadores de efeito são escritos em[HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)(linguagem de sombreamento de alto nível) e são compilados no código de bytes durante a compilação do efeito, que é então carregado pelo efeito durante o tempo de execução. Este documento de referência descreve como gravar HLSL em conformidade com [Direct2D](./direct2d-portal.md). A documentação do Direct3D contém uma visão geral do HLSL básico.

## <a name="creating-an-effect-interface"></a>Criando uma interface de efeito

A interface de efeito define como um aplicativo interage com o efeito personalizado. Para criar uma interface de efeito, uma classe deve implementar ID2D1EffectImpl, definir metadados que descrevem o efeito (como seu nome, contagem de entrada e propriedades) e criar métodos que registram o efeito personalizado para uso com [Direct2D](./direct2d-portal.md).

Depois que todos os componentes de uma interface de efeito tiverem sido implementados, o cabeçalho da classe será exibido da seguinte maneira:


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a>Implementar ID2D1EffectImpl

A interface [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) contém três métodos que você deve implementar:

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a>Initialize (ID2D1EffectContext \* pContextInternal, ID2D1TransformGraph \* pTransformGraph)

[Direct2D](./direct2d-portal.md) chama o método [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) após o método [**ID2D1DeviceContext:: createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) ser chamado pelo aplicativo. Você pode usar esse método para executar a inicialização interna ou qualquer outra operação necessária para o efeito. Além disso, você pode usá-lo para criar o grafo de transformação inicial do efeito.

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a>Setgraph (ID2D1TransformGraph \* pTransformGraph)

[Direct2D](./direct2d-portal.md) chama o método [**setgraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) quando o número de entradas para o efeito é alterado. Embora a maioria dos efeitos tenha um número constante de entradas, outros, como o [efeito composto](composite.md) , dão suporte a um número variável de entradas. Esse método permite que esses efeitos atualizem seu grafo de transformação em resposta a uma contagem de entrada variável. Se um efeito não oferecer suporte a uma contagem de entrada de variável, esse método poderá simplesmente retornar E \_ NOTIMPL.

### <a name="prepareforrender-d2d1_change_type-changetype"></a>PrepareForRender (alteração de tipo de alteração de D2D1 \_ \_ )

O método [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) fornece uma oportunidade de efeitos para executar qualquer operação em resposta a alterações externas. [Direct2D](./direct2d-portal.md) chama esse método logo antes de renderizar um efeito se pelo menos um deles for verdadeiro:

-   O efeito foi inicializado anteriormente, mas ainda não foi desenhado.
-   Uma propriedade de efeito foi alterada desde a última chamada de desenho.
-   O estado do contexto de [Direct2D](./direct2d-portal.md) de chamada (como DPI) foi alterado desde a última chamada de desenho.

### <a name="implement-the-effect-registration-and-callback-methods"></a>Implementar os métodos de registro de efeito e de retorno de chamada

Os aplicativos devem registrar efeitos com [Direct2D](./direct2d-portal.md) antes de instanciar. Esse registro tem como escopo uma instância de uma fábrica Direct2D e deve ser repetido sempre que o aplicativo é executado. Para habilitar esse registro, um efeito personalizado define um GUID exclusivo, um método público que registra o efeito e um método de retorno de chamada privado que retorna uma instância do efeito.

### <a name="define-a-guid"></a>Definir um GUID

Você deve definir um GUID que identifique exclusivamente o efeito para o registro com [Direct2D](./direct2d-portal.md). O aplicativo usa o mesmo para identificar o efeito quando chama [**ID2D1DeviceContext:: createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).

Esse código demonstra como definir tal GUID para um efeito. Você deve criar seu próprio GUID exclusivo usando uma ferramenta de geração de GUID, como guidgen.exe.


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a>Definir um método de registro público

Em seguida, defina um método público para o aplicativo chamar para registrar o efeito com [Direct2D](./direct2d-portal.md). Como o registro de efeito é específico de uma instância de uma fábrica Direct2D, o método aceita uma interface [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) como um parâmetro. Para registrar o efeito, o método chama a API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) no parâmetro **ID2D1Factory1** .

Essa API aceita uma cadeia de caracteres XML que descreve os metadados, as entradas e as propriedades do efeito. Os metadados para um efeito são apenas para fins informativos e podem ser consultados pelo aplicativo por meio da interface [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) . Os dados de entrada e propriedade, por outro lado, são usados pelo [Direct2D](./direct2d-portal.md) e representam a funcionalidade do efeito.

Uma cadeia de caracteres XML para um efeito de exemplo mínimo é mostrada aqui. A adição de propriedades personalizadas ao XML é abordada na seção Adicionando propriedades personalizadas a um efeito.


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a>Definir um método de retorno de chamada de fábrica de efeito

O efeito também deve fornecer um método de retorno de chamada privado que retorna uma instância do efeito por meio de um único \* \* parâmetro IUnknown. Um ponteiro para esse método é fornecido para [Direct2D](./direct2d-portal.md) quando o efeito é registrado por meio da API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) por meio do parâmetro de [**\_ \_ fábrica de efeito PD2D1**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a>Implementar a interface IUnknown

Por fim, o efeito deve implementar a interface IUnknown para compatibilidade com com.

## <a name="creating-the-effects-transform-graph"></a>Criando o grafo de transformação do efeito

Um efeito pode usar várias transformações diferentes (operações de imagem individuais) para criar seu efeito de imagem desejado. Para controlar a ordem na qual essas transformações são aplicadas à imagem de entrada, o efeito as organiza em um grafo de transformação. Um grafo de transformação pode fazer uso dos efeitos e transformações incluídos no [Direct2D](./direct2d-portal.md) , bem como transformações personalizadas criadas pelo autor do efeito.

### <a name="using-transforms-included-with-direct2d"></a>Usando transformações incluídas com Direct2D

Essas são as transformações mais comumente usadas fornecidas com [Direct2D](./direct2d-portal.md).

-   [**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): essa transformação mistura um número arbitrário de entradas com base em uma descrição de mistura, consulte o [**tópico \_ \_ Descrição do d2d1 Blend**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) e o [exemplo de modos de efeito composto do Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) para obter exemplos de mesclagem. Essa transformação é retornada pelo método [**ID2D1EffectContext:: CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .
-   [**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): essa transformação expande o tamanho de saída de uma imagem de acordo com o [**\_ \_ modo de extensão d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) especificado. Essa transformação é retornada pelo método [**ID2D1EffectContext:: CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .
-   [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): essa transformação desloca (traduz) sua entrada por qualquer número inteiro de pixels. Essa transformação é retornada pelo método [**ID2D1EffectContext:: CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .
-   Qualquer efeito existente pode ser tratado como uma transformação para fins de transformação de criação de grafo usando o método [**ID2D1EffectContext:: CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .

### <a name="creating-a-single-node-transform-graph"></a>Criando um grafo de transformação de nó único

Depois de criar uma transformação, a entrada do efeito precisa ser conectada à entrada da transformação e a saída da transformação precisa ser conectada à saída do efeito. Quando um efeito contém apenas uma única transformação, você pode usar o método [**ID2D1TransformGraph:: SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) para fazer isso facilmente.

Você pode criar ou modificar uma transformação nos métodos [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) ou [**setgraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) do efeito usando o parâmetro ID2D1TransformGraph fornecido. Se um efeito precisar fazer alterações no grafo de transformação em outro método em que esse parâmetro não esteja disponível, o efeito poderá salvar o parâmetro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) como uma variável de membro da classe e acessá-lo em outro lugar, como [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) ou um método de retorno de chamada de propriedade personalizada.

Um método de [**inicialização**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) de exemplo é mostrado aqui. Esse método cria um grafo de transformação de nó único que desloca a imagem em 100 pixels em cada eixo.


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a>Criando um grafo de transformação de vários nós

A adição de várias transformações ao grafo de transformação de um efeito permite que os efeitos realizem internamente várias operações de imagem que são apresentadas a um aplicativo como um único efeito unificado.

Conforme observado acima, o grafo de transformação do efeito pode ser editado em qualquer método de efeito usando o parâmetro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) recebido no método [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) do efeito. As seguintes APIs na interface podem ser usadas para criar ou modificar o grafo de transformação de um efeito:

### <a name="addnodeid2d1transformnode-pnode"></a>AddNode (ID2D1TransformNode \* pNode)

O método [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , em vigor, ' registra ' a transformação com o efeito e deve ser chamada antes que a transformação possa ser usada com qualquer um dos outros métodos de transformação do grafo.

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a>ConnectToEffectInput (UINT32 toEffectInputIndex, ID2D1TransformNode \* pNode, UINT32 toNodeInputIndex)

O método [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) conecta a entrada da imagem do efeito à entrada de uma transformação. A mesma entrada de efeito pode ser conectada a várias transformações.

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a>ConnectNode (ID2D1TransformNode \* pFromNode, ID2D1TransformNode \* PTONODE, UINT32 toNodeInputIndex)

O método [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) conecta a saída de uma transformação à entrada de outra transformação. Uma saída de transformação pode ser conectada a várias transformações.

### <a name="setoutputnodeid2d1transformnode-pnode"></a>SetOutputNode (ID2D1TransformNode \* pNode)

O método [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) conecta a saída de uma transformação à saída do efeito. Como um efeito tem apenas uma saída, apenas uma única transformação pode ser designada como ' nó de saída '.

Esse código usa duas transformações separadas para criar um efeito unificado. Nesse caso, o efeito é uma sombra projetada traduzida.


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a>Adicionando propriedades personalizadas a um efeito

Os efeitos podem definir propriedades personalizadas que permitem que um aplicativo altere o comportamento do efeito durante o tempo de execução. Há três etapas para definir uma propriedade para um efeito personalizado:

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a>Adicionar os metadados de propriedade aos dados de registro do efeito

### <a name="add-property-to-registration-xml"></a>Adicionar Propriedade ao XML de registro

Você deve definir as propriedades de um efeito personalizado durante o registro inicial do efeito com [Direct2D](./direct2d-portal.md). Primeiro, você deve atualizar o XML de registro do efeito em seu método de registro público com a nova propriedade:


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



Quando você define uma propriedade de efeito em XML, ela precisa de um nome, um tipo e um nome de exibição. O nome de exibição de uma propriedade, bem como os valores de categoria, autor e descrição do efeito geral podem e devem ser localizados.

Para cada propriedade, um efeito pode opcionalmente especificar valores padrão, mínimo e máximo. Esses valores são apenas para uso informativo. Eles não são impostos pelo [Direct2D](./direct2d-portal.md). Cabe a você implementar qualquer lógica padrão/mín/máx especificada na própria classe de efeito.

O valor de tipo listado no XML para a propriedade deve corresponder ao tipo de dados correspondente usado pelos métodos getter e setter da propriedade. Valores XML correspondentes para cada tipo de dados são mostrados nesta tabela:



| Tipo de dados                                                                                                                              | Valor XML correspondente |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| PWSTR                                                                                                                                  | string                  |
| BOOL                                                                                                                                   | bool                    |
| UINT                                                                                                                                   | uint32                  |
| INT                                                                                                                                    | int32                   |
| FLOAT                                                                                                                                  | FLOAT                   |
| [**\_Vetor D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | vector2                 |
| [**\_3F de vetor D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | Vector3                 |
| [**\_4F de vetor D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | Vector4                 |
| [**D2D \_ matriz \_ 3x2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool)) | matrix3x2               |
| [**D2D \_ matriz \_ 4x3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | matrix4x3               |
| [**D2D \_ matriz \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | matrix4x4               |
| [**D2D \_ matriz \_ 5X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | matrix5x4               |
| MINUCIOSA\[\]                                                                                                                               | blob                    |
| IUnknown\*                                                                                                                             | IUnknown                |
| [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*                                                                                       | colorcontext            |
| CLSID                                                                                                                                  | clsid                   |
| Enumeration ([**\_ \_ modo de interpolação d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)                                                | enum                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a>Mapear a nova propriedade para os métodos getter e setter

Em seguida, o efeito deve mapear essa nova propriedade para os métodos getter e setter. Isso é feito por meio da matriz de [**\_ \_ Associação de propriedade d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) que é passada para o método [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .

A matriz de [**\_ \_ associação da propriedade d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) é parecida com esta:


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



Depois de criar a matriz XML e bindings, passe-as para o método [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



A \_ macro de associação de tipo de valor d2d1 requer que \_ \_ a classe de efeito herde de [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) antes de qualquer outra interface.

As propriedades personalizadas de um efeito são indexadas na ordem em que são declaradas no XML e, uma vez criadas, podem ser acessadas pelo aplicativo usando os métodos [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) e [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) . Para sua conveniência, você pode criar uma enumeração pública que lista cada propriedade no arquivo de cabeçalho do efeito:


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a>Criar os métodos getter e setter para a propriedade

A próxima etapa é criar os métodos getter e setter para a nova propriedade. Os nomes dos métodos devem corresponder àqueles especificados na matriz de [**\_ \_ associação da propriedade d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) . Além disso, o tipo de propriedade especificado no XML do efeito deve corresponder ao tipo do parâmetro do método setter e ao valor de retorno do método getter.


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a>Atualizar as transformações do efeito em resposta à alteração da propriedade

Para realmente atualizar a saída da imagem de um efeito em resposta a uma alteração de propriedade, o efeito precisa alterar suas transformações subjacentes. Isso normalmente é feito no método [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) do efeito que o [Direct2D](./direct2d-portal.md) chama automaticamente quando uma das propriedades de um efeito é alterada. No entanto, as transformações podem ser atualizadas em qualquer um dos métodos do efeito: como inicializar ou os métodos setter da Propriedade do efeito.

Por exemplo, se um efeito contiver um [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) e quisesse modificar seu valor de deslocamento em resposta à propriedade de deslocamento do efeito que está sendo alterada, ele adicionaria o seguinte código em [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a>Criando uma transformação personalizada

Para implementar operações de imagem além do que é fornecido no [Direct2D](./direct2d-portal.md), você deve implementar transformações personalizadas. As transformações personalizadas podem alterar arbitrariamente uma imagem de entrada por meio do uso de sombreadores HLSL personalizados.

As transformações implementam uma das duas interfaces diferentes dependendo dos tipos de sombreadores que eles usam. As transformações que usam sombreadores de pixel e/ou vértice devem implementar [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), enquanto as transformações que usam sombreadores de computação devem implementar [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform). Essas interfaces herdam de [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform). Esta seção se concentra na implementação da funcionalidade que é comum para ambos.

A interface [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) tem quatro métodos para implementar:

### <a name="getinputcount"></a>GetInputCount

Esse método retorna um inteiro que representa a contagem de entrada para a transformação.


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a>MapInputRectsToOutputRect

[Direct2D](./direct2d-portal.md) chama o método [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) toda vez que a transformação é renderizada. Direct2D passa um retângulo que representa os limites de cada uma das entradas para a transformação. A transformação é então responsável pelo cálculo dos limites da imagem de saída. O tamanho dos retângulos para todos os métodos nesta interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) são definidos em pixels, não DIPs.

Esse método também é responsável por calcular a região da saída que é opaca com base na lógica do seu sombreador e nas regiões opacas de cada entrada. Uma região opaca de uma imagem é definida como aquela em que o canal alfa é ' 1 ' para todo o retângulo. Se não estiver claro se a saída de uma transformação é opaca, o retângulo opaco de saída deve ser definido como (0, 0, 0, 0) como um valor seguro. O [Direct2D](./direct2d-portal.md) usa essas informações para executar otimizações de renderização com o conteúdo ' garantido opaco '. Se esse valor for impreciso, ele poderá resultar em renderização incorreta.

Você pode modificar o comportamento de renderização da transformação (conforme definido nas seções 6 a 8) durante esse método. No entanto, não é possível modificar outras transformações no grafo de transformação ou o próprio layout do grafo aqui.


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



Para obter um exemplo mais complexo, considere como uma operação de desfoque simples seria representada:

Se uma operação de desfoque usar um raio de 5 pixels, o tamanho do retângulo de saída deverá ser expandido em 5 pixels, conforme mostrado abaixo. Ao modificar as coordenadas do retângulo, uma transformação deve garantir que sua lógica não cause nenhum fluxo acima/estourado nas coordenadas do retângulo.


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



Como a imagem está borrada, uma região da imagem opaca pode agora ser parcialmente transparente. Isso ocorre porque a área fora da imagem assume o padrão de preto transparente e essa transparência será mesclada na imagem ao lado das bordas. A transformação deve refletir isso em seus cálculos de retângulo opaco de saída:


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



Esses cálculos são visualizados aqui:

![ilustração de cálculo de retângulo.](images/custom-effects2.png)

Para obter mais informações sobre esse método, consulte a página de referência do [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .

### <a name="mapoutputrecttoinputrects"></a>MapOutputRectToInputRects

[Direct2D](./direct2d-portal.md) chama o método [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) após [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). A transformação deve calcular em qual parte da imagem ele precisa ler para processar corretamente a região de saída solicitada.

Como antes, se um efeito mapear estritamente pixels 1-1, ele poderá passar o retângulo de saída para o retângulo de entrada:


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



Da mesma forma, se uma transformação reduzir ou expandir uma imagem (como o exemplo de desfoque aqui), os pixels geralmente usam pixels circundantes para calcular seu valor. Com um desfoque, é feita a média de um pixel com seus pixels ao redor, mesmo que eles estejam fora dos limites da imagem de entrada. Esse comportamento é refletido no cálculo. Como antes, a transformação verifica se há estouros ao expandir as coordenadas de um retângulo.


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



Esta figura visualiza o cálculo. O [Direct2D](./direct2d-portal.md) automaticamente Obtém pixels pretos transparentes em que a imagem de entrada não existe, permitindo que o desfoque seja mesclado gradualmente com o conteúdo existente na tela.

![ilustração de um efeito de amostragem de pixels pretos transparentes fora de um retângulo.](images/custom-effects3.png)

Se o mapeamento não for trivial, esse método deverá definir o retângulo de entrada para a área máxima para garantir os resultados corretos. Para fazer isso, defina as bordas esquerda e superior como INT \_ min e as bordas direita e inferior como int \_ máx.

Para obter mais informações sobre esse método, consulte o tópico [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .

### <a name="mapinvalidrect"></a>MapInvalidRect

[Direct2D](./direct2d-portal.md) também chama o método [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . No entanto, ao contrário dos métodos [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) e [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) , não é garantido chamá-lo em um momento específico. Esse método conceitualmente decide que parte da saída de uma transformação precisa ser renderizada novamente em resposta a parte ou a todas as suas alterações de entrada. Há três cenários diferentes para os quais calcular o Rect inválido de uma transformação.

### <a name="transforms-with-one-to-one-pixel-mapping"></a>Transformações com mapeamento de pixel de um para um

Para transformações que mapeiam os pixels 1-1, basta passar o retângulo de entrada inválido para o retângulo de saída inválido:


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a>Transformações com mapeamento de pixel muitos para muitos

Quando os pixels de saída de uma transformação dependem de sua área ao redor, o retângulo de entrada inválido deve ser expandido de forma correspondente. Isso é para refletir que os pixels que circundam o retângulo de entrada inválido também serão afetados e se tornarão inválidos. Por exemplo, um desfoque de cinco pixels usa o seguinte cálculo:


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a>Transformações com mapeamento de pixel complexo

Para transformações em que os pixels de entrada e saída não têm um mapeamento simples, toda a saída pode ser marcada como inválida. Por exemplo, se uma transformação simplesmente produzir a cor média da entrada, toda a saída da transformação será alterada se até mesmo uma pequena parte da entrada for alterada. Nesse caso, o retângulo de saída inválido deve ser definido como um retângulo logicamente infinito (mostrado abaixo). [Direct2D](./direct2d-portal.md) coloca automaticamente os limites da saída.


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



Para obter mais informações sobre esse método, consulte o tópico [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .

Depois que esses métodos forem implementados, o cabeçalho da transformação conterá o seguinte:


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a>Adicionando um sombreador de pixel a uma transformação personalizada

Depois que uma transformação tiver sido criada, ela precisará fornecer um sombreador que manipulará os pixels da imagem. Esta seção aborda as etapas para usar um sombreador de pixel com uma transformação personalizada.

### <a name="implementing-id2d1drawtransform"></a>Implementando ID2D1DrawTransform

Para usar um sombreador de pixel, a transformação deve implementar a interface [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , que herda da interface [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) descrita na seção 5. Essa interface contém um novo método para implementar:

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a>SetDrawInfo (ID2D1DrawInfo \* pDrawInfo)

[Direct2D](./direct2d-portal.md) chama o método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) quando a transformação é adicionada pela primeira vez ao grafo de transformação de um efeito. Esse método fornece um parâmetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) que controla como a transformação é renderizada. Consulte o tópico **ID2D1DrawInfo** para obter os métodos disponíveis aqui.

Se a transformação optar por armazenar esse parâmetro como uma variável de membro de classe, o objeto *drawInfo* poderá ser acessado e alterado de outros métodos, como setters de propriedade ou [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). Notavelmente, não pode ser chamado a partir dos métodos [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) ou [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) no [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).

### <a name="creating-a-guid-for-the-pixel-shader"></a>Criando um GUID para o sombreador de pixel

Em seguida, a transformação deve definir um GUID exclusivo para o sombreador de pixel em si. Isso é usado quando o [Direct2D](./direct2d-portal.md) carrega o sombreador na memória, bem como quando a transformação escolhe qual pixel shader usar para execução. Ferramentas como guidgen.exe, que está incluído no Visual Studio, podem ser usadas para gerar um GUID aleatório.


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a>Carregando o sombreador de pixel com Direct2D

Um sombreador de pixel deve ser carregado na memória antes que possa ser usado pela transformação.

Para carregar o sombreador de pixel na memória, a transformação deve ler o código de byte do sombreador compilado do. Arquivo CSO gerado pelo Visual Studio (consulte a documentação do [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obter detalhes) em uma matriz de bytes. Essa técnica é demonstrada em detalhes no [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

Depois que os dados do sombreador tiverem sido carregados em uma matriz de bytes, chame o método [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) no objeto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) do efeito. [Direct2D](./direct2d-portal.md) ignora as chamadas para **LoadPixelShader** quando um sombreador com o mesmo GUID já foi carregado.

Depois que um sombreador de pixel é carregado na memória, a transformação precisa selecioná-lo para execução passando seu GUID para o método [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) no parâmetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fornecido durante o método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) . O sombreador de pixel já deve estar carregado na memória antes de ser selecionado para execução.

### <a name="changing-shader-operation-with-constant-buffers"></a>Alterando a operação do sombreador com buffers de constantes

Para alterar a forma como um sombreador é executado, uma transformação pode passar um buffer constante para o sombreador de pixel. Para fazer isso, uma transformação define uma struct que contém as variáveis desejadas no cabeçalho da classe:


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



Em seguida, a transformação chama o método [**ID2D1DrawInfo:: SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) no parâmetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fornecido no método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) para passar esse buffer para o sombreador.

O [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) também precisa definir uma struct correspondente que representa o buffer de constantes. As variáveis contidas no struct do sombreador devem corresponder às do struct da transformação.


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



Depois que o buffer tiver sido definido, os valores contidos em podem ser lidos de qualquer lugar dentro do sombreador de pixel.

### <a name="writing-a-pixel-shader-for-direct2d"></a>Escrevendo um sombreador de pixel para Direct2D

[Direct2D](./direct2d-portal.md) transformações de uso de sombreadores criados usando [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)padrão. No entanto, há alguns conceitos fundamentais para escrever um sombreador de pixel que é executado a partir do contexto de uma transformação. Para obter um exemplo completo de um sombreador de pixel totalmente funcional, consulte o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

O [Direct2D](./direct2d-portal.md) mapeia automaticamente as entradas de uma transformação para os objetos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**samplestate**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) no HLSL. O primeiro **Texture2D** está localizado em Register T0, e o primeiro **samplestate** está localizado em Register S0. Cada entrada adicional está localizada nos próximos registros correspondentes (T1 e S1, por exemplo). Os dados de pixel de uma determinada entrada podem ser amostrados chamando o exemplo no objeto **Texture2D** e passando o objeto de **amostrastate** correspondente e as coordenadas de Texel.

Um sombreador de pixel personalizado é executado uma vez para cada pixel renderizado. Cada vez que o sombreador é executado, o [Direct2D](./direct2d-portal.md) fornece automaticamente três parâmetros que identificam sua posição de execução atual:

-   Saída de espaço de cena: esse parâmetro representa a posição de execução atual em termos da superfície de destino geral. Ele é definido em pixels e seus valores mínimo/máximo correspondem aos limites do retângulo retornado por [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).
-   Saída de clip-Space: esse parâmetro é usado pelo Direct3D e não deve ser usado no sombreador de pixel de uma transformação.
-   Texel-Space Input: esse parâmetro representa a posição de execução atual em uma textura de entrada específica. Um sombreador não deve assumir nenhuma dependência de como esse valor é calculado. Ele só deve usá-lo para exemplificar a entrada do sombreador de pixel, conforme mostrado no código abaixo:


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a>Adicionando um sombreador de vértice a uma transformação personalizada

Você pode usar sombreadores de vértice para realizar diferentes cenários de geração de imagens do que sombreadores de pixel. Em particular, os sombreadores de vértice podem executar efeitos de imagem baseados em geometria transformando vértices que compõem uma imagem. Os sombreadores de vértice podem ser usados independentemente ou em conjunto com sombreadores de pixel especificados para transformação. Se um sombreador de vértice não for especificado, [Direct2D](./direct2d-portal.md) substituirá em um sombreador de vértice padrão para uso com o sombreador de pixel personalizado.

O processo para adicionar um sombreador de vértice a uma transformação personalizada é semelhante ao de um sombreador de pixel – a transformação implementa a interface [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , cria um GUID e (opcionalmente) passa buffers constantes para o sombreador. No entanto, há algumas etapas adicionais que são exclusivas de sombreadores de vértice:

### <a name="creating-a-vertex-buffer"></a>Criando um buffer de vértice

Um sombreador de vértice por definição é executado em vértices passados para ele, não para pixels individuais. Para especificar os vértices em que o sombreador será executado, uma transformação cria um buffer de vértice para passar para o sombreador. O layout dos buffers de vértice está além do escopo deste documento. Consulte a [referência do Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obter detalhes ou o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obter uma implementação de exemplo.

Depois de criar um buffer de vértice na memória, a transformação usa o método [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) no objeto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) do efeito que o contém para passar os dados para a GPU. Novamente, consulte o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obter uma implementação de exemplo.

Se nenhum buffer de vértice for especificado pela transformação, [Direct2D](./direct2d-portal.md) passará um buffer de vértice padrão que representa o local da imagem retangular.

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a>Alterando SetDrawInfo para utilizar um sombreador de vértice

Assim como com sombreadores de pixel, a transformação deve carregar e selecionar um sombreador de vértice para execução. Para carregar o sombreador de vértice, ele chama o método [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) no método [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) recebido no método Initialize do efeito. Para selecionar o sombreador de vértice para execução, ele chama [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) no parâmetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) recebido no método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) da transformação. Esse método aceita um GUID para um sombreador de vértices previamente carregado, bem como (opcionalmente) um buffer de vértice criado anteriormente para o sombreador a ser executado.

### <a name="implementing-a-direct2d-vertex-shader"></a>Implementando um sombreador de vértice Direct2D

Uma transformação de desenho pode conter um sombreador de pixel e um sombreador de vértice. Se uma transformação definir um sombreador de pixel e um sombreador de vértice, a saída do sombreador de vértice será fornecida diretamente ao sombreador de pixel: o aplicativo poderá personalizar a assinatura de retorno do sombreador de vértice/os parâmetros do sombreador de pixel, contanto que eles sejam consistentes.

Por outro lado, se uma transformação contiver apenas um sombreador de vértice e depender do sombreador de pixel de passagem padrão do [Direct2D](./direct2d-portal.md), ele deverá retornar a seguinte saída padrão:


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Um sombreador de vértice armazena o resultado de suas transformações de vértice na variável de saída do espaço de cena do sombreador. Para computar a saída do clipe e as variáveis de entrada de Texel, o [Direct2D](./direct2d-portal.md) fornece automaticamente matrizes de conversão em um buffer constante:


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



O código de sombreador de vértice de exemplo pode ser encontrado abaixo, que usa as matrizes de conversão para calcular o clipe correto e os espaços de Texel esperados pelo [Direct2D](./direct2d-portal.md):


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



O código acima pode ser usado como um ponto de partida para um sombreador de vértice. Ele simplesmente passa pela imagem de entrada sem executar nenhuma transformação. Novamente, consulte o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para uma transformação baseada em sombreador de vértice totalmente implementada.

Se nenhum buffer de vértice for especificado pela transformação, o [Direct2D](./direct2d-portal.md) substituirá em um buffer de vértice padrão que representa o local da imagem retangular. Os parâmetros para o sombreador de vértice são alterados para os da saída do sombreador padrão:


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



O sombreador de vértice não pode modificar seus parâmetros *sceneSpaceOutput* e *clipSpaceOutput* . Ele deve retorná-las inalteradas. No entanto, pode modificar os parâmetros *texelSpaceInput* para cada imagem de entrada. Se a transformação também contiver um sombreador de pixel personalizado, o sombreador de vértice ainda poderá passar parâmetros personalizados adicionais diretamente para o sombreador de pixel. Além disso, o buffer personalizado das matrizes de conversão *sceneSpace* (B0) não é mais fornecido.

## <a name="adding-a-compute-shader-to-a-custom-transform"></a>Adicionando um sombreador de computação a uma transformação personalizada

Por fim, as transformações personalizadas podem utilizar sombreadores de computação para determinados cenários de destino. Os sombreadores de computação podem ser usados para implementar efeitos de imagem complexos que exigem acesso arbitrário aos buffers de imagem de entrada e saída. Por exemplo, um algoritmo de histograma básico não pode ser implementado com um sombreador de pixel devido a limitações no acesso à memória.

Como os sombreadores de computação têm requisitos de nível de recursos de hardware mais altos que os sombreadores de pixel, os sombreadores de pixel devem ser usados quando possível para implementar um determinado efeito. Especificamente, os sombreadores de computação só são executados na maioria dos cartões de nível DirectX 10 e superiores. Se uma transformação optar por usar um sombreador de computação, ela deverá verificar o suporte de hardware apropriado durante a instanciação, além da implementação da interface [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .

### <a name="checking-for-compute-shader-support"></a>Verificando o suporte ao sombreador de computação

Se um efeito usar um sombreador de computação, ele deverá verificar o suporte ao sombreador de computação durante sua criação usando o método [**ID2D1EffectContext:: CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) . Se a GPU não oferecer suporte a sombreadores de computação, o efeito deverá retornar [**D2DERR \_ \_ \_ recursos de dispositivo insuficientes**](direct2d-error-codes.md).

Há dois tipos diferentes de sombreadores de computação que uma transformação pode usar: Shader Model 4 (DirectX 10) e Shader Model 5 (DirectX 11). Há certas limitações para sombreadores do modelo de sombreador 4. Consulte a documentação do [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obter detalhes. As transformações podem conter os dois tipos de sombreadores e podem voltar para o modelo de sombreador 4 quando necessário: consulte a [amostra do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para uma implementação disso.

### <a name="implement-id2d1computetransform"></a>Implementar ID2D1ComputeTransform

Essa interface contém dois novos métodos para implementar além daqueles no [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a>SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo)

Assim como com sombreadores de pixel e Vertex, [Direct2D](./direct2d-portal.md) chama o método [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) quando a transformação é adicionada pela primeira vez ao grafo de transformação de um efeito. Esse método fornece um parâmetro [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) que controla como a transformação é renderizada. Isso inclui escolher o sombreador de computação a ser executado por meio do método [**ID2D1ComputeInfo:: SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) . Se a transformação optar por armazenar esse parâmetro como uma variável de membro de classe, ele poderá ser acessado e alterado de qualquer método de transformação ou efeito com a exceção dos métodos [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) e [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . Consulte o tópico **ID2D1ComputeInfo** para ver outros métodos disponíveis aqui.

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a>CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect, UInt32 \* PDIMENSIONX, UInt32 \* pDimensionY, UInt32 \* pDimensionZ)

Enquanto os sombreadores de pixel são executados em uma base por pixel e os sombreadores de vértice são executados por vértice, os sombreadores de computação são executados de acordo com a 'threadgroupidade. Um objectthread representa um número de threads que são executados simultaneamente na GPU. O código HLSL do sombreador de computação decide quantos threads devem ser executados por um thread. O efeito dimensiona o número de threadgroups para que o sombreador execute o número desejado de vezes, dependendo da lógica do sombreador.

O método [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) permite que a transformação informe ao [Direct2D](./direct2d-portal.md) quantos grupos de threads são necessários, com base no tamanho da imagem e no conhecimento próprio da transformação do sombreador.

O número de vezes que o sombreador de computação é executado é um produto das contagens do The threadly especificado aqui e a anotação ' numthreads ' no [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)do sombreador de computação. Por exemplo, se a transformação definir as dimensões do grupos de threads como (2, 2, 1) o sombreador especificar (3, 3, 1) threads por thread, 4 threadgroups será executado, cada um com 9 threads, para um total de 36 instâncias de thread.

Um cenário comum é processar um pixel de saída para cada instância do sombreador de computação. Para calcular o número de grupos de threads para esse cenário, a transformação divide a largura e a altura da imagem pelas respectivas dimensões x e y da anotação ' numthreads ' no sombreador de computação [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).

Importante, se essa divisão for executada, o número de grupos de threads solicitados deve sempre ser arredondado para o número inteiro mais próximo, caso contrário, os pixels ' resto ' não serão executados no. Se um sombreador (por exemplo) computa um único pixel com cada thread, o código do método seria exibido da seguinte maneira.


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



O [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) usa o seguinte código para especificar o número de threads em cada grupo de threads:


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



Durante a execução, o Current thread e o índice de thread atual são passados como parâmetros para o método Shader:


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a>Lendo dados da imagem

Os sombreadores de computação acessam a imagem de entrada da transformação como uma única textura bidimensional:


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



No entanto, como sombreadores de pixel, não há garantia de que os dados da imagem comecem em (0, 0) na textura. Em vez disso, o [Direct2D](./direct2d-portal.md) fornece constantes do sistema que permitem que os sombreadores compensam qualquer deslocamento:


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



Depois que o buffer constante acima e o método auxiliar tiverem sido definidos, o sombreador poderá obter amostras de dados de imagem usando o seguinte:


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a>Gravando dados de imagem

[Direct2D](./direct2d-portal.md) espera que um sombreador defina um buffer de saída para que a imagem resultante seja colocada. No Shader Model 4 (DirectX 10), deve ser um buffer unidimensional devido a restrições de recurso:


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



A textura de saída é indexada na linha-primeiro para permitir que toda a imagem seja armazenada.


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



Por outro lado, os sombreadores do modelo do sombreador 5 (DirectX 11) podem usar texturas de saída bidimensionais:


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



Com sombreadores do modelo do sombreador 5, [Direct2D](./direct2d-portal.md) fornece um parâmetro "outputOffset" adicional no buffer de constantes. A saída do sombreador deve ser offsettedda por esse valor:


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



Um sombreador de computação de modelo de sombreamento de passagem 5 concluído é mostrado abaixo. Nele, cada um dos threads de sombreador de computação lê e grava um único pixel da imagem de entrada.


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



O código a seguir mostra a versão equivalente do modelo de sombreador 4 do sombreador. Observe que o sombreador agora é renderizado em um buffer de saída unidimensional.


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 