---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Computa pesos atualizados (parâmetros) usando os gradientes fornecidos, com base no algoritmo Adam (ptive de Oment de **Ada**= **M** estimativa). Esse operador é um otimizador e normalmente é usado na etapa de atualização de peso de um loop de treinamento para executar descendente de gradiente.
helpviewer_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- DML_ADAM_OPTIMIZER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ADAM_OPTIMIZER_OPERATOR_DESC, DML_ADAM_OPTIMIZER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.openlocfilehash: 9943f70bd3d62faf57f4eca83f9f09ce0119881a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417001"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a><span data-ttu-id="92bbc-104">Estrutura de DML_ADAM_OPTIMIZER_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="92bbc-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="92bbc-105">Computa pesos atualizados (parâmetros) usando os gradientes fornecidos, com base no algoritmo Adam (ptive de Oment de **Ada**= **M** estimativa).</span><span class="sxs-lookup"><span data-stu-id="92bbc-105">Computes updated weights (parameters) using the supplied gradients, based on the Adam (**ADA** ptive **M** oment estimation) algorithm.</span></span> <span data-ttu-id="92bbc-106">Esse operador é um otimizador e normalmente é usado na etapa de atualização de peso de um loop de treinamento para executar descendente de gradiente.</span><span class="sxs-lookup"><span data-stu-id="92bbc-106">This operator is an optimizer, and is typically used in the weight update step of a training loop to perform gradient descent.</span></span>

<span data-ttu-id="92bbc-107">Esse operador executa a seguinte computação:</span><span class="sxs-lookup"><span data-stu-id="92bbc-107">This operator performs the following computation:</span></span>

```
X = InputParametersTensor
M = InputFirstMomentTensor
V = InputSecondMomentTensor
G = GradientTensor
T = TrainingStepTensor

// Compute updated first and second moment estimates.
M = Beta1 * M + (1.0 - Beta1) * G
V = Beta2 * V + (1.0 - Beta2) * G * G

// Compute bias correction factor for first and second moment estimates.
Alpha = sqrt(1.0 - pow(Beta2, T)) / (1.0 - pow(Beta1, T))

X -= LearningRate * Alpha * M / (sqrt(V) + Epsilon)

OutputParametersTensor = X
OutputFirstMomentTensor = M
OutputSecondMomentTensor = V
```

