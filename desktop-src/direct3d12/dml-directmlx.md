---
title: DirectMLX
description: DirectMLX é uma biblioteca auxiliar somente de cabeçalho do C++ para DirectML, destinada a tornar mais fácil compor operadores individuais em grafos.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: ba7eca27a39b690f678bdac1ea0feba1991e8b40
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521183"
---
# <a name="directmlx"></a><span data-ttu-id="28dee-103">DirectMLX</span><span class="sxs-lookup"><span data-stu-id="28dee-103">DirectMLX</span></span>

<span data-ttu-id="28dee-104">DirectMLX é uma biblioteca auxiliar somente de cabeçalho do C++ para DirectML, destinada a tornar mais fácil compor operadores individuais em grafos.</span><span class="sxs-lookup"><span data-stu-id="28dee-104">DirectMLX is a C++ header-only helper library for DirectML, intended to make it easier to compose individual operators into graphs.</span></span>

<span data-ttu-id="28dee-105">O DirectMLX fornece wrappers convenientes para todos os tipos de operador de DirectML (DML), bem como sobrecargas de operadores intuitivas, o que torna mais simples instanciar operadores DML e encadear em gráficos complexos.</span><span class="sxs-lookup"><span data-stu-id="28dee-105">DirectMLX provides convenient wrappers for all DirectML (DML) operator types, as well as intuitive operator overloads, which makes it simpler to instantiate DML operators, and chain them into complex graphs.</span></span>

## <a name="where-to-find-directmlxh"></a><span data-ttu-id="28dee-106">Onde encontrar `DirectMLX.h`</span><span class="sxs-lookup"><span data-stu-id="28dee-106">Where to find `DirectMLX.h`</span></span>

