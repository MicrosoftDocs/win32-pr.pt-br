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
# <a name="using-fused-operators-to-improve-performance"></a>Usando operadores com fusível para melhorar o desempenho

Alguns operadores DirectML dão suporte a um conceito conhecido como *Fusion*. O operador Fusion é uma maneira de melhorar o desempenho mesclando um operador (normalmente, uma função de ativação) em um operador diferente para que eles sejam executados juntos sem a necessidade de uma viagem de ida e volta à memória.

## <a name="when-to-fuse-activations"></a>Quando unir ativações

As ativações com fusível são uma otimização de desempenho. Um cenário extremamente comum em muitos modelos de ML (aprendizado de máquina) é aplicar uma não linearidade (uma função de ativação) à saída de cada camada no modelo.

Normalmente, isso requer um ida e volta para a memória gráfica. Por exemplo, se uma convolução for seguida por uma ativação Relu não-fundida, a GPU deverá aguardar que os resultados da convolução sejam gravados na memória da GPU antes que possa começar a calcular a camada de ativação do Relu. Como a carga de trabalho de computação da maioria das funções de ativação tende a ser pequena, essa resposta para a memória de gráficos pode ser um grande afunilamento de desempenho.

A fusão de operadores permite que a função de ativação (Relu no exemplo acima) seja executada como parte do operador anterior (convolução, por exemplo). Isso permite que a GPU Compute a função de ativação sem esperar que os resultados do operador anterior sejam gravados na memória &mdash; e melhora o desempenho.

Como as ativações com fusível produzem o mesmo resultado, mas são mais rápidas em muitos casos, recomendamos que você elimine as camadas de ativação, combinando-as em seu operador precedente sempre que possível.

## <a name="how-to-fuse-activations"></a>Como unir as ativações

Os operadores que dão suporte a ativações com fusível têm um parâmetro opcional adicional em sua estrutura de operador, `const DML_OPERATOR_DESC* FusedActivation` . A convolução, por exemplo, dá suporte à ativação de fusível e tem um *FusedActivation* correspondente na descrição do operador (consulte [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).

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

Para fundir uma ativação, construa um [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) que descreve o tipo de ativação a ser fundido. Por exemplo, para fusível de uma função Relu, o tipo de operador correto seria [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).

> [!NOTE]
> Ao construir a descrição do operador para a função de ativação, você deve definir os parâmetros *InputTensor* e *OutputTensor* para a função de ativação como **NULL**.

## <a name="example"></a>Exemplo

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

Para obter um exemplo completo, o [exemplo DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) utiliza ativações com fusível para melhorar o desempenho.

## <a name="operators-that-support-fused-activation"></a>Operadores que dão suporte à ativação com fusível

* [DML_OPERATOR_CONVOLUTION](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** e **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**

## <a name="activations-that-are-supported-for-fusion"></a>Ativações com suporte para Fusion

* [DML_OPERATOR_ACTIVATION_ELU](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_ACTIVATION_HARD_SIGMOID**
* **DML_OPERATOR_ACTIVATION_IDENTITY**
* **DML_OPERATOR_ACTIVATION_LEAKY_RELU**
* **DML_OPERATOR_ACTIVATION_LINEAR**
* **DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_RELU**
* **DML_OPERATOR_ACTIVATION_SCALED_ELU**
* **DML_OPERATOR_ACTIVATION_SCALED_TANH**
* **DML_OPERATOR_ACTIVATION_SIGMOID**
* **DML_OPERATOR_ACTIVATION_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_SOFTSIGN**
* **DML_OPERATOR_ACTIVATION_TANH**
* **DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_ACTIVATION_CELU**

Quaisquer operadores que não estejam nessa lista não têm suporte para a ativação com fusível.

## <a name="see-also"></a>Confira também

[Exemplo de DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples)    
[DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