<span data-ttu-id="92bbc-108">Além de computar os parâmetros de peso atualizados (retornados em *OutputParametersTensor*), esse operador também retorna as estimativas atualizadas do primeiro e do segundo momento em *OutputFirstMomentTensor* e *OutputSecondMomentTensor*, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="92bbc-108">In addition to computing the updated weight parameters (returned in *OutputParametersTensor*), this operator also returns the updated first and second moment estimates in *OutputFirstMomentTensor* and *OutputSecondMomentTensor*, respectively.</span></span> <span data-ttu-id="92bbc-109">Normalmente, você deve armazenar essas estimativas de primeiro e segundo momento e fornecê-las como entradas durante a etapa de treinamento subsequente.</span><span class="sxs-lookup"><span data-stu-id="92bbc-109">Typically, you should store these first and second moment estimates, and supply them as inputs during the subsequent training step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92bbc-110">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="92bbc-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="92bbc-111">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="92bbc-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="92bbc-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92bbc-112">Syntax</span></span>
```cpp
struct DML_ADAM_OPTIMIZER_OPERATOR_DESC
{ 
  const DML_TENSOR_DESC* InputParametersTensor;
  const DML_TENSOR_DESC* InputFirstMomentTensor;
  const DML_TENSOR_DESC* InputSecondMomentTensor;
  const DML_TENSOR_DESC* GradientTensor;
  const DML_TENSOR_DESC* TrainingStepTensor;
  const DML_TENSOR_DESC* OutputParametersTensor;
  const DML_TENSOR_DESC* OutputFirstMomentTensor;
  const DML_TENSOR_DESC* OutputSecondMomentTensor;
  FLOAT LearningRate;
  FLOAT Beta1;
  FLOAT Beta2;
  FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="92bbc-113">Membros</span><span class="sxs-lookup"><span data-stu-id="92bbc-113">Members</span></span>

`InputParametersTensor`

<span data-ttu-id="92bbc-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92bbc-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92bbc-115">Um tensor que contém os parâmetros (pesos) para aplicar esse otimizador a.</span><span class="sxs-lookup"><span data-stu-id="92bbc-115">A tensor containing the parameters (weights) to apply this optimizer to.</span></span> <span data-ttu-id="92bbc-116">As estimativas de gradiente, primeiro e segundo momento, a etapa de treinamento atual, bem como hiperparâmetros *LearningRate*, *beta1* e *beta2*, são usadas por esse operador para executar gradiente descendente nos valores de peso fornecidos neste tensor.</span><span class="sxs-lookup"><span data-stu-id="92bbc-116">The gradient, first, and second moment estimates, current training step, as well as hyperparameters *LearningRate*, *Beta1*, and *Beta2*, are used by this operator to perform gradient descent on the weight values supplied in this tensor.</span></span>

`InputFirstMomentTensor`

<span data-ttu-id="92bbc-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92bbc-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92bbc-118">Um tensor que contém a primeira estimativa de tempo do gradiente para cada valor de peso.</span><span class="sxs-lookup"><span data-stu-id="92bbc-118">A tensor containing the first moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="92bbc-119">Esses valores normalmente são obtidos como resultado de uma execução anterior desse operador, por meio de *OutputFirstMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-119">These values are typically obtained as the result of a previous execution of this operator, via the *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="92bbc-120">Ao aplicar esse otimizador a um conjunto de pesos pela primeira vez (por exemplo, durante a etapa de treinamento inicial), os valores desse tensor normalmente devem ser inicializados como zero.</span><span class="sxs-lookup"><span data-stu-id="92bbc-120">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="92bbc-121">As execuções subsequentes devem usar os valores retornados em *OutputFirstMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-121">Subsequent executions should use the values returned in *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="92bbc-122">Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-122">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`InputSecondMomentTensor`

<span data-ttu-id="92bbc-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92bbc-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92bbc-124">Um tensor que contém a segunda estimativa de tempo do gradiente para cada valor de peso.</span><span class="sxs-lookup"><span data-stu-id="92bbc-124">A tensor containing the second moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="92bbc-125">Esses valores normalmente são obtidos como resultado de uma execução anterior desse operador, por meio de *OutputSecondMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-125">These values are typically obtained as the result of a previous execution of this operator, via the *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="92bbc-126">Ao aplicar esse otimizador a um conjunto de pesos pela primeira vez (por exemplo, durante a etapa de treinamento inicial), os valores desse tensor normalmente devem ser inicializados como zero.</span><span class="sxs-lookup"><span data-stu-id="92bbc-126">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="92bbc-127">As execuções subsequentes devem usar os valores retornados em *OutputSecondMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-127">Subsequent executions should use the values returned in *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="92bbc-128">Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-128">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`GradientTensor`

<span data-ttu-id="92bbc-129">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92bbc-129">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92bbc-130">Os gradientes a serem aplicados aos parâmetros de entrada (pesos) para descendente de gradiente.</span><span class="sxs-lookup"><span data-stu-id="92bbc-130">The gradients to apply to the input parameters (weights) for gradient descent.</span></span> <span data-ttu-id="92bbc-131">Os gradientes normalmente são obtidos em uma passagem de repropagação durante o treinamento.</span><span class="sxs-lookup"><span data-stu-id="92bbc-131">Gradients are typically obtained in a backpropagation pass during training.</span></span>

<span data-ttu-id="92bbc-132">Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-132">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`TrainingStepTensor`

<span data-ttu-id="92bbc-133">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92bbc-133">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92bbc-134">Um tensor escalar que contém um único valor inteiro que representa a contagem de etapas de treinamento atual.</span><span class="sxs-lookup"><span data-stu-id="92bbc-134">A scalar tensor containing a single integer value representing the current training step count.</span></span> <span data-ttu-id="92bbc-135">Esse valor junto com *beta1* e *beta2* é usado para calcular a decaimento exponencial do primeiro e do segundo tempo estimar os tempos.</span><span class="sxs-lookup"><span data-stu-id="92bbc-135">This value along with *Beta1* and *Beta2* is used to compute the exponential decay of the first and second moment estimate tensors.</span></span>

<span data-ttu-id="92bbc-136">Normalmente, o valor da etapa de treinamento começa em 0 no início do treinamento e é incrementado em 1 em cada etapa de treinamento sucessiva.</span><span class="sxs-lookup"><span data-stu-id="92bbc-136">Typically the training step value starts at 0 at the beginning of training, and is incremented by 1 on each successive training step.</span></span> <span data-ttu-id="92bbc-137">Esse operador não atualiza o valor da etapa de treinamento; Você deve fazer isso manualmente, por exemplo, usando [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="92bbc-137">This operator doesn't update the training step value; you should do that manually, for example using [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span></span>

<span data-ttu-id="92bbc-138">Esse tensor deve ser um escalar (ou seja, todos os *tamanhos* iguais a 1) e ter o tipo de dados [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span><span class="sxs-lookup"><span data-stu-id="92bbc-138">This tensor must be a scalar (that is, all *Sizes* equal to 1) and have data type [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span></span>

`OutputParametersTensor`

<span data-ttu-id="92bbc-139">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92bbc-139">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92bbc-140">Um tensor de saída que contém os valores de parâmetro (peso) atualizados após a aplicação do descendente do gradiente.</span><span class="sxs-lookup"><span data-stu-id="92bbc-140">An output tensor that holds the updated parameter (weight) values after gradient descent is applied.</span></span>

<span data-ttu-id="92bbc-141">Durante a associação, esse tensor é permitido para alias de um tensor de entrada qualificado, que pode ser usado para executar uma atualização in-loco desse tensor.</span><span class="sxs-lookup"><span data-stu-id="92bbc-141">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="92bbc-142">Consulte a seção [comentários](#remarks) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="92bbc-142">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="92bbc-143">Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-143">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputFirstMomentTensor`

