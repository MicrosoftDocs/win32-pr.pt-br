---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Computa gradientes de repropagação para a média de Pooling (consulte [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 79a43e93f504e8d6f36553a4f672ef7e5845610f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105764336"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="3591e-103">Estrutura de DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="3591e-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="3591e-104">Computa gradientes de repropagação para a média de Pooling (consulte [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="3591e-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="3591e-105">Considere um **DML_AVERAGE_POOLING_OPERATOR_DESC** 2x2, sem preenchimento e um stride de 1, que realiza o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3591e-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="3591e-106">Cada janela 2x2 no tensor de entrada é calculada para produzir um elemento da saída (lendo zeros para elementos além da borda).</span><span class="sxs-lookup"><span data-stu-id="3591e-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="3591e-107">Aqui está um exemplo da saída de **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** dadas parâmetros semelhantes.</span><span class="sxs-lookup"><span data-stu-id="3591e-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="3591e-108">Observe que os valores no *OutputGradientTensor* representam as contribuições ponderadas desse elemento para o *OutputTensor* durante o operador de [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) original.</span><span class="sxs-lookup"><span data-stu-id="3591e-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3591e-109">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="3591e-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="3591e-110">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="3591e-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3591e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3591e-111">Syntax</span></span>

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a><span data-ttu-id="3591e-112">Membros</span><span class="sxs-lookup"><span data-stu-id="3591e-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="3591e-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3591e-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3591e-114">O gradiente de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="3591e-114">The incoming gradient tensor.</span></span> <span data-ttu-id="3591e-115">Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="3591e-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="3591e-116">Normalmente, esse tensor teria os mesmos tamanhos da *saída* do [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="3591e-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="3591e-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3591e-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3591e-118">Um tensor de saída que contém os gradientes propagados.</span><span class="sxs-lookup"><span data-stu-id="3591e-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="3591e-119">Normalmente, esse tensor teria os mesmos tamanhos que a *entrada* do [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="3591e-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="3591e-120">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="3591e-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="3591e-121">O número de elementos nas matrizes de *prerides*, *WindowSize*, *StartPadding* e *endpadding* .</span><span class="sxs-lookup"><span data-stu-id="3591e-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="3591e-122">Esse valor deve ser igual à contagem espacial da dimensão.</span><span class="sxs-lookup"><span data-stu-id="3591e-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="3591e-123">A contagem de dimensões espaciais será 2 se os dezenasais de 4D forem fornecidos ou 3 se forem fornecidos mais de dezenas.</span><span class="sxs-lookup"><span data-stu-id="3591e-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="3591e-124">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3591e-124">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3591e-125">Veja os *avanços* no [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3591e-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="3591e-126">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3591e-126">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3591e-127">Consulte *WindowSize* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3591e-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="3591e-128">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3591e-128">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3591e-129">Consulte *StartPadding* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3591e-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="3591e-130">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3591e-130">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3591e-131">Consulte *endpadding* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3591e-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="3591e-132">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="3591e-132">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="3591e-133">Consulte *IncludePadding* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3591e-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="3591e-134">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="3591e-134">Availability</span></span>
<span data-ttu-id="3591e-135">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="3591e-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3591e-136">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="3591e-136">Tensor constraints</span></span>
<span data-ttu-id="3591e-137">*InputGradientTensor* e *OutputGradientTensor* devem ter o mesmo *tipo de dados* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="3591e-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3591e-138">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="3591e-138">Tensor support</span></span>
| <span data-ttu-id="3591e-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="3591e-139">Tensor</span></span> | <span data-ttu-id="3591e-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="3591e-140">Kind</span></span> | <span data-ttu-id="3591e-141">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="3591e-141">Supported dimension counts</span></span> | <span data-ttu-id="3591e-142">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="3591e-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3591e-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="3591e-143">InputGradientTensor</span></span> | <span data-ttu-id="3591e-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="3591e-144">Input</span></span> | <span data-ttu-id="3591e-145">4 a 5</span><span class="sxs-lookup"><span data-stu-id="3591e-145">4 to 5</span></span> | <span data-ttu-id="3591e-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3591e-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="3591e-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="3591e-147">OutputGradientTensor</span></span> | <span data-ttu-id="3591e-148">Saída</span><span class="sxs-lookup"><span data-stu-id="3591e-148">Output</span></span> | <span data-ttu-id="3591e-149">4 a 5</span><span class="sxs-lookup"><span data-stu-id="3591e-149">4 to 5</span></span> | <span data-ttu-id="3591e-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3591e-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="3591e-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3591e-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3591e-152">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="3591e-152">**Header**</span></span> | <span data-ttu-id="3591e-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="3591e-153">directml.h</span></span> |