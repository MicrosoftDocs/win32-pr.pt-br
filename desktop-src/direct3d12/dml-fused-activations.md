---
title: Usando operadores com fusível para melhorar o desempenho
description: Alguns operadores DirectML dão suporte a um conceito conhecido como *Fusion*. O operador Fusion é uma maneira de melhorar o desempenho mesclando um operador (normalmente, uma função de ativação) em um operador diferente para que eles sejam executados juntos sem a necessidade de uma viagem de ida e volta à memória.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: b692727d52e252bb3752573e692bcf5beda794e2
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548336"
---
# <a name="using-fused-operators-to-improve-performance"></a><span data-ttu-id="1fcdb-104">Usando operadores com fusível para melhorar o desempenho</span><span class="sxs-lookup"><span data-stu-id="1fcdb-104">Using fused operators to improve performance</span></span>

<span data-ttu-id="1fcdb-105">Alguns operadores DirectML dão suporte a um conceito conhecido como *Fusion*.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-105">Some DirectML operators support a concept known as *fusion*.</span></span> <span data-ttu-id="1fcdb-106">O operador Fusion é uma maneira de melhorar o desempenho mesclando um operador (normalmente, uma função de ativação) em um operador diferente para que eles sejam executados juntos sem a necessidade de uma viagem de ida e volta à memória.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-106">Operator fusion is a way to improve performance by merging one operator (typically, an activation function) into a different operator so that they are executed together without requiring a roundtrip to memory.</span></span>

## <a name="when-to-fuse-activations"></a><span data-ttu-id="1fcdb-107">Quando unir ativações</span><span class="sxs-lookup"><span data-stu-id="1fcdb-107">When to fuse activations</span></span>

<span data-ttu-id="1fcdb-108">As ativações com fusível são uma otimização de desempenho.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-108">Fused activations are a performance optimization.</span></span> <span data-ttu-id="1fcdb-109">Um cenário extremamente comum em muitos modelos de ML (aprendizado de máquina) é aplicar uma não linearidade (uma função de ativação) à saída de cada camada no modelo.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-109">An extremely common scenario in many machine learning (ML) models is to apply a nonlinearity (an activation function) to the output of each layer in the model.</span></span>

<span data-ttu-id="1fcdb-110">Normalmente, isso requer um ida e volta para a memória gráfica.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-110">Ordinarily, this requires a roundtrip to graphics memory.</span></span> <span data-ttu-id="1fcdb-111">Por exemplo, se uma convolução for seguida por uma ativação Relu não-fundida, a GPU deverá aguardar que os resultados da convolução sejam gravados na memória da GPU antes que possa começar a calcular a camada de ativação do Relu.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-111">For example if a Convolution is followed by a non-fused Relu activation, then the GPU must wait for the results of the Convolution to be written into GPU memory before it can begin computing the Relu activation layer.</span></span> <span data-ttu-id="1fcdb-112">Como a carga de trabalho de computação da maioria das funções de ativação tende a ser pequena, essa resposta para a memória de gráficos pode ser um grande afunilamento de desempenho.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-112">As the compute workload of most activation functions tends to be small, this roundtrip to graphics memory can be a major performance bottleneck.</span></span>