<span data-ttu-id="28dee-107">`DirectMLX.h` é distribuído como software livre na licença do MIT.</span><span class="sxs-lookup"><span data-stu-id="28dee-107">`DirectMLX.h` is distributed as open-source software under the MIT license.</span></span> <span data-ttu-id="28dee-108">A versão mais recente pode ser encontrada no [GitHub do DirectML](https://github.com/microsoft/DirectML/tree/master/Libraries).</span><span class="sxs-lookup"><span data-stu-id="28dee-108">The latest version can be found on the [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="28dee-109">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="28dee-109">Tensor constraints</span></span>

<span data-ttu-id="28dee-110">DirectMLX requer DirectML versão 1.4.0 ou mais recente (consulte o [histórico de versão do DirectML](dml-version-history.md#version-table)).</span><span class="sxs-lookup"><span data-stu-id="28dee-110">DirectMLX requires DirectML version 1.4.0, or newer (see [DirectML version history](dml-version-history.md#version-table)).</span></span> <span data-ttu-id="28dee-111">Não há suporte para versões mais antigas do DirectML.</span><span class="sxs-lookup"><span data-stu-id="28dee-111">Older versions of DirectML are not supported.</span></span>

<span data-ttu-id="28dee-112">DirectMLX. h requer um compilador com capacidade de C + +11, incluindo (mas não se limitando a):</span><span class="sxs-lookup"><span data-stu-id="28dee-112">DirectMLX.h requires a C++11-capable compiler, including (but not limited to):</span></span>

* <span data-ttu-id="28dee-113">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="28dee-113">Visual Studio 2017</span></span>
* <span data-ttu-id="28dee-114">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="28dee-114">Visual Studio 2019</span></span>
* <span data-ttu-id="28dee-115">Clang 10</span><span class="sxs-lookup"><span data-stu-id="28dee-115">Clang 10</span></span>

<span data-ttu-id="28dee-116">Observe que um compilador C++ 17 (ou mais recente) é a opção que recomendamos.</span><span class="sxs-lookup"><span data-stu-id="28dee-116">Note that a C++17 (or newer) compiler is the option that we recommend.</span></span> <span data-ttu-id="28dee-117">A compilação para C++ 11 é possível, mas requer o uso de bibliotecas de terceiros (como [GSL](https://github.com/microsoft/GSL) e [Abseil](https://github.com/abseil/abseil-cpp)) para substituir a funcionalidade de biblioteca padrão ausente.</span><span class="sxs-lookup"><span data-stu-id="28dee-117">Compiling for C++11 is possible, but it requires the use of third-party libraries (such as [GSL](https://github.com/microsoft/GSL) and [Abseil](https://github.com/abseil/abseil-cpp)) to replace missing standard library functionality.</span></span>

<span data-ttu-id="28dee-118">Se você tiver uma configuração que não pode ser compilada `DirectMLX.h` , registre [um problema em nosso GitHub](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="28dee-118">If you have a configuration that fails to compile `DirectMLX.h`, then please [file an issue on our GitHub](https://github.com/microsoft/DirectML/issues).</span></span>

## <a name="basic-usage"></a><span data-ttu-id="28dee-119">Uso básico</span><span class="sxs-lookup"><span data-stu-id="28dee-119">Basic usage</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Graph graph(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

<span data-ttu-id="28dee-120">Aqui está outro exemplo, que cria um grafo DirectML capaz de computar a [fórmula quadrática](https://en.wikipedia.org/wiki/Quadratic_formula).</span><span class="sxs-lookup"><span data-stu-id="28dee-120">Here's another example, which creates a DirectML graph capable of computing the [quadratic formula](https://en.wikipedia.org/wiki/Quadratic_formula).</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

std::pair<dml::Expression, dml::Expression>
    QuadraticFormula(dml::Expression a, dml::Expression b, dml::Expression c)
{
    // Quadratic formula: given an equation of the form ax^2 + bx + c = 0, x can be found by:
    //   x = -b +/- sqrt(b^2 - 4ac) / (2a)
    // https://en.wikipedia.org/wiki/Quadratic_formula

    // Note: DirectMLX provides operator overloads for common mathematical expressions. So for 
    // example a*c is equivalent to dml::Multiply(a, c).
    auto x1 = -b + dml::Sqrt(b*b - 4*a*c) / (2*a);
    auto x2 = -b - dml::Sqrt(b*b - 4*a*c) / (2*a);

    return { x1, x2 };
}

/* ... */

dml::Graph graph(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(graph, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(graph, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a><span data-ttu-id="28dee-121">Mais exemplos</span><span class="sxs-lookup"><span data-stu-id="28dee-121">More examples</span></span>

<span data-ttu-id="28dee-122">Exemplos completos usando DirectMLX podem ser encontrados no [repositório GitHub do DirectML](https://github.com/microsoft/DirectML/tree/master/Samples).</span><span class="sxs-lookup"><span data-stu-id="28dee-122">Complete samples using DirectMLX can be found on the [DirectML GitHub repo](https://github.com/microsoft/DirectML/tree/master/Samples).</span></span>

## <a name="compile-time-options"></a><span data-ttu-id="28dee-123">Opções de tempo de compilação</span><span class="sxs-lookup"><span data-stu-id="28dee-123">Compile-time options</span></span>

<span data-ttu-id="28dee-124">O DirectMLX dá suporte a #define de tempo de compilação para personalizar várias partes do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="28dee-124">DirectMLX supports compile-time #define's to customize various parts of the header.</span></span>

|<span data-ttu-id="28dee-125">Opção</span><span class="sxs-lookup"><span data-stu-id="28dee-125">Option</span></span>|<span data-ttu-id="28dee-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="28dee-126">Description</span></span>|
|-|-|
|<span data-ttu-id="28dee-127">**DMLX_NO_EXCEPTIONS**</span><span class="sxs-lookup"><span data-stu-id="28dee-127">**DMLX_NO_EXCEPTIONS**</span></span>|<span data-ttu-id="28dee-128">Se #define, isso fará com que os erros resultem em uma chamada para em `std::abort` vez de gerar uma exceção.</span><span class="sxs-lookup"><span data-stu-id="28dee-128">If #define'd, causes errors to result in a call to `std::abort` rather than throwing an exception.</span></span> <span data-ttu-id="28dee-129">Isso é definido por padrão se as exceções não estiverem disponíveis (por exemplo, se as exceções tiverem sido desabilitadas nas opções do compilador).</span><span class="sxs-lookup"><span data-stu-id="28dee-129">This is defined by default if exceptions are unavailable (for example, if exceptions have been disabled in the compiler options).</span></span>|
|<span data-ttu-id="28dee-130">**DMLX_USE_WIL**</span><span class="sxs-lookup"><span data-stu-id="28dee-130">**DMLX_USE_WIL**</span></span>|<span data-ttu-id="28dee-131">Se #define, as exceções serão geradas usando os tipos de exceção da [biblioteca de implementação do Windows](https://github.com/microsoft/wil) .</span><span class="sxs-lookup"><span data-stu-id="28dee-131">If #define'd, exceptions are thrown using [Windows Implementation Library](https://github.com/microsoft/wil) exception types.</span></span> <span data-ttu-id="28dee-132">Caso contrário, os tipos de exceção padrão (como `std::runtime_error` ) são usados em vez disso.</span><span class="sxs-lookup"><span data-stu-id="28dee-132">Otherwise, standard exception types (such as `std::runtime_error`) are used instead.</span></span> <span data-ttu-id="28dee-133">Essa opção não terá efeito se **DMLX_NO_EXCEPTIONS** estiver definida.</span><span class="sxs-lookup"><span data-stu-id="28dee-133">This option has no effect if **DMLX_NO_EXCEPTIONS** is defined.</span></span>|
|<span data-ttu-id="28dee-134">**DMLX_USE_ABSEIL**</span><span class="sxs-lookup"><span data-stu-id="28dee-134">**DMLX_USE_ABSEIL**</span></span>|<span data-ttu-id="28dee-135">Se #define, o usará [Abseil](https://github.com/abseil/abseil-cpp) como substituições de colocação para tipos de biblioteca padrão não disponíveis no c++ 11.</span><span class="sxs-lookup"><span data-stu-id="28dee-135">If #define'd, uses [Abseil](https://github.com/abseil/abseil-cpp) as drop-in replacements for standard library types unavailable in C++11.</span></span> <span data-ttu-id="28dee-136">Esses tipos incluem `absl::optional` (em vez de `std::optional` ), `absl::Span` (em vez de `std::span` ) e `absl::InlinedVector` .</span><span class="sxs-lookup"><span data-stu-id="28dee-136">These types include `absl::optional` (in place of `std::optional`), `absl::Span` (in place of `std::span`), and `absl::InlinedVector`.</span></span>|
|<span data-ttu-id="28dee-137">**DMLX_USE_GSL**</span><span class="sxs-lookup"><span data-stu-id="28dee-137">**DMLX_USE_GSL**</span></span>|<span data-ttu-id="28dee-138">Controla se o [GSL](https://github.com/microsoft/GSL) deve ser usado como a substituição para `std::span` .</span><span class="sxs-lookup"><span data-stu-id="28dee-138">Controls whether to use [GSL](https://github.com/microsoft/GSL) as the replacement for `std::span`.</span></span> <span data-ttu-id="28dee-139">Se #define, usos de `std::span` são substituídos por `gsl::span` em compiladores sem `std::span` implementações nativas.</span><span class="sxs-lookup"><span data-stu-id="28dee-139">If #define'd, uses of `std::span` are replaced by `gsl::span` on compilers without native `std::span` implementations.</span></span> <span data-ttu-id="28dee-140">Caso contrário, uma implementação de drop-in embutido será fornecida em vez disso.</span><span class="sxs-lookup"><span data-stu-id="28dee-140">Otherwise, an inline drop-in implementation is provided instead.</span></span> <span data-ttu-id="28dee-141">Observe que essa opção só é usada durante a compilação em um compilador pre-C + 20 sem suporte para `std::span` e quando nenhuma outra substituição de biblioteca padrão suspensa (como Abseil) está em uso.</span><span class="sxs-lookup"><span data-stu-id="28dee-141">Note that this option is only used when compiling on a pre-C++20 compiler without support for `std::span`, and when no other drop-in standard library replacement (like Abseil) is in use.</span></span>|

## <a name="controlling-tensor-layout"></a><span data-ttu-id="28dee-142">Controlando o layout tensor</span><span class="sxs-lookup"><span data-stu-id="28dee-142">Controlling tensor layout</span></span>

<span data-ttu-id="28dee-143">Para a maioria dos operadores, DirectMLX computa as propriedades dos tempos de saída do operador em seu nome.</span><span class="sxs-lookup"><span data-stu-id="28dee-143">For most operators, DirectMLX computes the properties of the operator's output tensors on your behalf.</span></span> <span data-ttu-id="28dee-144">Por exemplo, ao executar um `dml::Reduce` entre eixos `{ 0, 2, 3 }` com um tensor de entrada de tamanhos `{ 3, 4, 5, 6 }` , o DirectMLX calculará automaticamente as propriedades da saída tensor incluindo a forma correta de `{ 1, 4, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="28dee-144">For example when performing a `dml::Reduce` across axes `{ 0, 2, 3 }` with an input tensor of sizes `{ 3, 4, 5, 6 }`, DirectMLX will automatically compute the properties of the output tensor including the correct shape of `{ 1, 4, 1, 1 }`.</span></span>

<span data-ttu-id="28dee-145">No entanto, as outras propriedades de uma saída tensor incluem os *passos*, *TotalTensorSizeInBytes* e *GuaranteedBaseOffsetAlignment*.</span><span class="sxs-lookup"><span data-stu-id="28dee-145">However, the other properties of an output tensor include the *Strides*, *TotalTensorSizeInBytes*, and *GuaranteedBaseOffsetAlignment*.</span></span> <span data-ttu-id="28dee-146">Por padrão, DirectMLX define essas propriedades de modo que o tensor não tenha nenhum efeito, nenhum alinhamento de deslocamento base garantido e um tamanho de tensor total em bytes, como computado por [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span><span class="sxs-lookup"><span data-stu-id="28dee-146">By default, DirectMLX sets these properties such that the tensor has no striding, no guaranteed base offset alignment, and a total tensor size in bytes as computed by [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span></span>

<span data-ttu-id="28dee-147">O DirectMLX dá suporte à capacidade de personalizar essas propriedades tensor de saída, usando objetos conhecidos como *políticas de tensor*.</span><span class="sxs-lookup"><span data-stu-id="28dee-147">DirectMLX supports the ability to customize these output tensor properties, using objects known as *tensor policies*.</span></span> <span data-ttu-id="28dee-148">Um **TensorPolicy** é um retorno de chamada personalizável que é invocado pelo DirectMLX e retorna as propriedades tensor de saída, dado o tipo de dados, os sinalizadores e os tamanhos computados de tensor.</span><span class="sxs-lookup"><span data-stu-id="28dee-148">A **TensorPolicy** is a customizable callback that is invoked by DirectMLX, and returns output tensor properties given a tensor's computed data type, flags, and sizes.</span></span>

<span data-ttu-id="28dee-149">As políticas de tensor podem ser definidas no objeto **DML:: Graph** e serão usadas para todos os operadores subsequentes nesse grafo.</span><span class="sxs-lookup"><span data-stu-id="28dee-149">Tensor policies can be set on the **dml::Graph** object, and will be used for all subsequent operators on that graph.</span></span> <span data-ttu-id="28dee-150">As políticas de tensor também podem ser definidas diretamente ao construir um **TensorDesc**.</span><span class="sxs-lookup"><span data-stu-id="28dee-150">Tensor policies can also be set directly when constructing a **TensorDesc**.</span></span>

<span data-ttu-id="28dee-151">O layout dos tempos de vida produzidos por DirectMLX pode, portanto, ser controlado definindo um **TensorPolicy** que define os progressos adequados em seus tempos.</span><span class="sxs-lookup"><span data-stu-id="28dee-151">The layout of tensors produced by DirectMLX can therefore be controlled by setting a **TensorPolicy** that sets the appropriate strides on its tensors.</span></span>

### <a name="example-1"></a><span data-ttu-id="28dee-152">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28dee-152">Example 1</span></span>

```cpp
// Define a policy, which is a function that returns a TensorProperties given a data type,
// flags, and sizes.
dml::TensorProperties MyCustomPolicy(
    DML_TENSOR_DATA_TYPE dataType,
    DML_TENSOR_FLAGS flags,
    Span<const uint32_t> sizes)
{
    // Compute your custom strides, total tensor size in bytes, and guaranteed base
    // offset alignment
    dml::TensorProperties props;
    props.strides = /* ... */;
    props.totalTensorSizeInBytes = /* ... */;
    props.guaranteedBaseOffsetAlignment = /* ... */;
    return props;
};

// Set the policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a><span data-ttu-id="28dee-153">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28dee-153">Example 2</span></span>

<span data-ttu-id="28dee-154">O DirectMLX também fornece algumas políticas de tensor alternativas internas.</span><span class="sxs-lookup"><span data-stu-id="28dee-154">DirectMLX also provides some alternative tensor policies built-in.</span></span> <span data-ttu-id="28dee-155">A política de **InterleavedChannel** , por exemplo, é fornecida como uma conveniência e pode ser usada para produzir muitos tempos com sobretensão, de forma que sejam escritas em ordem NHWC.</span><span class="sxs-lookup"><span data-stu-id="28dee-155">The **InterleavedChannel** policy, for example, is provided as a convenience, and it can be used to produce tensors with strides such that they are written in NHWC order.</span></span>

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a><span data-ttu-id="28dee-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="28dee-156">See also</span></span>

* [<span data-ttu-id="28dee-157">GitHub DirectML</span><span class="sxs-lookup"><span data-stu-id="28dee-157">DirectML GitHub</span></span>](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [<span data-ttu-id="28dee-158">Exemplo de yolov4 de DirectMLX</span><span class="sxs-lookup"><span data-stu-id="28dee-158">DirectMLX yolov4 sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [<span data-ttu-id="28dee-159">Usando progressos para expressar o layout de enchimento e de memória</span><span class="sxs-lookup"><span data-stu-id="28dee-159">Using strides to express padding and memory layout</span></span>](./dml-strides.md)
* [<span data-ttu-id="28dee-160">Estrutura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="28dee-160">DML_GRAPH_DESC structure</span></span>](/windows/win32/api/directml/ns-directml-dml_graph_desc)