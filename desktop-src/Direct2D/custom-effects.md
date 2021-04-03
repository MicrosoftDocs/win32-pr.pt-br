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
# <a name="custom-effects"></a><span data-ttu-id="6584c-103">Efeitos personalizados</span><span class="sxs-lookup"><span data-stu-id="6584c-103">Custom effects</span></span>

<span data-ttu-id="6584c-104">O [Direct2D](./direct2d-portal.md) é fornecido com uma biblioteca de efeitos que executam uma variedade de operações de imagem comuns.</span><span class="sxs-lookup"><span data-stu-id="6584c-104">[Direct2D](./direct2d-portal.md) ships with a library of effects that perform a variety of common image operations.</span></span> <span data-ttu-id="6584c-105">Consulte o tópico sobre [efeitos internos](built-in-effects.md) para obter a lista completa de efeitos.</span><span class="sxs-lookup"><span data-stu-id="6584c-105">See the [built-in effects](built-in-effects.md) topic for the complete list of effects.</span></span> <span data-ttu-id="6584c-106">Para a funcionalidade que não pode ser obtida com os efeitos internos, o Direct2D permite que você escreva seus próprios efeitos personalizados usando o [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)padrão.</span><span class="sxs-lookup"><span data-stu-id="6584c-106">For functionality that cannot be achieved with the built-in effects, Direct2D allows you to write your own custom effects using standard [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl).</span></span> <span data-ttu-id="6584c-107">Você pode usar esses efeitos personalizados junto com os efeitos internos fornecidos com o Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6584c-107">You can use these custom effects alongside the built-in effects that ship with Direct2D.</span></span>

<span data-ttu-id="6584c-108">Para ver exemplos de um efeito completo de pixel, vértice e sombreador de computação, consulte o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="6584c-108">To see examples of a complete pixel, vertex, and compute shader effect, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="6584c-109">Neste tópico, mostramos as etapas e os conceitos necessários para projetar e criar um efeito personalizado repleto de recursos.</span><span class="sxs-lookup"><span data-stu-id="6584c-109">In this topic, we show you the steps and concepts you need to design and create a fully-featured custom effect.</span></span>

## <a name="introduction-what-is-inside-an-effect"></a><span data-ttu-id="6584c-110">Introdução: o que está dentro de um efeito?</span><span class="sxs-lookup"><span data-stu-id="6584c-110">Introduction: What is inside an effect?</span></span>

![diagrama de efeito de sombra drop.](images/custom-effects1.png)

<span data-ttu-id="6584c-112">Conceitualmente, um efeito [Direct2D](./direct2d-portal.md) executa uma tarefa de geração de imagens, como alterar o brilho, saturação uma imagem ou, como mostrado acima, criando uma sombra.</span><span class="sxs-lookup"><span data-stu-id="6584c-112">Conceptually, a [Direct2D](./direct2d-portal.md) effect performs an imaging task, like changing brightness, de-saturating an image, or as shown above, creating a drop shadow.</span></span> <span data-ttu-id="6584c-113">Para o aplicativo, eles são simples.</span><span class="sxs-lookup"><span data-stu-id="6584c-113">To the app, they are simple.</span></span> <span data-ttu-id="6584c-114">Eles podem aceitar zero ou mais imagens de entrada, expor várias propriedades que controlam sua operação e gerar uma única imagem de saída.</span><span class="sxs-lookup"><span data-stu-id="6584c-114">They can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="6584c-115">Há quatro partes diferentes de um efeito personalizado pelo qual um autor de efeito é responsável:</span><span class="sxs-lookup"><span data-stu-id="6584c-115">There are four different parts of a custom effect that an effect author is responsible for:</span></span>