<span data-ttu-id="1fcdb-113">A fusão de operadores permite que a função de ativação (Relu no exemplo acima) seja executada como parte do operador anterior (convolução, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="1fcdb-113">Operator fusion allows the activation function (Relu in the above example) to be performed as part of the preceding operator (Convolution, for example).</span></span> <span data-ttu-id="1fcdb-114">Isso permite que a GPU Compute a função de ativação sem esperar que os resultados do operador anterior sejam gravados na memória &mdash; e melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-114">This allows the GPU to compute the activation function without waiting for the results of the preceding operator to be written into memory&mdash;and that improves performance.</span></span>

<span data-ttu-id="1fcdb-115">Como as ativações com fusível produzem o mesmo resultado, mas são mais rápidas em muitos casos, recomendamos que você elimine as camadas de ativação, combinando-as em seu operador precedente sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-115">Because fused activations produce the same result, but are faster in many cases, we recommend that you eliminate activation layers by fusing them into their preceding operator wherever possible.</span></span>

## <a name="how-to-fuse-activations"></a><span data-ttu-id="1fcdb-116">Como unir as ativações</span><span class="sxs-lookup"><span data-stu-id="1fcdb-116">How to fuse activations</span></span>

<span data-ttu-id="1fcdb-117">Os operadores que dão suporte a ativações com fusível têm um parâmetro opcional adicional em sua estrutura de operador, `const DML_OPERATOR_DESC* FusedActivation` .</span><span class="sxs-lookup"><span data-stu-id="1fcdb-117">Operators that support fused activations have an additional optional parameter in their operator struct, `const DML_OPERATOR_DESC* FusedActivation`.</span></span> <span data-ttu-id="1fcdb-118">A convolução, por exemplo, dá suporte à ativação de fusível e tem um *FusedActivation* correspondente na descrição do operador (consulte [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="1fcdb-118">Convolution, for example, supports fused activation, and it has a corresponding *FusedActivation* in its operator description (see [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span></span>

```cpp
struct DML_CONVOLUTION_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* FilterTensor;
    \_Maybenull\_ const DML_TENSOR_DESC* BiasTensor;
    const DML_TENSOR_DESC* OutputTensor;
    DML_CONVOLUTION_MODE Mode;
    DML_CONVOLUTION_DIRECTION Direction;
    UINT DimensionCount;
    _Field_size_(DimensionCount) const UINT* Strides;
    _Field_size_(DimensionCount) const UINT* Dilations;
    _Field_size_(DimensionCount) const UINT* StartPadding;
    _Field_size_(DimensionCount) const UINT* EndPadding;
    _Field_size_(DimensionCount) const UINT* OutputPadding;
    UINT GroupCount;
    \_Maybenull\_ const DML_OPERATOR_DESC* FusedActivation;
};
```

<span data-ttu-id="1fcdb-119">Para fundir uma ativação, construa um [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) que descreve o tipo de ativação a ser fundido.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-119">To fuse an activation, construct a [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) that describes the type of activation to be fused.</span></span> <span data-ttu-id="1fcdb-120">Por exemplo, para fusível de uma função Relu, o tipo de operador correto seria [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="1fcdb-120">For example to fuse a Relu function, the correct operator type would be [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

> [!NOTE]
> <span data-ttu-id="1fcdb-121">Ao construir a descrição do operador para a função de ativação, você deve definir os parâmetros *InputTensor* e *OutputTensor* para a função de ativação como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-121">When constructing the operator description for the activation function, you must set the *InputTensor* and *OutputTensor* parameters for the activation function to **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="1fcdb-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1fcdb-122">Example</span></span>

```cpp
DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC leakyReluDesc;
leakyReluDesc.InputTensor = nullptr;
leakyReluDesc.OutputTensor = nullptr;
leakyReluDesc.Alpha = 0.01f;

DML_OPERATOR_DESC activationDesc = { DML_OPERATOR_ACTIVATION_LEAKY_RELU, &leakyReluDesc };

DML_CONVOLUTION_OPERATOR_DESC convDesc;
// ...
convDesc.FusedActivation = &activationDesc;
```

<span data-ttu-id="1fcdb-123">Para obter um exemplo completo, o [exemplo DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) utiliza ativações com fusível para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-123">For a complete example, the [DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples) utilizes fused activations to improve performance.</span></span>

## <a name="operators-that-support-fused-activation"></a><span data-ttu-id="1fcdb-124">Operadores que dão suporte à ativação com fusível</span><span class="sxs-lookup"><span data-stu-id="1fcdb-124">Operators that support fused activation</span></span>

* [<span data-ttu-id="1fcdb-125">DML_OPERATOR_CONVOLUTION</span><span class="sxs-lookup"><span data-stu-id="1fcdb-125">DML_OPERATOR_CONVOLUTION</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="1fcdb-126">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-126">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="1fcdb-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="1fcdb-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** e **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** and **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="1fcdb-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>

## <a name="activations-that-are-supported-for-fusion"></a><span data-ttu-id="1fcdb-130">Ativações com suporte para Fusion</span><span class="sxs-lookup"><span data-stu-id="1fcdb-130">Activations that are supported for fusion</span></span>

* [<span data-ttu-id="1fcdb-131">DML_OPERATOR_ACTIVATION_ELU</span><span class="sxs-lookup"><span data-stu-id="1fcdb-131">DML_OPERATOR_ACTIVATION_ELU</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="1fcdb-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span></span>
* <span data-ttu-id="1fcdb-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span></span>
* <span data-ttu-id="1fcdb-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span></span>
* <span data-ttu-id="1fcdb-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span></span>
* <span data-ttu-id="1fcdb-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span></span>
* <span data-ttu-id="1fcdb-137">**DML_OPERATOR_ACTIVATION_RELU**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-137">**DML_OPERATOR_ACTIVATION_RELU**</span></span>
* <span data-ttu-id="1fcdb-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span></span>
* <span data-ttu-id="1fcdb-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span></span>
* <span data-ttu-id="1fcdb-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span></span>
* <span data-ttu-id="1fcdb-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span></span>
* <span data-ttu-id="1fcdb-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span></span>
* <span data-ttu-id="1fcdb-143">**DML_OPERATOR_ACTIVATION_TANH**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-143">**DML_OPERATOR_ACTIVATION_TANH**</span></span>
* <span data-ttu-id="1fcdb-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span></span>
* <span data-ttu-id="1fcdb-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="1fcdb-146">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="1fcdb-146">**DML_OPERATOR_ACTIVATION_CELU**</span></span>

<span data-ttu-id="1fcdb-147">Quaisquer operadores que não estejam nessa lista não têm suporte para a ativação com fusível.</span><span class="sxs-lookup"><span data-stu-id="1fcdb-147">Any operators not in this list are not supported for fused activation.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fcdb-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fcdb-148">See also</span></span>

<span data-ttu-id="1fcdb-149">[Exemplo de DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples)  </span><span class="sxs-lookup"><span data-stu-id="1fcdb-149">[DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples)  </span></span>  
[<span data-ttu-id="1fcdb-150">DML_CONVOLUTION_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="1fcdb-150">DML_CONVOLUTION_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