<span data-ttu-id="92bbc-144">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92bbc-144">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92bbc-145">Uma tensor de saída que contém estimativas de primeiro momento atualizadas.</span><span class="sxs-lookup"><span data-stu-id="92bbc-145">An output tensor containing updated first moment estimates.</span></span> <span data-ttu-id="92bbc-146">Você deve armazenar os valores desse tensor e fornecê-los em *InputFirstMomentTensor* durante a etapa de treinamento subsequente.</span><span class="sxs-lookup"><span data-stu-id="92bbc-146">You should store the values of this tensor, and supply them in *InputFirstMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="92bbc-147">Durante a associação, esse tensor é permitido para alias de um tensor de entrada qualificado, que pode ser usado para executar uma atualização in-loco desse tensor.</span><span class="sxs-lookup"><span data-stu-id="92bbc-147">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="92bbc-148">Consulte a seção [comentários](#remarks) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="92bbc-148">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="92bbc-149">Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-149">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputSecondMomentTensor`

<span data-ttu-id="92bbc-150">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92bbc-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92bbc-151">Um tensor de saída que contém estimativas de segundo momento atualizadas.</span><span class="sxs-lookup"><span data-stu-id="92bbc-151">An output tensor containing updated second moment estimates.</span></span> <span data-ttu-id="92bbc-152">Você deve armazenar os valores desse tensor e fornecê-los em *InputSecondMomentTensor* durante a etapa de treinamento subsequente.</span><span class="sxs-lookup"><span data-stu-id="92bbc-152">You should store the values of this tensor and supply them in *InputSecondMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="92bbc-153">Durante a associação, esse tensor é permitido para alias de um tensor de entrada qualificado, que pode ser usado para executar uma atualização in-loco desse tensor.</span><span class="sxs-lookup"><span data-stu-id="92bbc-153">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="92bbc-154">Consulte a seção [comentários](#remarks) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="92bbc-154">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="92bbc-155">Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-155">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`LearningRate`

<span data-ttu-id="92bbc-156">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="92bbc-156">Type: **float**</span></span>

<span data-ttu-id="92bbc-157">A taxa de aprendizagem, também conhecida como o *tamanho da etapa*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-157">The learning rate, also commonly referred to as the *step size*.</span></span> <span data-ttu-id="92bbc-158">A taxa de aprendizagem é um hiperparâmetro que determina a magnitude da atualização de peso ao longo do vetor de gradiente em cada etapa de treinamento.</span><span class="sxs-lookup"><span data-stu-id="92bbc-158">The learning rate is a hyperparameter that determines the magnitude of the weight update along the gradient vector on each training step.</span></span>

`Beta1`

<span data-ttu-id="92bbc-159">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="92bbc-159">Type: **float**</span></span>

<span data-ttu-id="92bbc-160">Um hiperparâmetro que representa a taxa de decaimento exponencial da primeira estimativa de momento do gradiente.</span><span class="sxs-lookup"><span data-stu-id="92bbc-160">A hyperparameter representing the exponential decay rate of the gradient's first moment estimate.</span></span> <span data-ttu-id="92bbc-161">Esse valor deve estar entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="92bbc-161">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="92bbc-162">Um valor de 0,9 f é típico.</span><span class="sxs-lookup"><span data-stu-id="92bbc-162">A value of 0.9f is typical.</span></span>

`Beta2`

<span data-ttu-id="92bbc-163">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="92bbc-163">Type: **float**</span></span>

<span data-ttu-id="92bbc-164">Um hiperparâmetro que representa a taxa de decaimento exponencial da estimativa do segundo tempo do gradiente.</span><span class="sxs-lookup"><span data-stu-id="92bbc-164">A hyperparameter representing the exponential decay rate of the gradient's second moment estimate.</span></span> <span data-ttu-id="92bbc-165">Esse valor deve estar entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="92bbc-165">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="92bbc-166">Um valor de 0,999 f é típico.</span><span class="sxs-lookup"><span data-stu-id="92bbc-166">A value of 0.999f is typical.</span></span>

`Epsilon`

<span data-ttu-id="92bbc-167">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="92bbc-167">Type: **float**</span></span>

<span data-ttu-id="92bbc-168">Um valor pequeno usado para ajudar na estabilidade numérica, impedindo a divisão por zero.</span><span class="sxs-lookup"><span data-stu-id="92bbc-168">A small value used to help numerical stability by preventing division-by-zero.</span></span> <span data-ttu-id="92bbc-169">Para entradas de ponto flutuante de 32 bits, os valores típicos incluem 1e-8 ou `FLT_EPSILON` .</span><span class="sxs-lookup"><span data-stu-id="92bbc-169">For 32-bit floating-point inputs, typical values include 1e-8 or `FLT_EPSILON`.</span></span>

## <a name="remarks"></a><span data-ttu-id="92bbc-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="92bbc-170">Remarks</span></span>
<span data-ttu-id="92bbc-171">Esse operador dá suporte à execução in-loco, o que significa que cada tensor de saída tem permissão para alias de um tensor de entrada qualificado durante a associação.</span><span class="sxs-lookup"><span data-stu-id="92bbc-171">This operator supports in-place execution, meaning that each output tensor is permitted to alias an eligible input tensor during binding.</span></span> <span data-ttu-id="92bbc-172">Por exemplo, é possível associar o mesmo recurso para *InputParametersTensor* e *OutputParametersTensor* a fim de alcançar efetivamente uma atualização in-loco dos parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="92bbc-172">For example, it's possible to bind the same resource for both the *InputParametersTensor* and *OutputParametersTensor* in order to effectively achieve an in-place update of the input parameters.</span></span> <span data-ttu-id="92bbc-173">Todos os tempos de entrada desse operador, com exceção do *TrainingStepTensor*, estão qualificados para serem alias dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="92bbc-173">All of this operator's input tensors, with the exception of the *TrainingStepTensor*, are eligible to be aliased in this way.</span></span>

## <a name="availability"></a><span data-ttu-id="92bbc-174">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="92bbc-174">Availability</span></span>
<span data-ttu-id="92bbc-175">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="92bbc-175">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="92bbc-176">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-176">Tensor constraints</span></span>
* <span data-ttu-id="92bbc-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* e *TrainingStepTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor*, and *TrainingStepTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="92bbc-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor* e *OutputSecondMomentTensor* devem ter os mesmos *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="92bbc-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, and *OutputSecondMomentTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="92bbc-179">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-179">Tensor support</span></span>
| <span data-ttu-id="92bbc-180">Tensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-180">Tensor</span></span> | <span data-ttu-id="92bbc-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="92bbc-181">Kind</span></span> | <span data-ttu-id="92bbc-182">Dimensões</span><span class="sxs-lookup"><span data-stu-id="92bbc-182">Dimensions</span></span> | <span data-ttu-id="92bbc-183">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="92bbc-183">Supported dimension counts</span></span> | <span data-ttu-id="92bbc-184">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="92bbc-184">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="92bbc-185">InputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-185">InputParametersTensor</span></span> | <span data-ttu-id="92bbc-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="92bbc-186">Input</span></span> | <span data-ttu-id="92bbc-187">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="92bbc-187">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="92bbc-188">4</span><span class="sxs-lookup"><span data-stu-id="92bbc-188">4</span></span> | <span data-ttu-id="92bbc-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92bbc-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="92bbc-190">InputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-190">InputFirstMomentTensor</span></span> | <span data-ttu-id="92bbc-191">Entrada</span><span class="sxs-lookup"><span data-stu-id="92bbc-191">Input</span></span> | <span data-ttu-id="92bbc-192">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="92bbc-192">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="92bbc-193">4</span><span class="sxs-lookup"><span data-stu-id="92bbc-193">4</span></span> | <span data-ttu-id="92bbc-194">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92bbc-194">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="92bbc-195">InputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-195">InputSecondMomentTensor</span></span> | <span data-ttu-id="92bbc-196">Entrada</span><span class="sxs-lookup"><span data-stu-id="92bbc-196">Input</span></span> | <span data-ttu-id="92bbc-197">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="92bbc-197">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="92bbc-198">4</span><span class="sxs-lookup"><span data-stu-id="92bbc-198">4</span></span> | <span data-ttu-id="92bbc-199">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92bbc-199">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="92bbc-200">GradientTensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-200">GradientTensor</span></span> | <span data-ttu-id="92bbc-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="92bbc-201">Input</span></span> | <span data-ttu-id="92bbc-202">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="92bbc-202">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="92bbc-203">4</span><span class="sxs-lookup"><span data-stu-id="92bbc-203">4</span></span> | <span data-ttu-id="92bbc-204">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92bbc-204">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="92bbc-205">TrainingStepTensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-205">TrainingStepTensor</span></span> | <span data-ttu-id="92bbc-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="92bbc-206">Input</span></span> | <span data-ttu-id="92bbc-207">{1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="92bbc-207">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="92bbc-208">4</span><span class="sxs-lookup"><span data-stu-id="92bbc-208">4</span></span> | <span data-ttu-id="92bbc-209">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92bbc-209">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="92bbc-210">OutputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-210">OutputParametersTensor</span></span> | <span data-ttu-id="92bbc-211">Saída</span><span class="sxs-lookup"><span data-stu-id="92bbc-211">Output</span></span> | <span data-ttu-id="92bbc-212">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="92bbc-212">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="92bbc-213">4</span><span class="sxs-lookup"><span data-stu-id="92bbc-213">4</span></span> | <span data-ttu-id="92bbc-214">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92bbc-214">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="92bbc-215">OutputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-215">OutputFirstMomentTensor</span></span> | <span data-ttu-id="92bbc-216">Saída</span><span class="sxs-lookup"><span data-stu-id="92bbc-216">Output</span></span> | <span data-ttu-id="92bbc-217">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="92bbc-217">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="92bbc-218">4</span><span class="sxs-lookup"><span data-stu-id="92bbc-218">4</span></span> | <span data-ttu-id="92bbc-219">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92bbc-219">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="92bbc-220">OutputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="92bbc-220">OutputSecondMomentTensor</span></span> | <span data-ttu-id="92bbc-221">Saída</span><span class="sxs-lookup"><span data-stu-id="92bbc-221">Output</span></span> | <span data-ttu-id="92bbc-222">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="92bbc-222">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="92bbc-223">4</span><span class="sxs-lookup"><span data-stu-id="92bbc-223">4</span></span> | <span data-ttu-id="92bbc-224">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92bbc-224">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="92bbc-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92bbc-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="92bbc-226">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="92bbc-226">**Header**</span></span> | <span data-ttu-id="92bbc-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="92bbc-227">directml.h</span></span> |