1.  <span data-ttu-id="6584c-116">Interface de efeito: a interface de efeito define conceitualmente como um aplicativo interage com um efeito personalizado (como quantas entradas o efeito aceita e quais propriedades estão disponíveis).</span><span class="sxs-lookup"><span data-stu-id="6584c-116">Effect Interface: The effect interface conceptually defines how an app interacts with a custom effect (like how many inputs the effect accepts and what properties are available).</span></span> <span data-ttu-id="6584c-117">A interface de efeito gerencia um grafo de transformação, que contém as operações de geração de imagens reais.</span><span class="sxs-lookup"><span data-stu-id="6584c-117">The effect interface manages a transform graph, which contains the actual imaging operations.</span></span>
2.  <span data-ttu-id="6584c-118">Grafo de transformação: cada efeito cria um grafo de transformação interno composto por transformações individuais.</span><span class="sxs-lookup"><span data-stu-id="6584c-118">Transform graph: Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="6584c-119">Cada transformação representa uma única operação de imagem.</span><span class="sxs-lookup"><span data-stu-id="6584c-119">Each transform represents a single image operation.</span></span> <span data-ttu-id="6584c-120">O efeito é responsável por vincular essas transformações em um grafo para executar o efeito de imagem pretendido.</span><span class="sxs-lookup"><span data-stu-id="6584c-120">The effect is responsible for linking these transforms together into a graph to perform the intended imaging effect.</span></span> <span data-ttu-id="6584c-121">Um efeito pode adicionar, remover, modificar e reordenar transformações em resposta a alterações nas propriedades externas do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-121">An effect can add, remove, modify, and reorder transforms in response to changes to the effect's external properties.</span></span>
3.  <span data-ttu-id="6584c-122">Transformação: uma transformação representa uma única operação de imagem.</span><span class="sxs-lookup"><span data-stu-id="6584c-122">Transform: A transform represents a single image operation.</span></span> <span data-ttu-id="6584c-123">Sua principal finalidade é alojar os sombreadores que são executados para cada pixel de saída.</span><span class="sxs-lookup"><span data-stu-id="6584c-123">Its main purpose is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="6584c-124">Para esse fim, é responsável por calcular o novo tamanho de sua imagem de saída com base na lógica em seus sombreadores.</span><span class="sxs-lookup"><span data-stu-id="6584c-124">To that end, it is responsible for calculating the new size of its output image based on logic in its shaders.</span></span> <span data-ttu-id="6584c-125">Ele também deve calcular em qual área de sua imagem de entrada os sombreadores precisam ler para renderizar a região de saída solicitada.</span><span class="sxs-lookup"><span data-stu-id="6584c-125">It also must calculate which area of its input image the shaders need to read from to render the requested output region.</span></span>
4.  <span data-ttu-id="6584c-126">Sombreador: um sombreador é executado em relação à entrada da transformação na GPU (ou CPU se a renderização de software for especificada quando o aplicativo criar o dispositivo Direct3D).</span><span class="sxs-lookup"><span data-stu-id="6584c-126">Shader: A shader is executed against the transform's input on the GPU (or CPU if software rendering is specified when the app creates the Direct3D device).</span></span> <span data-ttu-id="6584c-127">Os sombreadores de efeito são escritos em[HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)(linguagem de sombreamento de alto nível) e são compilados no código de bytes durante a compilação do efeito, que é então carregado pelo efeito durante o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6584c-127">Effect shaders are written in High Level Shading Language ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) and are compiled into byte code during the effect's compilation, which is then loaded by the effect during run-time.</span></span> <span data-ttu-id="6584c-128">Este documento de referência descreve como gravar HLSL em conformidade com [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6584c-128">This reference document describes how to write [Direct2D](./direct2d-portal.md)-compliant HLSL.</span></span> <span data-ttu-id="6584c-129">A documentação do Direct3D contém uma visão geral do HLSL básico.</span><span class="sxs-lookup"><span data-stu-id="6584c-129">The Direct3D documentation contains a basic HLSL overview.</span></span>

## <a name="creating-an-effect-interface"></a><span data-ttu-id="6584c-130">Criando uma interface de efeito</span><span class="sxs-lookup"><span data-stu-id="6584c-130">Creating an effect interface</span></span>

<span data-ttu-id="6584c-131">A interface de efeito define como um aplicativo interage com o efeito personalizado.</span><span class="sxs-lookup"><span data-stu-id="6584c-131">The effect interface defines how an app interacts with the custom effect.</span></span> <span data-ttu-id="6584c-132">Para criar uma interface de efeito, uma classe deve implementar ID2D1EffectImpl, definir metadados que descrevem o efeito (como seu nome, contagem de entrada e propriedades) e criar métodos que registram o efeito personalizado para uso com [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6584c-132">To create an effect interface, a class must implement ID2D1EffectImpl, define metadata that describes the effect (such as its name, input count and properties), and create methods that register the custom effect for use with [Direct2D](./direct2d-portal.md).</span></span>

<span data-ttu-id="6584c-133">Depois que todos os componentes de uma interface de efeito tiverem sido implementados, o cabeçalho da classe será exibido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6584c-133">Once all of the components for an effect interface have been implemented, the class' header will appear like this:</span></span>


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



### <a name="implement-id2d1effectimpl"></a><span data-ttu-id="6584c-134">Implementar ID2D1EffectImpl</span><span class="sxs-lookup"><span data-stu-id="6584c-134">Implement ID2D1EffectImpl</span></span>

<span data-ttu-id="6584c-135">A interface [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) contém três métodos que você deve implementar:</span><span class="sxs-lookup"><span data-stu-id="6584c-135">The [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) interface contains three methods that you must implement:</span></span>

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a><span data-ttu-id="6584c-136">Initialize (ID2D1EffectContext \* pContextInternal, ID2D1TransformGraph \* pTransformGraph)</span><span class="sxs-lookup"><span data-stu-id="6584c-136">Initialize(ID2D1EffectContext \*pContextInternal, ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="6584c-137">[Direct2D](./direct2d-portal.md) chama o método [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) após o método [**ID2D1DeviceContext:: createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) ser chamado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6584c-137">[Direct2D](./direct2d-portal.md) calls the [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method after the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method has been called by the app.</span></span> <span data-ttu-id="6584c-138">Você pode usar esse método para executar a inicialização interna ou qualquer outra operação necessária para o efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-138">You can use this method to perform internal initialization or any other operations needed for the effect.</span></span> <span data-ttu-id="6584c-139">Além disso, você pode usá-lo para criar o grafo de transformação inicial do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-139">Additionally, you can use it to create the effect's initial transform graph.</span></span>

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a><span data-ttu-id="6584c-140">Setgraph (ID2D1TransformGraph \* pTransformGraph)</span><span class="sxs-lookup"><span data-stu-id="6584c-140">SetGraph(ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="6584c-141">[Direct2D](./direct2d-portal.md) chama o método [**setgraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) quando o número de entradas para o efeito é alterado.</span><span class="sxs-lookup"><span data-stu-id="6584c-141">[Direct2D](./direct2d-portal.md) calls the [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) method when the number of inputs to the effect is changed.</span></span> <span data-ttu-id="6584c-142">Embora a maioria dos efeitos tenha um número constante de entradas, outros, como o [efeito composto](composite.md) , dão suporte a um número variável de entradas.</span><span class="sxs-lookup"><span data-stu-id="6584c-142">While most effects have a constant number of inputs, others like the [Composite effect](composite.md) support a variable number of inputs.</span></span> <span data-ttu-id="6584c-143">Esse método permite que esses efeitos atualizem seu grafo de transformação em resposta a uma contagem de entrada variável.</span><span class="sxs-lookup"><span data-stu-id="6584c-143">This method allows these effects to update their transform graph in response to a changing input count.</span></span> <span data-ttu-id="6584c-144">Se um efeito não oferecer suporte a uma contagem de entrada de variável, esse método poderá simplesmente retornar E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6584c-144">If an effect does not support a variable input count, this method can simply return E\_NOTIMPL.</span></span>

### <a name="prepareforrender-d2d1_change_type-changetype"></a><span data-ttu-id="6584c-145">PrepareForRender (alteração de tipo de alteração de D2D1 \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="6584c-145">PrepareForRender (D2D1\_CHANGE\_TYPE changeType)</span></span>

<span data-ttu-id="6584c-146">O método [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) fornece uma oportunidade de efeitos para executar qualquer operação em resposta a alterações externas.</span><span class="sxs-lookup"><span data-stu-id="6584c-146">The [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method provides an opportunity for effects to perform any operations in response to external changes.</span></span> <span data-ttu-id="6584c-147">[Direct2D](./direct2d-portal.md) chama esse método logo antes de renderizar um efeito se pelo menos um deles for verdadeiro:</span><span class="sxs-lookup"><span data-stu-id="6584c-147">[Direct2D](./direct2d-portal.md) calls this method just before it renders an effect if at least one of these is true:</span></span>

-   <span data-ttu-id="6584c-148">O efeito foi inicializado anteriormente, mas ainda não foi desenhado.</span><span class="sxs-lookup"><span data-stu-id="6584c-148">The effect has been previously initialized but not yet drawn.</span></span>
-   <span data-ttu-id="6584c-149">Uma propriedade de efeito foi alterada desde a última chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="6584c-149">An effect property has changed since the last draw call.</span></span>
-   <span data-ttu-id="6584c-150">O estado do contexto de [Direct2D](./direct2d-portal.md) de chamada (como DPI) foi alterado desde a última chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="6584c-150">The state of the calling [Direct2D](./direct2d-portal.md) context (like DPI) has changed since the last draw call.</span></span>

### <a name="implement-the-effect-registration-and-callback-methods"></a><span data-ttu-id="6584c-151">Implementar os métodos de registro de efeito e de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="6584c-151">Implement the effect registration and callback methods</span></span>

<span data-ttu-id="6584c-152">Os aplicativos devem registrar efeitos com [Direct2D](./direct2d-portal.md) antes de instanciar.</span><span class="sxs-lookup"><span data-stu-id="6584c-152">Apps must register effects with [Direct2D](./direct2d-portal.md) before instantiating them.</span></span> <span data-ttu-id="6584c-153">Esse registro tem como escopo uma instância de uma fábrica Direct2D e deve ser repetido sempre que o aplicativo é executado.</span><span class="sxs-lookup"><span data-stu-id="6584c-153">This registration is scoped to an instance of a Direct2D factory, and must be repeated each time the app is run.</span></span> <span data-ttu-id="6584c-154">Para habilitar esse registro, um efeito personalizado define um GUID exclusivo, um método público que registra o efeito e um método de retorno de chamada privado que retorna uma instância do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-154">To enable this registration, a custom effect defines a unique GUID, a public method that registers the effect, and a private callback method that returns an instance of the effect.</span></span>

### <a name="define-a-guid"></a><span data-ttu-id="6584c-155">Definir um GUID</span><span class="sxs-lookup"><span data-stu-id="6584c-155">Define a GUID</span></span>

<span data-ttu-id="6584c-156">Você deve definir um GUID que identifique exclusivamente o efeito para o registro com [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6584c-156">You must define a GUID that uniquely identifies the effect for registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="6584c-157">O aplicativo usa o mesmo para identificar o efeito quando chama [**ID2D1DeviceContext:: createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span><span class="sxs-lookup"><span data-stu-id="6584c-157">The app uses the same to identify the effect when it calls [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span></span>

<span data-ttu-id="6584c-158">Esse código demonstra como definir tal GUID para um efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-158">This code demonstrates defining such a GUID for an effect.</span></span> <span data-ttu-id="6584c-159">Você deve criar seu próprio GUID exclusivo usando uma ferramenta de geração de GUID, como guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="6584c-159">You must create its own unique GUID using a GUID generation tool such as guidgen.exe.</span></span>


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a><span data-ttu-id="6584c-160">Definir um método de registro público</span><span class="sxs-lookup"><span data-stu-id="6584c-160">Define a public registration method</span></span>

<span data-ttu-id="6584c-161">Em seguida, defina um método público para o aplicativo chamar para registrar o efeito com [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6584c-161">Next, define a public method for the app to call to register the effect with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="6584c-162">Como o registro de efeito é específico de uma instância de uma fábrica Direct2D, o método aceita uma interface [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6584c-162">Because effect registration is specific to an instance of a Direct2D factory, the method accepts an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface as a parameter.</span></span> <span data-ttu-id="6584c-163">Para registrar o efeito, o método chama a API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) no parâmetro **ID2D1Factory1** .</span><span class="sxs-lookup"><span data-stu-id="6584c-163">To register the effect, the method then calls the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API on the **ID2D1Factory1** parameter.</span></span>

<span data-ttu-id="6584c-164">Essa API aceita uma cadeia de caracteres XML que descreve os metadados, as entradas e as propriedades do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-164">This API accepts an XML string that describes the metadata, inputs, and properties of the effect.</span></span> <span data-ttu-id="6584c-165">Os metadados para um efeito são apenas para fins informativos e podem ser consultados pelo aplicativo por meio da interface [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) .</span><span class="sxs-lookup"><span data-stu-id="6584c-165">The metadata for an effect is for informational purposes only, and can be queried by the app through the [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) interface.</span></span> <span data-ttu-id="6584c-166">Os dados de entrada e propriedade, por outro lado, são usados pelo [Direct2D](./direct2d-portal.md) e representam a funcionalidade do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-166">The input and property data, on the other hand, is used by [Direct2D](./direct2d-portal.md) and represents the effect's functionality.</span></span>

<span data-ttu-id="6584c-167">Uma cadeia de caracteres XML para um efeito de exemplo mínimo é mostrada aqui.</span><span class="sxs-lookup"><span data-stu-id="6584c-167">An XML string for a minimal sample effect is shown here.</span></span> <span data-ttu-id="6584c-168">A adição de propriedades personalizadas ao XML é abordada na seção Adicionando propriedades personalizadas a um efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-168">Adding custom properties to the XML is covered in the Adding custom properties to an effect section.</span></span>


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



### <a name="define-an-effect-factory-callback-method"></a><span data-ttu-id="6584c-169">Definir um método de retorno de chamada de fábrica de efeito</span><span class="sxs-lookup"><span data-stu-id="6584c-169">Define an effect factory callback method</span></span>

<span data-ttu-id="6584c-170">O efeito também deve fornecer um método de retorno de chamada privado que retorna uma instância do efeito por meio de um único \* \* parâmetro IUnknown.</span><span class="sxs-lookup"><span data-stu-id="6584c-170">The effect must also provide a private callback method that returns an instance of the effect through a single IUnknown\*\* parameter.</span></span> <span data-ttu-id="6584c-171">Um ponteiro para esse método é fornecido para [Direct2D](./direct2d-portal.md) quando o efeito é registrado por meio da API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) por meio do parâmetro de [**\_ \_ fábrica de efeito PD2D1**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .</span><span class="sxs-lookup"><span data-stu-id="6584c-171">A pointer to this method is provided to [Direct2D](./direct2d-portal.md) when the effect is registered via the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API through the [**PD2D1\_EFFECT\_FACTORY**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory)\\ parameter.</span></span>


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



### <a name="implement-the-iunknown-interface"></a><span data-ttu-id="6584c-172">Implementar a interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="6584c-172">Implement the IUnknown interface</span></span>

<span data-ttu-id="6584c-173">Por fim, o efeito deve implementar a interface IUnknown para compatibilidade com com.</span><span class="sxs-lookup"><span data-stu-id="6584c-173">Finally, the effect must implement the IUnknown interface for compatibility with COM.</span></span>

## <a name="creating-the-effects-transform-graph"></a><span data-ttu-id="6584c-174">Criando o grafo de transformação do efeito</span><span class="sxs-lookup"><span data-stu-id="6584c-174">Creating the effect's transform graph</span></span>

<span data-ttu-id="6584c-175">Um efeito pode usar várias transformações diferentes (operações de imagem individuais) para criar seu efeito de imagem desejado.</span><span class="sxs-lookup"><span data-stu-id="6584c-175">An effect can use several different transforms (individual image operations) to create its desired imaging effect.</span></span> <span data-ttu-id="6584c-176">Para controlar a ordem na qual essas transformações são aplicadas à imagem de entrada, o efeito as organiza em um grafo de transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-176">To control the order in which these transforms are applied to the input image, the effect arranges them into a transform graph.</span></span> <span data-ttu-id="6584c-177">Um grafo de transformação pode fazer uso dos efeitos e transformações incluídos no [Direct2D](./direct2d-portal.md) , bem como transformações personalizadas criadas pelo autor do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-177">A transform graph can make use of the effects and transforms included in [Direct2D](./direct2d-portal.md) as well as custom transforms created by the effect author.</span></span>

### <a name="using-transforms-included-with-direct2d"></a><span data-ttu-id="6584c-178">Usando transformações incluídas com Direct2D</span><span class="sxs-lookup"><span data-stu-id="6584c-178">Using transforms included with Direct2D</span></span>

<span data-ttu-id="6584c-179">Essas são as transformações mais comumente usadas fornecidas com [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6584c-179">These are the most commonly used transforms provided with [Direct2D](./direct2d-portal.md).</span></span>

-   <span data-ttu-id="6584c-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): essa transformação mistura um número arbitrário de entradas com base em uma descrição de mistura, consulte o [**tópico \_ \_ Descrição do d2d1 Blend**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) e o [exemplo de modos de efeito composto do Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) para obter exemplos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="6584c-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): This transform blends an arbitrary number of inputs together based on a blend description, see the [**D2D1\_BLEND\_DESCRIPTION**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) topic and the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) for blending examples.</span></span> <span data-ttu-id="6584c-181">Essa transformação é retornada pelo método [**ID2D1EffectContext:: CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .</span><span class="sxs-lookup"><span data-stu-id="6584c-181">This transform is returned by the [**ID2D1EffectContext::CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) method.</span></span>
-   <span data-ttu-id="6584c-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): essa transformação expande o tamanho de saída de uma imagem de acordo com o [**\_ \_ modo de extensão d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) especificado.</span><span class="sxs-lookup"><span data-stu-id="6584c-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): This transform expands an image's output size according to the [**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) specified.</span></span> <span data-ttu-id="6584c-183">Essa transformação é retornada pelo método [**ID2D1EffectContext:: CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .</span><span class="sxs-lookup"><span data-stu-id="6584c-183">This transform is returned by the [**ID2D1EffectContext::CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) method.</span></span>
-   <span data-ttu-id="6584c-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): essa transformação desloca (traduz) sua entrada por qualquer número inteiro de pixels.</span><span class="sxs-lookup"><span data-stu-id="6584c-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): This transform offsets (translates) its input by any whole number of pixels.</span></span> <span data-ttu-id="6584c-185">Essa transformação é retornada pelo método [**ID2D1EffectContext:: CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .</span><span class="sxs-lookup"><span data-stu-id="6584c-185">This transform is returned by the [**ID2D1EffectContext::CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) method.</span></span>
-   <span data-ttu-id="6584c-186">Qualquer efeito existente pode ser tratado como uma transformação para fins de transformação de criação de grafo usando o método [**ID2D1EffectContext:: CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .</span><span class="sxs-lookup"><span data-stu-id="6584c-186">Any existing effect can be treated as a transform for the purposes of transform graph creation by using the [**ID2D1EffectContext::CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) method.</span></span>

### <a name="creating-a-single-node-transform-graph"></a><span data-ttu-id="6584c-187">Criando um grafo de transformação de nó único</span><span class="sxs-lookup"><span data-stu-id="6584c-187">Creating a single-node transform graph</span></span>

<span data-ttu-id="6584c-188">Depois de criar uma transformação, a entrada do efeito precisa ser conectada à entrada da transformação e a saída da transformação precisa ser conectada à saída do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-188">Once you create a transform, the effect's input needs to be connected to the transform's input, and the transform's output needs to be connected to the effect's output.</span></span> <span data-ttu-id="6584c-189">Quando um efeito contém apenas uma única transformação, você pode usar o método [**ID2D1TransformGraph:: SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) para fazer isso facilmente.</span><span class="sxs-lookup"><span data-stu-id="6584c-189">When an effect only contains a single transform, you can use the [**ID2D1TransformGraph::SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) method to easily accomplish this.</span></span>

<span data-ttu-id="6584c-190">Você pode criar ou modificar uma transformação nos métodos [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) ou [**setgraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) do efeito usando o parâmetro ID2D1TransformGraph fornecido.</span><span class="sxs-lookup"><span data-stu-id="6584c-190">You can create or modify a transform in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) or [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) methods using the provided ID2D1TransformGraph parameter.</span></span> <span data-ttu-id="6584c-191">Se um efeito precisar fazer alterações no grafo de transformação em outro método em que esse parâmetro não esteja disponível, o efeito poderá salvar o parâmetro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) como uma variável de membro da classe e acessá-lo em outro lugar, como [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) ou um método de retorno de chamada de propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="6584c-191">If an effect needs to make changes to the transform graph in another method where this parameter is not available, the effect can save the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter as a member variable of the class and access it elsewhere, such as [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) or a custom property callback method.</span></span>

<span data-ttu-id="6584c-192">Um método de [**inicialização**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) de exemplo é mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="6584c-192">A sample [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method is shown here.</span></span> <span data-ttu-id="6584c-193">Esse método cria um grafo de transformação de nó único que desloca a imagem em 100 pixels em cada eixo.</span><span class="sxs-lookup"><span data-stu-id="6584c-193">This method creates a single-node transform graph that offsets the image by one hundred pixels in each axis.</span></span>


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



### <a name="creating-a-multi-node-transform-graph"></a><span data-ttu-id="6584c-194">Criando um grafo de transformação de vários nós</span><span class="sxs-lookup"><span data-stu-id="6584c-194">Creating a multi-node transform graph</span></span>

<span data-ttu-id="6584c-195">A adição de várias transformações ao grafo de transformação de um efeito permite que os efeitos realizem internamente várias operações de imagem que são apresentadas a um aplicativo como um único efeito unificado.</span><span class="sxs-lookup"><span data-stu-id="6584c-195">Adding multiple transforms to an effect's transform graph allows effects to internally perform multiple image operations that are presented to an app as a single unified effect.</span></span>

<span data-ttu-id="6584c-196">Conforme observado acima, o grafo de transformação do efeito pode ser editado em qualquer método de efeito usando o parâmetro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) recebido no método [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-196">As noted above, the effect's transform graph may be edited in any effect method using the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter received in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method.</span></span> <span data-ttu-id="6584c-197">As seguintes APIs na interface podem ser usadas para criar ou modificar o grafo de transformação de um efeito:</span><span class="sxs-lookup"><span data-stu-id="6584c-197">The following APIs on that interface can be used to create or modify an effect's transform graph:</span></span>

### <a name="addnodeid2d1transformnode-pnode"></a><span data-ttu-id="6584c-198">AddNode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="6584c-198">AddNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="6584c-199">O método [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , em vigor, ' registra ' a transformação com o efeito e deve ser chamada antes que a transformação possa ser usada com qualquer um dos outros métodos de transformação do grafo.</span><span class="sxs-lookup"><span data-stu-id="6584c-199">The [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) method, in effect, 'registers' the transform with the effect, and must be called before the transform can be used with any of the other transform graph methods.</span></span>

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a><span data-ttu-id="6584c-200">ConnectToEffectInput (UINT32 toEffectInputIndex, ID2D1TransformNode \* pNode, UINT32 toNodeInputIndex)</span><span class="sxs-lookup"><span data-stu-id="6584c-200">ConnectToEffectInput(UINT32 toEffectInputIndex, ID2D1TransformNode \*pNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="6584c-201">O método [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) conecta a entrada da imagem do efeito à entrada de uma transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-201">The [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) method connects the effect's image input to a transform's input.</span></span> <span data-ttu-id="6584c-202">A mesma entrada de efeito pode ser conectada a várias transformações.</span><span class="sxs-lookup"><span data-stu-id="6584c-202">The same effect input can be connected to multiple transforms.</span></span>

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a><span data-ttu-id="6584c-203">ConnectNode (ID2D1TransformNode \* pFromNode, ID2D1TransformNode \* PTONODE, UINT32 toNodeInputIndex)</span><span class="sxs-lookup"><span data-stu-id="6584c-203">ConnectNode(ID2D1TransformNode \*pFromNode, ID2D1TransformNode \*pToNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="6584c-204">O método [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) conecta a saída de uma transformação à entrada de outra transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-204">The [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) method connects a transform's output to another transform's input.</span></span> <span data-ttu-id="6584c-205">Uma saída de transformação pode ser conectada a várias transformações.</span><span class="sxs-lookup"><span data-stu-id="6584c-205">A transform output can be connected to multiple transforms.</span></span>

### <a name="setoutputnodeid2d1transformnode-pnode"></a><span data-ttu-id="6584c-206">SetOutputNode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="6584c-206">SetOutputNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="6584c-207">O método [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) conecta a saída de uma transformação à saída do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-207">The [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) method connects a transform's output to the effect's output.</span></span> <span data-ttu-id="6584c-208">Como um efeito tem apenas uma saída, apenas uma única transformação pode ser designada como ' nó de saída '.</span><span class="sxs-lookup"><span data-stu-id="6584c-208">Because an effect only has one output, only a single transform can be designated as the 'output node'.</span></span>

<span data-ttu-id="6584c-209">Esse código usa duas transformações separadas para criar um efeito unificado.</span><span class="sxs-lookup"><span data-stu-id="6584c-209">This code uses two separate transforms to create a unified effect.</span></span> <span data-ttu-id="6584c-210">Nesse caso, o efeito é uma sombra projetada traduzida.</span><span class="sxs-lookup"><span data-stu-id="6584c-210">In this case, the effect is a translated drop shadow.</span></span>


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



## <a name="adding-custom-properties-to-an-effect"></a><span data-ttu-id="6584c-211">Adicionando propriedades personalizadas a um efeito</span><span class="sxs-lookup"><span data-stu-id="6584c-211">Adding custom properties to an effect</span></span>

<span data-ttu-id="6584c-212">Os efeitos podem definir propriedades personalizadas que permitem que um aplicativo altere o comportamento do efeito durante o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6584c-212">Effects can define custom properties that allow an app to change the effect's behavior during runtime.</span></span> <span data-ttu-id="6584c-213">Há três etapas para definir uma propriedade para um efeito personalizado:</span><span class="sxs-lookup"><span data-stu-id="6584c-213">There are three steps to define a property for a custom effect:</span></span>

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a><span data-ttu-id="6584c-214">Adicionar os metadados de propriedade aos dados de registro do efeito</span><span class="sxs-lookup"><span data-stu-id="6584c-214">Add the property metadata to the effect's registration data</span></span>

### <a name="add-property-to-registration-xml"></a><span data-ttu-id="6584c-215">Adicionar Propriedade ao XML de registro</span><span class="sxs-lookup"><span data-stu-id="6584c-215">Add property to registration XML</span></span>

<span data-ttu-id="6584c-216">Você deve definir as propriedades de um efeito personalizado durante o registro inicial do efeito com [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6584c-216">You must define a custom effect's properties during the effect's initial registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="6584c-217">Primeiro, você deve atualizar o XML de registro do efeito em seu método de registro público com a nova propriedade:</span><span class="sxs-lookup"><span data-stu-id="6584c-217">First, you must update the effect's registration XML in its public registration method with the new property:</span></span>


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



<span data-ttu-id="6584c-218">Quando você define uma propriedade de efeito em XML, ela precisa de um nome, um tipo e um nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="6584c-218">When you define an effect property in XML, it needs a name, a type, and a display name.</span></span> <span data-ttu-id="6584c-219">O nome de exibição de uma propriedade, bem como os valores de categoria, autor e descrição do efeito geral podem e devem ser localizados.</span><span class="sxs-lookup"><span data-stu-id="6584c-219">A property's display name, as well as the overall effect's category, author, and description values can and should be localized.</span></span>

<span data-ttu-id="6584c-220">Para cada propriedade, um efeito pode opcionalmente especificar valores padrão, mínimo e máximo.</span><span class="sxs-lookup"><span data-stu-id="6584c-220">For each property, an effect can optionally specify default, min, and max values.</span></span> <span data-ttu-id="6584c-221">Esses valores são apenas para uso informativo.</span><span class="sxs-lookup"><span data-stu-id="6584c-221">These values are for informational use only.</span></span> <span data-ttu-id="6584c-222">Eles não são impostos pelo [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6584c-222">They are not enforced by [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="6584c-223">Cabe a você implementar qualquer lógica padrão/mín/máx especificada na própria classe de efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-223">It is up to you to implement any specified default/min/max logic in the effect class yourself.</span></span>

<span data-ttu-id="6584c-224">O valor de tipo listado no XML para a propriedade deve corresponder ao tipo de dados correspondente usado pelos métodos getter e setter da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6584c-224">The type value listed in the XML for the property must match the corresponding data type used by the property's getter and setter methods.</span></span> <span data-ttu-id="6584c-225">Valores XML correspondentes para cada tipo de dados são mostrados nesta tabela:</span><span class="sxs-lookup"><span data-stu-id="6584c-225">Corresponding XML values for each data type are shown in this table:</span></span>



| <span data-ttu-id="6584c-226">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6584c-226">Data type</span></span>                                                                                                                              | <span data-ttu-id="6584c-227">Valor XML correspondente</span><span class="sxs-lookup"><span data-stu-id="6584c-227">Corresponding XML value</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="6584c-228">PWSTR</span><span class="sxs-lookup"><span data-stu-id="6584c-228">PWSTR</span></span>                                                                                                                                  | <span data-ttu-id="6584c-229">string</span><span class="sxs-lookup"><span data-stu-id="6584c-229">string</span></span>                  |
| <span data-ttu-id="6584c-230">BOOL</span><span class="sxs-lookup"><span data-stu-id="6584c-230">BOOL</span></span>                                                                                                                                   | <span data-ttu-id="6584c-231">bool</span><span class="sxs-lookup"><span data-stu-id="6584c-231">bool</span></span>                    |
| <span data-ttu-id="6584c-232">UINT</span><span class="sxs-lookup"><span data-stu-id="6584c-232">UINT</span></span>                                                                                                                                   | <span data-ttu-id="6584c-233">uint32</span><span class="sxs-lookup"><span data-stu-id="6584c-233">uint32</span></span>                  |
| <span data-ttu-id="6584c-234">INT</span><span class="sxs-lookup"><span data-stu-id="6584c-234">INT</span></span>                                                                                                                                    | <span data-ttu-id="6584c-235">int32</span><span class="sxs-lookup"><span data-stu-id="6584c-235">int32</span></span>                   |
| <span data-ttu-id="6584c-236">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6584c-236">FLOAT</span></span>                                                                                                                                  | <span data-ttu-id="6584c-237">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6584c-237">float</span></span>                   |
| [<span data-ttu-id="6584c-238">**\_Vetor D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="6584c-238">**D2D\_VECTOR\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | <span data-ttu-id="6584c-239">vector2</span><span class="sxs-lookup"><span data-stu-id="6584c-239">vector2</span></span>                 |
| [<span data-ttu-id="6584c-240">**\_3F de vetor D2D \_**</span><span class="sxs-lookup"><span data-stu-id="6584c-240">**D2D\_VECTOR\_3F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | <span data-ttu-id="6584c-241">Vector3</span><span class="sxs-lookup"><span data-stu-id="6584c-241">vector3</span></span>                 |
| [<span data-ttu-id="6584c-242">**\_4F de vetor D2D \_**</span><span class="sxs-lookup"><span data-stu-id="6584c-242">**D2D\_VECTOR\_4F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | <span data-ttu-id="6584c-243">Vector4</span><span class="sxs-lookup"><span data-stu-id="6584c-243">vector4</span></span>                 |
| <span data-ttu-id="6584c-244">[**D2D \_ matriz \_ 3x2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span><span class="sxs-lookup"><span data-stu-id="6584c-244">[**D2D\_MATRIX\_3X2\_F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span></span> | <span data-ttu-id="6584c-245">matrix3x2</span><span class="sxs-lookup"><span data-stu-id="6584c-245">matrix3x2</span></span>               |
| [<span data-ttu-id="6584c-246">**D2D \_ matriz \_ 4x3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="6584c-246">**D2D\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | <span data-ttu-id="6584c-247">matrix4x3</span><span class="sxs-lookup"><span data-stu-id="6584c-247">matrix4x3</span></span>               |
| [<span data-ttu-id="6584c-248">**D2D \_ matriz \_ 4x4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="6584c-248">**D2D\_MATRIX\_4X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | <span data-ttu-id="6584c-249">matrix4x4</span><span class="sxs-lookup"><span data-stu-id="6584c-249">matrix4x4</span></span>               |
| [<span data-ttu-id="6584c-250">**D2D \_ matriz \_ 5X4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="6584c-250">**D2D\_MATRIX\_5X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | <span data-ttu-id="6584c-251">matrix5x4</span><span class="sxs-lookup"><span data-stu-id="6584c-251">matrix5x4</span></span>               |
| <span data-ttu-id="6584c-252">MINUCIOSA\[\]</span><span class="sxs-lookup"><span data-stu-id="6584c-252">BYTE\[\]</span></span>                                                                                                                               | <span data-ttu-id="6584c-253">blob</span><span class="sxs-lookup"><span data-stu-id="6584c-253">blob</span></span>                    |
| <span data-ttu-id="6584c-254">IUnknown\*</span><span class="sxs-lookup"><span data-stu-id="6584c-254">IUnknown\*</span></span>                                                                                                                             | <span data-ttu-id="6584c-255">IUnknown</span><span class="sxs-lookup"><span data-stu-id="6584c-255">iunknown</span></span>                |
| <span data-ttu-id="6584c-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span><span class="sxs-lookup"><span data-stu-id="6584c-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span></span>                                                                                       | <span data-ttu-id="6584c-257">colorcontext</span><span class="sxs-lookup"><span data-stu-id="6584c-257">colorcontext</span></span>            |
| <span data-ttu-id="6584c-258">CLSID</span><span class="sxs-lookup"><span data-stu-id="6584c-258">CLSID</span></span>                                                                                                                                  | <span data-ttu-id="6584c-259">clsid</span><span class="sxs-lookup"><span data-stu-id="6584c-259">clsid</span></span>                   |
| <span data-ttu-id="6584c-260">Enumeration ([**\_ \_ modo de interpolação d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span><span class="sxs-lookup"><span data-stu-id="6584c-260">Enumeration ([**D2D1\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span></span>                                                | <span data-ttu-id="6584c-261">enum</span><span class="sxs-lookup"><span data-stu-id="6584c-261">enum</span></span>                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a><span data-ttu-id="6584c-262">Mapear a nova propriedade para os métodos getter e setter</span><span class="sxs-lookup"><span data-stu-id="6584c-262">Map the new property to getter and setter methods</span></span>

<span data-ttu-id="6584c-263">Em seguida, o efeito deve mapear essa nova propriedade para os métodos getter e setter.</span><span class="sxs-lookup"><span data-stu-id="6584c-263">Next, the effect must map this new property to getter and setter methods.</span></span> <span data-ttu-id="6584c-264">Isso é feito por meio da matriz de [**\_ \_ Associação de propriedade d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) que é passada para o método [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .</span><span class="sxs-lookup"><span data-stu-id="6584c-264">This is done through the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array that is passed into the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method.</span></span>

<span data-ttu-id="6584c-265">A matriz de [**\_ \_ associação da propriedade d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) é parecida com esta:</span><span class="sxs-lookup"><span data-stu-id="6584c-265">The [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array looks like this:</span></span>


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



<span data-ttu-id="6584c-266">Depois de criar a matriz XML e bindings, passe-as para o método [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :</span><span class="sxs-lookup"><span data-stu-id="6584c-266">Once you create the XML and bindings array, pass them into the [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method:</span></span>


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



<span data-ttu-id="6584c-267">A \_ macro de associação de tipo de valor d2d1 requer que \_ \_ a classe de efeito herde de [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) antes de qualquer outra interface.</span><span class="sxs-lookup"><span data-stu-id="6584c-267">The D2D1\_VALUE\_TYPE\_BINDING macro requires the effect class to inherit from [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) before any other interface.</span></span>

<span data-ttu-id="6584c-268">As propriedades personalizadas de um efeito são indexadas na ordem em que são declaradas no XML e, uma vez criadas, podem ser acessadas pelo aplicativo usando os métodos [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) e [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) .</span><span class="sxs-lookup"><span data-stu-id="6584c-268">Custom properties for an effect are indexed in the order they are declared in the XML, and once created can be accessed by the app using the [**ID2D1Properties::SetValue**](id2d1properties-setvalue-overload.md) and [**ID2D1Properties::GetValue**](id2d1properties-getvalue-overload.md) methods.</span></span> <span data-ttu-id="6584c-269">Para sua conveniência, você pode criar uma enumeração pública que lista cada propriedade no arquivo de cabeçalho do efeito:</span><span class="sxs-lookup"><span data-stu-id="6584c-269">For convenience, you can create a public enumeration that lists each property in the effect's header file:</span></span>


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a><span data-ttu-id="6584c-270">Criar os métodos getter e setter para a propriedade</span><span class="sxs-lookup"><span data-stu-id="6584c-270">Create the getter and setter methods for the property</span></span>

<span data-ttu-id="6584c-271">A próxima etapa é criar os métodos getter e setter para a nova propriedade.</span><span class="sxs-lookup"><span data-stu-id="6584c-271">The next step is to create the getter and setter methods for the new property.</span></span> <span data-ttu-id="6584c-272">Os nomes dos métodos devem corresponder àqueles especificados na matriz de [**\_ \_ associação da propriedade d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) .</span><span class="sxs-lookup"><span data-stu-id="6584c-272">The names of the methods must match the ones specified in the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array.</span></span> <span data-ttu-id="6584c-273">Além disso, o tipo de propriedade especificado no XML do efeito deve corresponder ao tipo do parâmetro do método setter e ao valor de retorno do método getter.</span><span class="sxs-lookup"><span data-stu-id="6584c-273">In addition, the property type specified in the effect's XML must match the type of the setter method's parameter and the getter method's return value.</span></span>


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



### <a name="update-effects-transforms-in-response-to-property-change"></a><span data-ttu-id="6584c-274">Atualizar as transformações do efeito em resposta à alteração da propriedade</span><span class="sxs-lookup"><span data-stu-id="6584c-274">Update effect's transforms in response to property change</span></span>

<span data-ttu-id="6584c-275">Para realmente atualizar a saída da imagem de um efeito em resposta a uma alteração de propriedade, o efeito precisa alterar suas transformações subjacentes.</span><span class="sxs-lookup"><span data-stu-id="6584c-275">To actually update an effect's image output in response to a property change, the effect needs to change its underlying transforms.</span></span> <span data-ttu-id="6584c-276">Isso normalmente é feito no método [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) do efeito que o [Direct2D](./direct2d-portal.md) chama automaticamente quando uma das propriedades de um efeito é alterada.</span><span class="sxs-lookup"><span data-stu-id="6584c-276">This is typically done in the effect's [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method which [Direct2D](./direct2d-portal.md) automatically calls when one of an effect's properties has been changed.</span></span> <span data-ttu-id="6584c-277">No entanto, as transformações podem ser atualizadas em qualquer um dos métodos do efeito: como inicializar ou os métodos setter da Propriedade do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-277">However, transforms can be updated in any of the effect's methods: such as Initialize or the effect's property setter methods.</span></span>

<span data-ttu-id="6584c-278">Por exemplo, se um efeito contiver um [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) e quisesse modificar seu valor de deslocamento em resposta à propriedade de deslocamento do efeito que está sendo alterada, ele adicionaria o seguinte código em [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span><span class="sxs-lookup"><span data-stu-id="6584c-278">For example, if an effect contained an [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) and wanted to modify its offset value in response to the effect's Offset property being changed, it would add the following code in [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span></span>


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



## <a name="creating-a-custom-transform"></a><span data-ttu-id="6584c-279">Criando uma transformação personalizada</span><span class="sxs-lookup"><span data-stu-id="6584c-279">Creating a custom transform</span></span>

<span data-ttu-id="6584c-280">Para implementar operações de imagem além do que é fornecido no [Direct2D](./direct2d-portal.md), você deve implementar transformações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6584c-280">To implement image operations beyond what is provided in [Direct2D](./direct2d-portal.md), you must implement custom transforms.</span></span> <span data-ttu-id="6584c-281">As transformações personalizadas podem alterar arbitrariamente uma imagem de entrada por meio do uso de sombreadores HLSL personalizados.</span><span class="sxs-lookup"><span data-stu-id="6584c-281">Custom transforms can arbitrarily change an input image through the use of custom HLSL shaders.</span></span>

<span data-ttu-id="6584c-282">As transformações implementam uma das duas interfaces diferentes dependendo dos tipos de sombreadores que eles usam.</span><span class="sxs-lookup"><span data-stu-id="6584c-282">Transforms implement one of two different interfaces depending on the types of shaders they use.</span></span> <span data-ttu-id="6584c-283">As transformações que usam sombreadores de pixel e/ou vértice devem implementar [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), enquanto as transformações que usam sombreadores de computação devem implementar [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span><span class="sxs-lookup"><span data-stu-id="6584c-283">Transforms using pixel and/or vertex shaders must implement [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), while transforms using compute shaders must implement [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span></span> <span data-ttu-id="6584c-284">Essas interfaces herdam de [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="6584c-284">These interfaces both inherit from [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span> <span data-ttu-id="6584c-285">Esta seção se concentra na implementação da funcionalidade que é comum para ambos.</span><span class="sxs-lookup"><span data-stu-id="6584c-285">This section focuses on implementing the functionality that is common to both.</span></span>

<span data-ttu-id="6584c-286">A interface [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) tem quatro métodos para implementar:</span><span class="sxs-lookup"><span data-stu-id="6584c-286">The [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface has four methods to implement:</span></span>

### <a name="getinputcount"></a><span data-ttu-id="6584c-287">GetInputCount</span><span class="sxs-lookup"><span data-stu-id="6584c-287">GetInputCount</span></span>

<span data-ttu-id="6584c-288">Esse método retorna um inteiro que representa a contagem de entrada para a transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-288">This method returns an integer representing the input count for the transform.</span></span>


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a><span data-ttu-id="6584c-289">MapInputRectsToOutputRect</span><span class="sxs-lookup"><span data-stu-id="6584c-289">MapInputRectsToOutputRect</span></span>

<span data-ttu-id="6584c-290">[Direct2D](./direct2d-portal.md) chama o método [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) toda vez que a transformação é renderizada.</span><span class="sxs-lookup"><span data-stu-id="6584c-290">[Direct2D](./direct2d-portal.md) calls the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) method each time the transform is rendered.</span></span> <span data-ttu-id="6584c-291">Direct2D passa um retângulo que representa os limites de cada uma das entradas para a transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-291">Direct2D passes a rectangle representing the bounds of each of the inputs to the transform.</span></span> <span data-ttu-id="6584c-292">A transformação é então responsável pelo cálculo dos limites da imagem de saída.</span><span class="sxs-lookup"><span data-stu-id="6584c-292">The transform is then responsible for calculating the bounds of the output image.</span></span> <span data-ttu-id="6584c-293">O tamanho dos retângulos para todos os métodos nesta interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) são definidos em pixels, não DIPs.</span><span class="sxs-lookup"><span data-stu-id="6584c-293">The size of the rectangles for all the methods on this interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) are defined in pixels, not DIPs.</span></span>

<span data-ttu-id="6584c-294">Esse método também é responsável por calcular a região da saída que é opaca com base na lógica do seu sombreador e nas regiões opacas de cada entrada.</span><span class="sxs-lookup"><span data-stu-id="6584c-294">This method is also responsible for calculating the region of the output that is opaque based on the logic of its shader and the opaque regions of each input.</span></span> <span data-ttu-id="6584c-295">Uma região opaca de uma imagem é definida como aquela em que o canal alfa é ' 1 ' para todo o retângulo.</span><span class="sxs-lookup"><span data-stu-id="6584c-295">An opaque region of an image is defined as that where the alpha channel is '1' for the entirety of the rectangle.</span></span> <span data-ttu-id="6584c-296">Se não estiver claro se a saída de uma transformação é opaca, o retângulo opaco de saída deve ser definido como (0, 0, 0, 0) como um valor seguro.</span><span class="sxs-lookup"><span data-stu-id="6584c-296">If it is unclear whether a transform's output is opaque, the output opaque rectangle should be set to (0, 0, 0, 0) as a safe value.</span></span> <span data-ttu-id="6584c-297">O [Direct2D](./direct2d-portal.md) usa essas informações para executar otimizações de renderização com o conteúdo ' garantido opaco '.</span><span class="sxs-lookup"><span data-stu-id="6584c-297">[Direct2D](./direct2d-portal.md) uses this info to perform rendering optimizations with 'guaranteed opaque' content.</span></span> <span data-ttu-id="6584c-298">Se esse valor for impreciso, ele poderá resultar em renderização incorreta.</span><span class="sxs-lookup"><span data-stu-id="6584c-298">If this value is inaccurate, it can result in incorrect rendering.</span></span>

<span data-ttu-id="6584c-299">Você pode modificar o comportamento de renderização da transformação (conforme definido nas seções 6 a 8) durante esse método.</span><span class="sxs-lookup"><span data-stu-id="6584c-299">The you can modify the transform's rendering behavior (as defined in sections 6 through 8) during this method.</span></span> <span data-ttu-id="6584c-300">No entanto, não é possível modificar outras transformações no grafo de transformação ou o próprio layout do grafo aqui.</span><span class="sxs-lookup"><span data-stu-id="6584c-300">However, the you can't modify other transforms in the transform graph, or the graph layout itself here.</span></span>


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



<span data-ttu-id="6584c-301">Para obter um exemplo mais complexo, considere como uma operação de desfoque simples seria representada:</span><span class="sxs-lookup"><span data-stu-id="6584c-301">For a more complex example, consider how a simple blur operation would be represented:</span></span>

<span data-ttu-id="6584c-302">Se uma operação de desfoque usar um raio de 5 pixels, o tamanho do retângulo de saída deverá ser expandido em 5 pixels, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="6584c-302">If a blur operation uses a 5 pixel radius, the size of the output rectangle must expand by 5 pixels, as shown below.</span></span> <span data-ttu-id="6584c-303">Ao modificar as coordenadas do retângulo, uma transformação deve garantir que sua lógica não cause nenhum fluxo acima/estourado nas coordenadas do retângulo.</span><span class="sxs-lookup"><span data-stu-id="6584c-303">When modifying rectangle coordinates, a transform must ensure that its logic does not cause any over/underflows in the rectangle coordinates.</span></span>


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



<span data-ttu-id="6584c-304">Como a imagem está borrada, uma região da imagem opaca pode agora ser parcialmente transparente.</span><span class="sxs-lookup"><span data-stu-id="6584c-304">Because the image is blurred, a region of the image which was opaque may now be partially transparent.</span></span> <span data-ttu-id="6584c-305">Isso ocorre porque a área fora da imagem assume o padrão de preto transparente e essa transparência será mesclada na imagem ao lado das bordas.</span><span class="sxs-lookup"><span data-stu-id="6584c-305">This is because the area outside the image defaults to transparent black and this transparency will be blended into the image around the edges.</span></span> <span data-ttu-id="6584c-306">A transformação deve refletir isso em seus cálculos de retângulo opaco de saída:</span><span class="sxs-lookup"><span data-stu-id="6584c-306">The transform must reflect this in its output opaque rectangle calculations:</span></span>


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



<span data-ttu-id="6584c-307">Esses cálculos são visualizados aqui:</span><span class="sxs-lookup"><span data-stu-id="6584c-307">These calculations are visualized here:</span></span>

![ilustração de cálculo de retângulo.](images/custom-effects2.png)

<span data-ttu-id="6584c-309">Para obter mais informações sobre esse método, consulte a página de referência do [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .</span><span class="sxs-lookup"><span data-stu-id="6584c-309">For more info about this method, see the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) reference page.</span></span>

### <a name="mapoutputrecttoinputrects"></a><span data-ttu-id="6584c-310">MapOutputRectToInputRects</span><span class="sxs-lookup"><span data-stu-id="6584c-310">MapOutputRectToInputRects</span></span>

<span data-ttu-id="6584c-311">[Direct2D](./direct2d-portal.md) chama o método [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) após [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="6584c-311">[Direct2D](./direct2d-portal.md) calls the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) method after [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="6584c-312">A transformação deve calcular em qual parte da imagem ele precisa ler para processar corretamente a região de saída solicitada.</span><span class="sxs-lookup"><span data-stu-id="6584c-312">The transform must calculate what portion of the image it needs to read from in order to correctly render the requested output region.</span></span>

<span data-ttu-id="6584c-313">Como antes, se um efeito mapear estritamente pixels 1-1, ele poderá passar o retângulo de saída para o retângulo de entrada:</span><span class="sxs-lookup"><span data-stu-id="6584c-313">As before, if an effect strictly maps pixels 1-1, it can pass the output rectangle through to the input rectangle:</span></span>


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



<span data-ttu-id="6584c-314">Da mesma forma, se uma transformação reduzir ou expandir uma imagem (como o exemplo de desfoque aqui), os pixels geralmente usam pixels circundantes para calcular seu valor.</span><span class="sxs-lookup"><span data-stu-id="6584c-314">Likewise, if a transform shrinks or expands an image (like the blur example here), pixels often use surrounding pixels to calculate their value.</span></span> <span data-ttu-id="6584c-315">Com um desfoque, é feita a média de um pixel com seus pixels ao redor, mesmo que eles estejam fora dos limites da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="6584c-315">With a blur, a pixel is averaged with its surrounding pixels, even if they are outside of the bounds of the input image.</span></span> <span data-ttu-id="6584c-316">Esse comportamento é refletido no cálculo.</span><span class="sxs-lookup"><span data-stu-id="6584c-316">This behavior is reflected in the calculation.</span></span> <span data-ttu-id="6584c-317">Como antes, a transformação verifica se há estouros ao expandir as coordenadas de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="6584c-317">As before, the transform checks for overflows when expanding a rectangle's coordinates.</span></span>


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



<span data-ttu-id="6584c-318">Esta figura visualiza o cálculo.</span><span class="sxs-lookup"><span data-stu-id="6584c-318">This figure visualizes the calculation.</span></span> <span data-ttu-id="6584c-319">O [Direct2D](./direct2d-portal.md) automaticamente Obtém pixels pretos transparentes em que a imagem de entrada não existe, permitindo que o desfoque seja mesclado gradualmente com o conteúdo existente na tela.</span><span class="sxs-lookup"><span data-stu-id="6584c-319">[Direct2D](./direct2d-portal.md) automatically samples transparent black pixels where the input image doesn't exist, allowing the blur to be blended gradually with the existing content on the screen.</span></span>

![ilustração de um efeito de amostragem de pixels pretos transparentes fora de um retângulo.](images/custom-effects3.png)

<span data-ttu-id="6584c-321">Se o mapeamento não for trivial, esse método deverá definir o retângulo de entrada para a área máxima para garantir os resultados corretos.</span><span class="sxs-lookup"><span data-stu-id="6584c-321">If the mapping is non-trivial, then this method should set the input rectangle to the maximum area to guarantee correct results.</span></span> <span data-ttu-id="6584c-322">Para fazer isso, defina as bordas esquerda e superior como INT \_ min e as bordas direita e inferior como int \_ máx.</span><span class="sxs-lookup"><span data-stu-id="6584c-322">To do this, set the left and top edges to INT\_MIN, and the right and bottom edges to INT\_MAX.</span></span>

<span data-ttu-id="6584c-323">Para obter mais informações sobre esse método, consulte o tópico [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .</span><span class="sxs-lookup"><span data-stu-id="6584c-323">For more info about this method, see the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) topic.</span></span>

### <a name="mapinvalidrect"></a><span data-ttu-id="6584c-324">MapInvalidRect</span><span class="sxs-lookup"><span data-stu-id="6584c-324">MapInvalidRect</span></span>

<span data-ttu-id="6584c-325">[Direct2D](./direct2d-portal.md) também chama o método [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="6584c-325">[Direct2D](./direct2d-portal.md) also calls the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) method.</span></span> <span data-ttu-id="6584c-326">No entanto, ao contrário dos métodos [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) e [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) , não é garantido chamá-lo em um momento específico.</span><span class="sxs-lookup"><span data-stu-id="6584c-326">However, unlike the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) and [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) methods Direct2D is not guaranteed to call it at any particular time.</span></span> <span data-ttu-id="6584c-327">Esse método conceitualmente decide que parte da saída de uma transformação precisa ser renderizada novamente em resposta a parte ou a todas as suas alterações de entrada.</span><span class="sxs-lookup"><span data-stu-id="6584c-327">This method conceptually decides what part of a transform's output needs to be re-rendered in response to part or all of its input changing.</span></span> <span data-ttu-id="6584c-328">Há três cenários diferentes para os quais calcular o Rect inválido de uma transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-328">There are three different scenarios for which to calculate a transform's invalid rect.</span></span>

### <a name="transforms-with-one-to-one-pixel-mapping"></a><span data-ttu-id="6584c-329">Transformações com mapeamento de pixel de um para um</span><span class="sxs-lookup"><span data-stu-id="6584c-329">Transforms with one-to-one pixel mapping</span></span>

<span data-ttu-id="6584c-330">Para transformações que mapeiam os pixels 1-1, basta passar o retângulo de entrada inválido para o retângulo de saída inválido:</span><span class="sxs-lookup"><span data-stu-id="6584c-330">For transforms that map pixels 1-1, simply pass the invalid input rectangle through to the invalid output rectangle:</span></span>


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



### <a name="transforms-with-many-to-many-pixel-mapping"></a><span data-ttu-id="6584c-331">Transformações com mapeamento de pixel muitos para muitos</span><span class="sxs-lookup"><span data-stu-id="6584c-331">Transforms with many-to-many pixel mapping</span></span>

<span data-ttu-id="6584c-332">Quando os pixels de saída de uma transformação dependem de sua área ao redor, o retângulo de entrada inválido deve ser expandido de forma correspondente.</span><span class="sxs-lookup"><span data-stu-id="6584c-332">When a transform's output pixels are dependent on their surrounding area, the invalid input rectangle must correspondingly be expanded.</span></span> <span data-ttu-id="6584c-333">Isso é para refletir que os pixels que circundam o retângulo de entrada inválido também serão afetados e se tornarão inválidos.</span><span class="sxs-lookup"><span data-stu-id="6584c-333">This is to reflect that pixels surrounding the invalid input rectangle will also be affected and become invalid.</span></span> <span data-ttu-id="6584c-334">Por exemplo, um desfoque de cinco pixels usa o seguinte cálculo:</span><span class="sxs-lookup"><span data-stu-id="6584c-334">For example, a five pixel blur uses the following calculation:</span></span>


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a><span data-ttu-id="6584c-335">Transformações com mapeamento de pixel complexo</span><span class="sxs-lookup"><span data-stu-id="6584c-335">Transforms with complex pixel mapping</span></span>

<span data-ttu-id="6584c-336">Para transformações em que os pixels de entrada e saída não têm um mapeamento simples, toda a saída pode ser marcada como inválida.</span><span class="sxs-lookup"><span data-stu-id="6584c-336">For transforms where input and output pixels do not have a simple mapping, the entire output can be marked as invalid.</span></span> <span data-ttu-id="6584c-337">Por exemplo, se uma transformação simplesmente produzir a cor média da entrada, toda a saída da transformação será alterada se até mesmo uma pequena parte da entrada for alterada.</span><span class="sxs-lookup"><span data-stu-id="6584c-337">For example, if a transform simply outputs the average color of the input, the entire output of the transform changes if even a small part of the input is changed.</span></span> <span data-ttu-id="6584c-338">Nesse caso, o retângulo de saída inválido deve ser definido como um retângulo logicamente infinito (mostrado abaixo).</span><span class="sxs-lookup"><span data-stu-id="6584c-338">In this case, the invalid output rectangle should be set to a logically infinite rectangle (shown below).</span></span> <span data-ttu-id="6584c-339">[Direct2D](./direct2d-portal.md) coloca automaticamente os limites da saída.</span><span class="sxs-lookup"><span data-stu-id="6584c-339">[Direct2D](./direct2d-portal.md) automatically clamps this to the bounds of the output.</span></span>


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



<span data-ttu-id="6584c-340">Para obter mais informações sobre esse método, consulte o tópico [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="6584c-340">For more info about this method, see the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) topic.</span></span>

<span data-ttu-id="6584c-341">Depois que esses métodos forem implementados, o cabeçalho da transformação conterá o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6584c-341">Once these methods have been implemented, your transform's header will contain the following:</span></span>


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



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a><span data-ttu-id="6584c-342">Adicionando um sombreador de pixel a uma transformação personalizada</span><span class="sxs-lookup"><span data-stu-id="6584c-342">Adding a pixel shader to a custom transform</span></span>

<span data-ttu-id="6584c-343">Depois que uma transformação tiver sido criada, ela precisará fornecer um sombreador que manipulará os pixels da imagem.</span><span class="sxs-lookup"><span data-stu-id="6584c-343">Once a transform has been created, it needs to provide a shader that will manipulate the image pixels.</span></span> <span data-ttu-id="6584c-344">Esta seção aborda as etapas para usar um sombreador de pixel com uma transformação personalizada.</span><span class="sxs-lookup"><span data-stu-id="6584c-344">This section covers the steps to using a pixel shader with a custom transform.</span></span>

### <a name="implementing-id2d1drawtransform"></a><span data-ttu-id="6584c-345">Implementando ID2D1DrawTransform</span><span class="sxs-lookup"><span data-stu-id="6584c-345">Implementing ID2D1DrawTransform</span></span>

<span data-ttu-id="6584c-346">Para usar um sombreador de pixel, a transformação deve implementar a interface [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , que herda da interface [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) descrita na seção 5.</span><span class="sxs-lookup"><span data-stu-id="6584c-346">To use a pixel shader, the transform must implement the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, which inherits from the [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface described in section 5.</span></span> <span data-ttu-id="6584c-347">Essa interface contém um novo método para implementar:</span><span class="sxs-lookup"><span data-stu-id="6584c-347">This interface contains one new method to implement:</span></span>

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a><span data-ttu-id="6584c-348">SetDrawInfo (ID2D1DrawInfo \* pDrawInfo)</span><span class="sxs-lookup"><span data-stu-id="6584c-348">SetDrawInfo(ID2D1DrawInfo \*pDrawInfo)</span></span>

<span data-ttu-id="6584c-349">[Direct2D](./direct2d-portal.md) chama o método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) quando a transformação é adicionada pela primeira vez ao grafo de transformação de um efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-349">[Direct2D](./direct2d-portal.md) calls the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="6584c-350">Esse método fornece um parâmetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) que controla como a transformação é renderizada.</span><span class="sxs-lookup"><span data-stu-id="6584c-350">This method provides an [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="6584c-351">Consulte o tópico **ID2D1DrawInfo** para obter os métodos disponíveis aqui.</span><span class="sxs-lookup"><span data-stu-id="6584c-351">See the **ID2D1DrawInfo** topic for the methods available here.</span></span>

<span data-ttu-id="6584c-352">Se a transformação optar por armazenar esse parâmetro como uma variável de membro de classe, o objeto *drawInfo* poderá ser acessado e alterado de outros métodos, como setters de propriedade ou [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="6584c-352">If the transform chooses to store this parameter as a class member variable, the *drawInfo* object can be accessed and changed from other methods such as property setters or [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="6584c-353">Notavelmente, não pode ser chamado a partir dos métodos [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) ou [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) no [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="6584c-353">Notably, it cannot be called from the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) or [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods on [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span>

### <a name="creating-a-guid-for-the-pixel-shader"></a><span data-ttu-id="6584c-354">Criando um GUID para o sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="6584c-354">Creating a GUID for the pixel shader</span></span>

<span data-ttu-id="6584c-355">Em seguida, a transformação deve definir um GUID exclusivo para o sombreador de pixel em si.</span><span class="sxs-lookup"><span data-stu-id="6584c-355">Next, the transform must define a unique GUID for the pixel shader itself.</span></span> <span data-ttu-id="6584c-356">Isso é usado quando o [Direct2D](./direct2d-portal.md) carrega o sombreador na memória, bem como quando a transformação escolhe qual pixel shader usar para execução.</span><span class="sxs-lookup"><span data-stu-id="6584c-356">This is used when [Direct2D](./direct2d-portal.md) loads the shader into memory, as well as when the transform chooses which pixel shader to use for execution.</span></span> <span data-ttu-id="6584c-357">Ferramentas como guidgen.exe, que está incluído no Visual Studio, podem ser usadas para gerar um GUID aleatório.</span><span class="sxs-lookup"><span data-stu-id="6584c-357">Tools such as guidgen.exe, which is included with Visual Studio, can be used to generate a random GUID.</span></span>


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a><span data-ttu-id="6584c-358">Carregando o sombreador de pixel com Direct2D</span><span class="sxs-lookup"><span data-stu-id="6584c-358">Loading the pixel shader with Direct2D</span></span>

<span data-ttu-id="6584c-359">Um sombreador de pixel deve ser carregado na memória antes que possa ser usado pela transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-359">A pixel shader must be loaded into memory before it can be used by the transform.</span></span>

<span data-ttu-id="6584c-360">Para carregar o sombreador de pixel na memória, a transformação deve ler o código de byte do sombreador compilado do. Arquivo CSO gerado pelo Visual Studio (consulte a documentação do [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obter detalhes) em uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="6584c-360">To load the pixel shader into memory, the transform should read the compiled shader byte code from the .CSO file generated by Visual Studio (see [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details) into a byte array.</span></span> <span data-ttu-id="6584c-361">Essa técnica é demonstrada em detalhes no [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="6584c-361">This technique is demonstrated in detail in the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="6584c-362">Depois que os dados do sombreador tiverem sido carregados em uma matriz de bytes, chame o método [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) no objeto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-362">Once the shader data has been loaded into a byte array, call the [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) method on the effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object.</span></span> <span data-ttu-id="6584c-363">[Direct2D](./direct2d-portal.md) ignora as chamadas para **LoadPixelShader** quando um sombreador com o mesmo GUID já foi carregado.</span><span class="sxs-lookup"><span data-stu-id="6584c-363">[Direct2D](./direct2d-portal.md) ignores calls to **LoadPixelShader** when a shader with the same GUID has already been loaded.</span></span>

<span data-ttu-id="6584c-364">Depois que um sombreador de pixel é carregado na memória, a transformação precisa selecioná-lo para execução passando seu GUID para o método [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) no parâmetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fornecido durante o método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) .</span><span class="sxs-lookup"><span data-stu-id="6584c-364">After a pixel shader has been loaded into memory, the transform needs to select it for execution by passing its GUID to the [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided during the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="6584c-365">O sombreador de pixel já deve estar carregado na memória antes de ser selecionado para execução.</span><span class="sxs-lookup"><span data-stu-id="6584c-365">The pixel shader must be already loaded into memory before being selected for execution.</span></span>

### <a name="changing-shader-operation-with-constant-buffers"></a><span data-ttu-id="6584c-366">Alterando a operação do sombreador com buffers de constantes</span><span class="sxs-lookup"><span data-stu-id="6584c-366">Changing shader operation with constant buffers</span></span>

<span data-ttu-id="6584c-367">Para alterar a forma como um sombreador é executado, uma transformação pode passar um buffer constante para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6584c-367">To change how a shader executes, a transform may pass a constant buffer to the pixel shader.</span></span> <span data-ttu-id="6584c-368">Para fazer isso, uma transformação define uma struct que contém as variáveis desejadas no cabeçalho da classe:</span><span class="sxs-lookup"><span data-stu-id="6584c-368">To do so, a transform defines a struct that contains the desired variables in the class header:</span></span>


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



<span data-ttu-id="6584c-369">Em seguida, a transformação chama o método [**ID2D1DrawInfo:: SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) no parâmetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fornecido no método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) para passar esse buffer para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="6584c-369">The transform then calls the [**ID2D1DrawInfo::SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided in the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method to pass this buffer to the shader.</span></span>

<span data-ttu-id="6584c-370">O [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) também precisa definir uma struct correspondente que representa o buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="6584c-370">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) also needs to define a corresponding struct that represents the constant buffer.</span></span> <span data-ttu-id="6584c-371">As variáveis contidas no struct do sombreador devem corresponder às do struct da transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-371">The variables contained in the shader's struct must match those in the transform's struct.</span></span>


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



<span data-ttu-id="6584c-372">Depois que o buffer tiver sido definido, os valores contidos em podem ser lidos de qualquer lugar dentro do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6584c-372">Once the buffer has been defined, the values contained within can be read from anywhere within the pixel shader.</span></span>

### <a name="writing-a-pixel-shader-for-direct2d"></a><span data-ttu-id="6584c-373">Escrevendo um sombreador de pixel para Direct2D</span><span class="sxs-lookup"><span data-stu-id="6584c-373">Writing a pixel shader for Direct2D</span></span>

<span data-ttu-id="6584c-374">[Direct2D](./direct2d-portal.md) transformações de uso de sombreadores criados usando [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)padrão.</span><span class="sxs-lookup"><span data-stu-id="6584c-374">[Direct2D](./direct2d-portal.md) transforms use shaders authored using standard [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="6584c-375">No entanto, há alguns conceitos fundamentais para escrever um sombreador de pixel que é executado a partir do contexto de uma transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-375">However, there are a few key concepts to writing a pixel shader that executes from the context of a transform.</span></span> <span data-ttu-id="6584c-376">Para obter um exemplo completo de um sombreador de pixel totalmente funcional, consulte o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="6584c-376">For a completed example of a fully functionally pixel shader, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="6584c-377">O [Direct2D](./direct2d-portal.md) mapeia automaticamente as entradas de uma transformação para os objetos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**samplestate**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) no HLSL.</span><span class="sxs-lookup"><span data-stu-id="6584c-377">[Direct2D](./direct2d-portal.md) automatically maps a transform's inputs to [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) objects in the HLSL.</span></span> <span data-ttu-id="6584c-378">O primeiro **Texture2D** está localizado em Register T0, e o primeiro **samplestate** está localizado em Register S0.</span><span class="sxs-lookup"><span data-stu-id="6584c-378">The first **Texture2D** is located at register t0, and the first **SamplerState** is located at register s0.</span></span> <span data-ttu-id="6584c-379">Cada entrada adicional está localizada nos próximos registros correspondentes (T1 e S1, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="6584c-379">Each additional input is located at the next corresponding registers (t1 and s1 for example).</span></span> <span data-ttu-id="6584c-380">Os dados de pixel de uma determinada entrada podem ser amostrados chamando o exemplo no objeto **Texture2D** e passando o objeto de **amostrastate** correspondente e as coordenadas de Texel.</span><span class="sxs-lookup"><span data-stu-id="6584c-380">Pixel data for a particular input can be sampled by calling Sample on the **Texture2D** object and passing in the corresponding **SamplerState** object and the texel coordinates.</span></span>

<span data-ttu-id="6584c-381">Um sombreador de pixel personalizado é executado uma vez para cada pixel renderizado.</span><span class="sxs-lookup"><span data-stu-id="6584c-381">A custom pixel shader is run once for each pixel that is rendered.</span></span> <span data-ttu-id="6584c-382">Cada vez que o sombreador é executado, o [Direct2D](./direct2d-portal.md) fornece automaticamente três parâmetros que identificam sua posição de execução atual:</span><span class="sxs-lookup"><span data-stu-id="6584c-382">Each time the shader is run, [Direct2D](./direct2d-portal.md) automatically provides three parameters that identify its current execution position:</span></span>

-   <span data-ttu-id="6584c-383">Saída de espaço de cena: esse parâmetro representa a posição de execução atual em termos da superfície de destino geral.</span><span class="sxs-lookup"><span data-stu-id="6584c-383">Scene-space output: This parameter represents the current execution position in terms of the overall target surface.</span></span> <span data-ttu-id="6584c-384">Ele é definido em pixels e seus valores mínimo/máximo correspondem aos limites do retângulo retornado por [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="6584c-384">It is defined in pixels and its min/max values correspond to the bounds of the rectangle returned by [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span>
-   <span data-ttu-id="6584c-385">Saída de clip-Space: esse parâmetro é usado pelo Direct3D e não deve ser usado no sombreador de pixel de uma transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-385">Clip-space output: This parameter is used by Direct3D, and is must not be used in a transform's pixel shader.</span></span>
-   <span data-ttu-id="6584c-386">Texel-Space Input: esse parâmetro representa a posição de execução atual em uma textura de entrada específica.</span><span class="sxs-lookup"><span data-stu-id="6584c-386">Texel-space input: This parameter represents the current execution position in a particular input texture.</span></span> <span data-ttu-id="6584c-387">Um sombreador não deve assumir nenhuma dependência de como esse valor é calculado.</span><span class="sxs-lookup"><span data-stu-id="6584c-387">A shader should not take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="6584c-388">Ele só deve usá-lo para exemplificar a entrada do sombreador de pixel, conforme mostrado no código abaixo:</span><span class="sxs-lookup"><span data-stu-id="6584c-388">It should only use it to sample the pixel shader's input, as shown in the code below:</span></span>


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



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a><span data-ttu-id="6584c-389">Adicionando um sombreador de vértice a uma transformação personalizada</span><span class="sxs-lookup"><span data-stu-id="6584c-389">Adding a vertex shader to a custom transform</span></span>

<span data-ttu-id="6584c-390">Você pode usar sombreadores de vértice para realizar diferentes cenários de geração de imagens do que sombreadores de pixel.</span><span class="sxs-lookup"><span data-stu-id="6584c-390">You can use vertex shaders to accomplish different imaging scenarios than pixel shaders.</span></span> <span data-ttu-id="6584c-391">Em particular, os sombreadores de vértice podem executar efeitos de imagem baseados em geometria transformando vértices que compõem uma imagem.</span><span class="sxs-lookup"><span data-stu-id="6584c-391">In particular, vertex shaders can perform geometry-based image effects by transforming vertices that comprise an image.</span></span> <span data-ttu-id="6584c-392">Os sombreadores de vértice podem ser usados independentemente ou em conjunto com sombreadores de pixel especificados para transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-392">Vertex shaders can be used independently of or in conjunction with transform-specified pixel shaders.</span></span> <span data-ttu-id="6584c-393">Se um sombreador de vértice não for especificado, [Direct2D](./direct2d-portal.md) substituirá em um sombreador de vértice padrão para uso com o sombreador de pixel personalizado.</span><span class="sxs-lookup"><span data-stu-id="6584c-393">If a vertex shader is not specified, [Direct2D](./direct2d-portal.md) substitutes in a default vertex shader for use with the custom pixel shader.</span></span>

<span data-ttu-id="6584c-394">O processo para adicionar um sombreador de vértice a uma transformação personalizada é semelhante ao de um sombreador de pixel – a transformação implementa a interface [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , cria um GUID e (opcionalmente) passa buffers constantes para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="6584c-394">The process for adding a vertex shader to a custom transform is similar to that of a pixel shader – the transform implements the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, creates a GUID, and (optionally) passes constant buffers to the shader.</span></span> <span data-ttu-id="6584c-395">No entanto, há algumas etapas adicionais que são exclusivas de sombreadores de vértice:</span><span class="sxs-lookup"><span data-stu-id="6584c-395">However, there are a few key additional steps that are unique to vertex shaders:</span></span>

### <a name="creating-a-vertex-buffer"></a><span data-ttu-id="6584c-396">Criando um buffer de vértice</span><span class="sxs-lookup"><span data-stu-id="6584c-396">Creating a vertex buffer</span></span>

<span data-ttu-id="6584c-397">Um sombreador de vértice por definição é executado em vértices passados para ele, não para pixels individuais.</span><span class="sxs-lookup"><span data-stu-id="6584c-397">A vertex shader by definition executes on vertices passed to it, not individual pixels.</span></span> <span data-ttu-id="6584c-398">Para especificar os vértices em que o sombreador será executado, uma transformação cria um buffer de vértice para passar para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="6584c-398">To specify the vertices for the shader to execute on, a transform creates a vertex buffer to pass to the shader.</span></span> <span data-ttu-id="6584c-399">O layout dos buffers de vértice está além do escopo deste documento.</span><span class="sxs-lookup"><span data-stu-id="6584c-399">The layout of vertex buffers is beyond the scope of this document.</span></span> <span data-ttu-id="6584c-400">Consulte a [referência do Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obter detalhes ou o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obter uma implementação de exemplo.</span><span class="sxs-lookup"><span data-stu-id="6584c-400">Please see the [Direct3D reference](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) for details, or the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="6584c-401">Depois de criar um buffer de vértice na memória, a transformação usa o método [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) no objeto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) do efeito que o contém para passar os dados para a GPU.</span><span class="sxs-lookup"><span data-stu-id="6584c-401">After creating a vertex buffer in memory, the transform uses the [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) method on the containing effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object to pass that data to the GPU.</span></span> <span data-ttu-id="6584c-402">Novamente, consulte o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obter uma implementação de exemplo.</span><span class="sxs-lookup"><span data-stu-id="6584c-402">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="6584c-403">Se nenhum buffer de vértice for especificado pela transformação, [Direct2D](./direct2d-portal.md) passará um buffer de vértice padrão que representa o local da imagem retangular.</span><span class="sxs-lookup"><span data-stu-id="6584c-403">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) passes a default vertex buffer representing the rectangular image location.</span></span>

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a><span data-ttu-id="6584c-404">Alterando SetDrawInfo para utilizar um sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6584c-404">Changing SetDrawInfo to utilize a vertex shader</span></span>

<span data-ttu-id="6584c-405">Assim como com sombreadores de pixel, a transformação deve carregar e selecionar um sombreador de vértice para execução.</span><span class="sxs-lookup"><span data-stu-id="6584c-405">Like with pixel shaders, the transform must load and select a vertex shader for execution.</span></span> <span data-ttu-id="6584c-406">Para carregar o sombreador de vértice, ele chama o método [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) no método [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) recebido no método Initialize do efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-406">To load the vertex shader, it calls the [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) method on the [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) method received in the effect's Initialize method.</span></span> <span data-ttu-id="6584c-407">Para selecionar o sombreador de vértice para execução, ele chama [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) no parâmetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) recebido no método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) da transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-407">To select the vertex shader for execution, it calls [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter received in the transform's [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="6584c-408">Esse método aceita um GUID para um sombreador de vértices previamente carregado, bem como (opcionalmente) um buffer de vértice criado anteriormente para o sombreador a ser executado.</span><span class="sxs-lookup"><span data-stu-id="6584c-408">This method accepts a GUID for a previously-loaded vertex shader as well as (optionally) a previously-created vertex buffer for the shader to execute on.</span></span>

### <a name="implementing-a-direct2d-vertex-shader"></a><span data-ttu-id="6584c-409">Implementando um sombreador de vértice Direct2D</span><span class="sxs-lookup"><span data-stu-id="6584c-409">Implementing a Direct2D vertex shader</span></span>

<span data-ttu-id="6584c-410">Uma transformação de desenho pode conter um sombreador de pixel e um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="6584c-410">A draw transform can contain both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="6584c-411">Se uma transformação definir um sombreador de pixel e um sombreador de vértice, a saída do sombreador de vértice será fornecida diretamente ao sombreador de pixel: o aplicativo poderá personalizar a assinatura de retorno do sombreador de vértice/os parâmetros do sombreador de pixel, contanto que eles sejam consistentes.</span><span class="sxs-lookup"><span data-stu-id="6584c-411">If a transform defines both a pixel shader and a vertex shader, then the output from the vertex shader is given directly to the pixel shader: the app can customize the return signature of the vertex shader / the parameters of the pixel shader as long as they are consistent.</span></span>

<span data-ttu-id="6584c-412">Por outro lado, se uma transformação contiver apenas um sombreador de vértice e depender do sombreador de pixel de passagem padrão do [Direct2D](./direct2d-portal.md), ele deverá retornar a seguinte saída padrão:</span><span class="sxs-lookup"><span data-stu-id="6584c-412">On the other hand, if a transform only contains a vertex shader, and relies on [Direct2D](./direct2d-portal.md)'s default pass-through pixel shader, it must return the following default output:</span></span>


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="6584c-413">Um sombreador de vértice armazena o resultado de suas transformações de vértice na variável de saída do espaço de cena do sombreador.</span><span class="sxs-lookup"><span data-stu-id="6584c-413">A vertex shader stores the result of its vertex transformations in the shader's Scene-space output variable.</span></span> <span data-ttu-id="6584c-414">Para computar a saída do clipe e as variáveis de entrada de Texel, o [Direct2D](./direct2d-portal.md) fornece automaticamente matrizes de conversão em um buffer constante:</span><span class="sxs-lookup"><span data-stu-id="6584c-414">To compute the Clip-space output and the Texel-space input variables, [Direct2D](./direct2d-portal.md) automatically provides conversion matrices in a constant buffer:</span></span>


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



<span data-ttu-id="6584c-415">O código de sombreador de vértice de exemplo pode ser encontrado abaixo, que usa as matrizes de conversão para calcular o clipe correto e os espaços de Texel esperados pelo [Direct2D](./direct2d-portal.md):</span><span class="sxs-lookup"><span data-stu-id="6584c-415">Sample vertex shader code can be found below that uses the conversion matrices to calculate the correct clip and texel spaces expected by [Direct2D](./direct2d-portal.md):</span></span>


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



<span data-ttu-id="6584c-416">O código acima pode ser usado como um ponto de partida para um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="6584c-416">The above code can be used as a starting point for a vertex shader.</span></span> <span data-ttu-id="6584c-417">Ele simplesmente passa pela imagem de entrada sem executar nenhuma transformação.</span><span class="sxs-lookup"><span data-stu-id="6584c-417">It merely passes through the input image without performing any transforms.</span></span> <span data-ttu-id="6584c-418">Novamente, consulte o [exemplo do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para uma transformação baseada em sombreador de vértice totalmente implementada.</span><span class="sxs-lookup"><span data-stu-id="6584c-418">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a fully-implemented vertex shader-based transform.</span></span>

<span data-ttu-id="6584c-419">Se nenhum buffer de vértice for especificado pela transformação, o [Direct2D](./direct2d-portal.md) substituirá em um buffer de vértice padrão que representa o local da imagem retangular.</span><span class="sxs-lookup"><span data-stu-id="6584c-419">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) substitutes in a default vertex buffer representing the rectangular image location.</span></span> <span data-ttu-id="6584c-420">Os parâmetros para o sombreador de vértice são alterados para os da saída do sombreador padrão:</span><span class="sxs-lookup"><span data-stu-id="6584c-420">The parameters to the vertex shader are changed to those of the default shader output:</span></span>


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="6584c-421">O sombreador de vértice não pode modificar seus parâmetros *sceneSpaceOutput* e *clipSpaceOutput* .</span><span class="sxs-lookup"><span data-stu-id="6584c-421">The vertex shader may not modify its *sceneSpaceOutput* and *clipSpaceOutput* parameters.</span></span> <span data-ttu-id="6584c-422">Ele deve retorná-las inalteradas.</span><span class="sxs-lookup"><span data-stu-id="6584c-422">It must return them unchanged.</span></span> <span data-ttu-id="6584c-423">No entanto, pode modificar os parâmetros *texelSpaceInput* para cada imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="6584c-423">It may however modify the *texelSpaceInput* parameter(s) for each input image.</span></span> <span data-ttu-id="6584c-424">Se a transformação também contiver um sombreador de pixel personalizado, o sombreador de vértice ainda poderá passar parâmetros personalizados adicionais diretamente para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6584c-424">If the transform also contains a custom pixel shader, the vertex shader is still able to pass additional custom parameters directly to the pixel shader.</span></span> <span data-ttu-id="6584c-425">Além disso, o buffer personalizado das matrizes de conversão *sceneSpace* (B0) não é mais fornecido.</span><span class="sxs-lookup"><span data-stu-id="6584c-425">Additionally, the *sceneSpace* conversion matrices custom buffer (b0) is no longer provided.</span></span>

## <a name="adding-a-compute-shader-to-a-custom-transform"></a><span data-ttu-id="6584c-426">Adicionando um sombreador de computação a uma transformação personalizada</span><span class="sxs-lookup"><span data-stu-id="6584c-426">Adding a compute shader to a custom transform</span></span>

<span data-ttu-id="6584c-427">Por fim, as transformações personalizadas podem utilizar sombreadores de computação para determinados cenários de destino.</span><span class="sxs-lookup"><span data-stu-id="6584c-427">Finally, custom transforms may utilize compute shaders for certain targeted scenarios.</span></span> <span data-ttu-id="6584c-428">Os sombreadores de computação podem ser usados para implementar efeitos de imagem complexos que exigem acesso arbitrário aos buffers de imagem de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="6584c-428">Compute shaders can be used to implement complex image effects that require arbitrary access to input and output image buffers.</span></span> <span data-ttu-id="6584c-429">Por exemplo, um algoritmo de histograma básico não pode ser implementado com um sombreador de pixel devido a limitações no acesso à memória.</span><span class="sxs-lookup"><span data-stu-id="6584c-429">For example, a basic histogram algorithm cannot be implemented with a pixel shader due to limitations on memory access.</span></span>

<span data-ttu-id="6584c-430">Como os sombreadores de computação têm requisitos de nível de recursos de hardware mais altos que os sombreadores de pixel, os sombreadores de pixel devem ser usados quando possível para implementar um determinado efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-430">Because compute shaders have higher hardware feature level requirements than pixel shaders, pixel shaders should be used when possible to implement a given effect.</span></span> <span data-ttu-id="6584c-431">Especificamente, os sombreadores de computação só são executados na maioria dos cartões de nível DirectX 10 e superiores.</span><span class="sxs-lookup"><span data-stu-id="6584c-431">Specifically, compute shaders only run on most DirectX 10 level cards and higher.</span></span> <span data-ttu-id="6584c-432">Se uma transformação optar por usar um sombreador de computação, ela deverá verificar o suporte de hardware apropriado durante a instanciação, além da implementação da interface [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .</span><span class="sxs-lookup"><span data-stu-id="6584c-432">If a transform chooses to use a compute shader, it must check for the appropriate hardware support during instantiation in addition to implementing the [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) interface.</span></span>

### <a name="checking-for-compute-shader-support"></a><span data-ttu-id="6584c-433">Verificando o suporte ao sombreador de computação</span><span class="sxs-lookup"><span data-stu-id="6584c-433">Checking for Compute Shader support</span></span>

<span data-ttu-id="6584c-434">Se um efeito usar um sombreador de computação, ele deverá verificar o suporte ao sombreador de computação durante sua criação usando o método [**ID2D1EffectContext:: CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) .</span><span class="sxs-lookup"><span data-stu-id="6584c-434">If an effect uses a compute shader, it must check for compute shader support during its creation using the [**ID2D1EffectContext::CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) method.</span></span> <span data-ttu-id="6584c-435">Se a GPU não oferecer suporte a sombreadores de computação, o efeito deverá retornar [**D2DERR \_ \_ \_ recursos de dispositivo insuficientes**](direct2d-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6584c-435">If the GPU does not support compute shaders, the effect must return [**D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES**](direct2d-error-codes.md).</span></span>

<span data-ttu-id="6584c-436">Há dois tipos diferentes de sombreadores de computação que uma transformação pode usar: Shader Model 4 (DirectX 10) e Shader Model 5 (DirectX 11).</span><span class="sxs-lookup"><span data-stu-id="6584c-436">There are two different types of compute shaders that a transform can use: Shader Model 4 (DirectX 10) and Shader Model 5 (DirectX 11).</span></span> <span data-ttu-id="6584c-437">Há certas limitações para sombreadores do modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="6584c-437">There are certain limitations to Shader Model 4 shaders.</span></span> <span data-ttu-id="6584c-438">Consulte a documentação do [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6584c-438">See the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details.</span></span> <span data-ttu-id="6584c-439">As transformações podem conter os dois tipos de sombreadores e podem voltar para o modelo de sombreador 4 quando necessário: consulte a [amostra do SDK do D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para uma implementação disso.</span><span class="sxs-lookup"><span data-stu-id="6584c-439">Transforms can contain both types of shaders, and can fall back to Shader Model 4 when required: see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for an implementation of this.</span></span>

### <a name="implement-id2d1computetransform"></a><span data-ttu-id="6584c-440">Implementar ID2D1ComputeTransform</span><span class="sxs-lookup"><span data-stu-id="6584c-440">Implement ID2D1ComputeTransform</span></span>

<span data-ttu-id="6584c-441">Essa interface contém dois novos métodos para implementar além daqueles no [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="6584c-441">This interface contains two new methods to implement in addition to the ones in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span></span>

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a><span data-ttu-id="6584c-442">SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo)</span><span class="sxs-lookup"><span data-stu-id="6584c-442">SetComputeInfo(ID2D1ComputeInfo \*pComputeInfo)</span></span>

<span data-ttu-id="6584c-443">Assim como com sombreadores de pixel e Vertex, [Direct2D](./direct2d-portal.md) chama o método [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) quando a transformação é adicionada pela primeira vez ao grafo de transformação de um efeito.</span><span class="sxs-lookup"><span data-stu-id="6584c-443">Like with pixel and vertex shaders, [Direct2D](./direct2d-portal.md) calls the [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="6584c-444">Esse método fornece um parâmetro [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) que controla como a transformação é renderizada.</span><span class="sxs-lookup"><span data-stu-id="6584c-444">This method provides an [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="6584c-445">Isso inclui escolher o sombreador de computação a ser executado por meio do método [**ID2D1ComputeInfo:: SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) .</span><span class="sxs-lookup"><span data-stu-id="6584c-445">This includes choosing the compute shader to execute through the [**ID2D1ComputeInfo::SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) method.</span></span> <span data-ttu-id="6584c-446">Se a transformação optar por armazenar esse parâmetro como uma variável de membro de classe, ele poderá ser acessado e alterado de qualquer método de transformação ou efeito com a exceção dos métodos [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) e [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="6584c-446">If the transform chooses to store this parameter as a class member variable, it can be accessed and changed from any transform or effect method with the exception of the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) and [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods.</span></span> <span data-ttu-id="6584c-447">Consulte o tópico **ID2D1ComputeInfo** para ver outros métodos disponíveis aqui.</span><span class="sxs-lookup"><span data-stu-id="6584c-447">See the **ID2D1ComputeInfo** topic for other methods available here.</span></span>

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a><span data-ttu-id="6584c-448">CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect, UInt32 \* PDIMENSIONX, UInt32 \* pDimensionY, UInt32 \* pDimensionZ)</span><span class="sxs-lookup"><span data-stu-id="6584c-448">CalculateThreadgroups(ID2D1ComputeInfo \*pOutputRect, UINT32 \*pDimensionX, UINT32 \*pDimensionY, UINT32 \*pDimensionZ)</span></span>

<span data-ttu-id="6584c-449">Enquanto os sombreadores de pixel são executados em uma base por pixel e os sombreadores de vértice são executados por vértice, os sombreadores de computação são executados de acordo com a 'threadgroupidade.</span><span class="sxs-lookup"><span data-stu-id="6584c-449">Whereas pixel shaders are executed on a per-pixel basis and vertex shaders are executed on a per-vertex basis, compute shaders are executed on a per-'threadgroup' basis.</span></span> <span data-ttu-id="6584c-450">Um objectthread representa um número de threads que são executados simultaneamente na GPU.</span><span class="sxs-lookup"><span data-stu-id="6584c-450">A threadgroup represents a number of threads that execute concurrently on the GPU.</span></span> <span data-ttu-id="6584c-451">O código HLSL do sombreador de computação decide quantos threads devem ser executados por um thread.</span><span class="sxs-lookup"><span data-stu-id="6584c-451">The compute shader HLSL code decides how many threads should be executed per threadgroup.</span></span> <span data-ttu-id="6584c-452">O efeito dimensiona o número de threadgroups para que o sombreador execute o número desejado de vezes, dependendo da lógica do sombreador.</span><span class="sxs-lookup"><span data-stu-id="6584c-452">The effect scales the number of threadgroups so that the shader executes the desired number of times, depending on the shader's logic.</span></span>

<span data-ttu-id="6584c-453">O método [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) permite que a transformação informe ao [Direct2D](./direct2d-portal.md) quantos grupos de threads são necessários, com base no tamanho da imagem e no conhecimento próprio da transformação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="6584c-453">The [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) method allows the transform to inform [Direct2D](./direct2d-portal.md) how many thread groups are required, based on the size of the image and the transform's own knowledge of the shader.</span></span>

<span data-ttu-id="6584c-454">O número de vezes que o sombreador de computação é executado é um produto das contagens do The threadly especificado aqui e a anotação ' numthreads ' no [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="6584c-454">The number of times the compute shader is executed is a product of the threadgroup counts specified here and the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="6584c-455">Por exemplo, se a transformação definir as dimensões do grupos de threads como (2, 2, 1) o sombreador especificar (3, 3, 1) threads por thread, 4 threadgroups será executado, cada um com 9 threads, para um total de 36 instâncias de thread.</span><span class="sxs-lookup"><span data-stu-id="6584c-455">For example, if the transform sets the threadgroup dimensions to be (2,2,1) the shader specifies (3,3,1) threads per threadgroup, then 4 threadgroups will be executed, each with 9 threads in them, for a total of 36 thread instances.</span></span>

<span data-ttu-id="6584c-456">Um cenário comum é processar um pixel de saída para cada instância do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="6584c-456">A common scenario is to process one output pixel for each instance of the compute shader.</span></span> <span data-ttu-id="6584c-457">Para calcular o número de grupos de threads para esse cenário, a transformação divide a largura e a altura da imagem pelas respectivas dimensões x e y da anotação ' numthreads ' no sombreador de computação [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span><span class="sxs-lookup"><span data-stu-id="6584c-457">To calculate the number of thread groups for this scenario, the transform divides the width and height of the image by the respective x and y dimensions of the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span>

<span data-ttu-id="6584c-458">Importante, se essa divisão for executada, o número de grupos de threads solicitados deve sempre ser arredondado para o número inteiro mais próximo, caso contrário, os pixels ' resto ' não serão executados no.</span><span class="sxs-lookup"><span data-stu-id="6584c-458">Importantly, if this division is performed, then the number of thread groups requested must always be rounded up to the nearest integer, otherwise the 'remainder' pixels will not be executed upon.</span></span> <span data-ttu-id="6584c-459">Se um sombreador (por exemplo) computa um único pixel com cada thread, o código do método seria exibido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6584c-459">If a shader (for example) computes a single pixel with each thread, the method's code would appear as follows.</span></span>


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



<span data-ttu-id="6584c-460">O [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) usa o seguinte código para especificar o número de threads em cada grupo de threads:</span><span class="sxs-lookup"><span data-stu-id="6584c-460">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) uses the following code to specify the number of threads in each thread group:</span></span>


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



<span data-ttu-id="6584c-461">Durante a execução, o Current thread e o índice de thread atual são passados como parâmetros para o método Shader:</span><span class="sxs-lookup"><span data-stu-id="6584c-461">During execution, the current threadgroup and current thread index are passed as parameters to the shader method:</span></span>


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



### <a name="reading-image-data"></a><span data-ttu-id="6584c-462">Lendo dados da imagem</span><span class="sxs-lookup"><span data-stu-id="6584c-462">Reading image data</span></span>

<span data-ttu-id="6584c-463">Os sombreadores de computação acessam a imagem de entrada da transformação como uma única textura bidimensional:</span><span class="sxs-lookup"><span data-stu-id="6584c-463">Compute shaders access the transform's input image as a single two-dimensional texture:</span></span>


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



<span data-ttu-id="6584c-464">No entanto, como sombreadores de pixel, não há garantia de que os dados da imagem comecem em (0, 0) na textura.</span><span class="sxs-lookup"><span data-stu-id="6584c-464">However, like pixel shaders, the image's data is not guaranteed to begin at (0, 0) on the texture.</span></span> <span data-ttu-id="6584c-465">Em vez disso, o [Direct2D](./direct2d-portal.md) fornece constantes do sistema que permitem que os sombreadores compensam qualquer deslocamento:</span><span class="sxs-lookup"><span data-stu-id="6584c-465">Instead, [Direct2D](./direct2d-portal.md) provides system constants that allow shaders to compensate for any offset:</span></span>


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



<span data-ttu-id="6584c-466">Depois que o buffer constante acima e o método auxiliar tiverem sido definidos, o sombreador poderá obter amostras de dados de imagem usando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6584c-466">Once the above constant buffer and helper method have been defined, the shader can sample image data using the following:</span></span>


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



### <a name="writing-image-data"></a><span data-ttu-id="6584c-467">Gravando dados de imagem</span><span class="sxs-lookup"><span data-stu-id="6584c-467">Writing image data</span></span>

<span data-ttu-id="6584c-468">[Direct2D](./direct2d-portal.md) espera que um sombreador defina um buffer de saída para que a imagem resultante seja colocada.</span><span class="sxs-lookup"><span data-stu-id="6584c-468">[Direct2D](./direct2d-portal.md) expects a shader to define an output buffer for the resulting image to be placed.</span></span> <span data-ttu-id="6584c-469">No Shader Model 4 (DirectX 10), deve ser um buffer unidimensional devido a restrições de recurso:</span><span class="sxs-lookup"><span data-stu-id="6584c-469">In Shader Model 4 (DirectX 10), this must be a single-dimensional buffer due to feature constraints:</span></span>


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



<span data-ttu-id="6584c-470">A textura de saída é indexada na linha-primeiro para permitir que toda a imagem seja armazenada.</span><span class="sxs-lookup"><span data-stu-id="6584c-470">The output texture is indexed row-first to allow the entire image to be stored.</span></span>


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



<span data-ttu-id="6584c-471">Por outro lado, os sombreadores do modelo do sombreador 5 (DirectX 11) podem usar texturas de saída bidimensionais:</span><span class="sxs-lookup"><span data-stu-id="6584c-471">On the other hand, Shader Model 5 (DirectX 11) shaders can use two-dimensional output textures:</span></span>


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



<span data-ttu-id="6584c-472">Com sombreadores do modelo do sombreador 5, [Direct2D](./direct2d-portal.md) fornece um parâmetro "outputOffset" adicional no buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="6584c-472">With Shader Model 5 shaders, [Direct2D](./direct2d-portal.md) provides an additional 'outputOffset' parameter in the constant buffer.</span></span> <span data-ttu-id="6584c-473">A saída do sombreador deve ser offsettedda por esse valor:</span><span class="sxs-lookup"><span data-stu-id="6584c-473">The shader's output should be offsetted by this amount:</span></span>


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="6584c-474">Um sombreador de computação de modelo de sombreamento de passagem 5 concluído é mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="6584c-474">A completed pass-through Shader Model 5 compute shader is shown below.</span></span> <span data-ttu-id="6584c-475">Nele, cada um dos threads de sombreador de computação lê e grava um único pixel da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="6584c-475">In it, each of the compute shader threads reads and writes a single pixel of the input image.</span></span>


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



<span data-ttu-id="6584c-476">O código a seguir mostra a versão equivalente do modelo de sombreador 4 do sombreador.</span><span class="sxs-lookup"><span data-stu-id="6584c-476">The code below shows the equivalent Shader Model 4 version of the shader.</span></span> <span data-ttu-id="6584c-477">Observe que o sombreador agora é renderizado em um buffer de saída unidimensional.</span><span class="sxs-lookup"><span data-stu-id="6584c-477">Notice that the shader now renders into a single-dimensional output buffer.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6584c-478">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6584c-478">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6584c-479">Exemplo do SDK do D2DCustomEffects</span><span class="sxs-lookup"><span data-stu-id="6584c-479">D2DCustomEffects SDK sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 