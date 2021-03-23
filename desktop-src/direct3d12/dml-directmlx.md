---
title: DirectMLX
description: DirectMLX é uma biblioteca auxiliar somente de cabeçalho do C++ para DirectML, destinada a tornar mais fácil compor operadores individuais em grafos.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 8388edd51b6ad3ca30fe1c65947167cee7dac5e6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548335"
---
# <a name="directmlx"></a>DirectMLX

DirectMLX é uma biblioteca auxiliar somente de cabeçalho do C++ para DirectML, destinada a tornar mais fácil compor operadores individuais em grafos.

O DirectMLX fornece wrappers convenientes para todos os tipos de operador de DirectML (DML), bem como sobrecargas de operadores intuitivas, o que torna mais simples instanciar operadores DML e encadear em gráficos complexos.

## <a name="where-to-find-directmlxh"></a>Onde encontrar `DirectMLX.h`

`DirectMLX.h` é distribuído como software livre na licença do MIT. A versão mais recente pode ser encontrada no [GitHub do DirectML](https://github.com/microsoft/DirectML/tree/master/Libraries).

## <a name="tensor-constraints"></a>Restrições de tensor

DirectMLX requer DirectML versão 1.4.0 ou mais recente (consulte o [histórico de versão do DirectML](dml-version-history.md#version-table)). Não há suporte para versões mais antigas do DirectML.

DirectMLX. h requer um compilador com capacidade de C + +11, incluindo (mas não se limitando a):

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

Observe que um compilador C++ 17 (ou mais recente) é uma opção que recomendamos. A compilação para C++ 11 é possível, mas requer o uso de bibliotecas de terceiros (como [GSL](https://github.com/microsoft/GSL) e [Abseil](https://github.com/abseil/abseil-cpp)) para substituir a funcionalidade de biblioteca padrão ausente.

Se você tiver uma configuração que não pode ser compilada `DirectMLX.h` , registre [um problema em nosso GitHub](https://github.com/microsoft/DirectML/issues).

## <a name="basic-usage"></a>Uso básico

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Scope scope(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

Aqui está outro exemplo, que cria um grafo DirectML capaz de computar a [fórmula quadrática](https://en.wikipedia.org/wiki/Quadratic_formula).

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

dml::Scope scope(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(scope, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(scope, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a>Mais exemplos

Exemplos completos usando DirectMLX podem ser encontrados no [repositório GitHub do DirectML](https://github.com/microsoft/DirectML/tree/master/Samples).

## <a name="compile-time-options"></a>Opções de Compile-Time

O DirectMLX dá suporte a #define de tempo de compilação para personalizar várias partes do cabeçalho.

|Opção|Descrição|
|-|-|
|**DMLX_NO_EXCEPTIONS**|Se #define, isso fará com que os erros resultem em uma chamada para em `std::abort` vez de gerar uma exceção. Isso é definido por padrão se as exceções não estiverem disponíveis (por exemplo, se as exceções tiverem sido desabilitadas nas opções do compilador).|
|**DMLX_USE_WIL**|Se #define, as exceções serão geradas usando os tipos de exceção da [biblioteca de implementação do Windows](https://github.com/microsoft/wil) . Caso contrário, os tipos de exceção padrão (como `std::runtime_error` ) são usados em vez disso. Essa opção não terá efeito se **DMLX_NO_EXCEPTIONS** estiver definida.|
|**DMLX_USE_ABSEIL**|Se #define, o usará [Abseil](https://github.com/abseil/abseil-cpp) como substituições de colocação para tipos de biblioteca padrão não disponíveis no c++ 11. Esses tipos incluem `absl::optional` (em vez de `std::optional` ), `absl::Span` (em vez de `std::span` ) e `absl::InlinedVector` .|
|**DMLX_USE_GSL**|Controla se o [GSL](https://github.com/microsoft/GSL) deve ser usado como a substituição para `std::span` . Se #define, usos de `std::span` são substituídos por `gsl::span` em compiladores sem `std::span` implementações nativas. Caso contrário, uma implementação de drop-in embutido será fornecida em vez disso. Observe que essa opção só é usada durante a compilação em um compilador pre-C + 20 sem suporte para `std::span` e quando nenhuma outra substituição de biblioteca padrão suspensa (como Abseil) está em uso.|

## <a name="controlling-tensor-layout"></a>Controlando o layout tensor

Para a maioria dos operadores, DirectMLX computa as propriedades dos tempos de saída do operador em seu nome. Por exemplo, ao executar um `dml::Reduce` entre eixos `{ 0, 2, 3 }` com um tensor de entrada de tamanhos `{ 3, 4, 5, 6 }` , o DirectMLX calculará automaticamente as propriedades da saída tensor incluindo a forma correta de `{ 1, 4, 1, 1 }` .

No entanto, as outras propriedades de uma saída tensor incluem os *passos*, *TotalTensorSizeInBytes* e *GuaranteedBaseOffsetAlignment*. Por padrão, DirectMLX define essas propriedades de modo que o tensor não tenha nenhum efeito, nenhum alinhamento de deslocamento base garantido e um tamanho de tensor total em bytes, como computado por [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).

O DirectMLX dá suporte à capacidade de personalizar essas propriedades tensor de saída, usando objetos conhecidos como *políticas de tensor*. Um **TensorPolicy** é um retorno de chamada personalizável que é invocado pelo DirectMLX e retorna as propriedades tensor de saída, dado o tipo de dados, os sinalizadores e os tamanhos computados de tensor.

As políticas de tensor podem ser definidas no objeto **DML:: Scope** e serão usadas para todos os operadores subsequentes nesse grafo. As políticas de tensor também podem ser definidas diretamente ao construir um **TensorDesc**.

O layout dos tempos de vida produzidos por DirectMLX pode, portanto, ser controlado definindo um **TensorPolicy** que define os progressos adequados em seus tempos.

### <a name="example-1"></a>Exemplo 1

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

// Set the policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a>Exemplo 2

O DirectMLX também fornece algumas políticas de tensor alternativas internas. A política de **InterleavedChannel** , por exemplo, é fornecida como uma conveniência e pode ser usada para produzir muitos tempos com sobretensão, de forma que sejam escritas em ordem NHWC.

```cpp
// Set the InterleavedChannel policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>Confira também

* [GitHub DirectML](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [Exemplo de yolov4 de DirectMLX](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [Usando progressos para expressar o layout de enchimento e de memória](./dml-strides.md)
* [Estrutura de DML_GRAPH_DESC](./directml/ns-directml-dml_graph_desc.md)