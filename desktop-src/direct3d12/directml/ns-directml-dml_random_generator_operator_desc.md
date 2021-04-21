---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Preenche um tensor de saída com bits gerados de forma determinística, pseudo aleatória e distribuído uniformemente. Opcionalmente, esse operador também pode gerar um estado de gerador interno atualizado, que pode ser usado durante as execuções subsequentes do operador.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 6807c3a1ac91716739075f51196a75ae76ca479b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804071"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a><span data-ttu-id="3724d-104">Estrutura de DML_RANDOM_GENERATOR_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="3724d-104">DML_RANDOM_GENERATOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="3724d-105">Preenche um tensor de saída com bits gerados de forma determinística, pseudo aleatória e distribuído uniformemente.</span><span class="sxs-lookup"><span data-stu-id="3724d-105">Fills an output tensor with deterministically-generated, pseudo-random, uniformly-distributed bits.</span></span> <span data-ttu-id="3724d-106">Opcionalmente, esse operador também pode gerar um estado de gerador interno atualizado, que pode ser usado durante as execuções subsequentes do operador.</span><span class="sxs-lookup"><span data-stu-id="3724d-106">This operator optionally may also output an updated internal generator state, which can be used during subsequent executions of the operator.</span></span>

<span data-ttu-id="3724d-107">Esse operador é determinístico e se comporta como se fosse uma função pura &mdash; , ou seja, sua execução não produz efeitos colaterais e não usa nenhum estado global.</span><span class="sxs-lookup"><span data-stu-id="3724d-107">This operator is deterministic, and behaves as if it were a pure function&mdash;that is, its execution produces no side-effects, and uses no global state.</span></span> <span data-ttu-id="3724d-108">A saída pseudo aleatória produzida por esse operador é exclusivamente dependente dos valores fornecidos no *InputStateTensor*.</span><span class="sxs-lookup"><span data-stu-id="3724d-108">The pseudo-random output produced by this operator is solely dependent on the values supplied in the *InputStateTensor*.</span></span>

<span data-ttu-id="3724d-109">Os geradores implementados por esse operador não são criptograficamente seguros; Portanto, esse operador não deve ser usado para criptografia, geração de chave ou outros aplicativos que exijam a geração de números aleatórios criptograficamente seguros.</span><span class="sxs-lookup"><span data-stu-id="3724d-109">The generators implemented by this operator are not cryptographically secure; therefore, this operator should not be used for encryption, key generation, or other applications which require cryptographically secure random number generation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3724d-110">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3724d-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="3724d-111">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="3724d-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3724d-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3724d-112">Syntax</span></span>

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a><span data-ttu-id="3724d-113">Membros</span><span class="sxs-lookup"><span data-stu-id="3724d-113">Members</span></span>

`InputStateTensor`

<span data-ttu-id="3724d-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3724d-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3724d-115">Um tensor de entrada que contém o estado do gerador interno.</span><span class="sxs-lookup"><span data-stu-id="3724d-115">An input tensor containing the internal generator state.</span></span> <span data-ttu-id="3724d-116">O tamanho e o formato dessa entrada tensor dependem do [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span><span class="sxs-lookup"><span data-stu-id="3724d-116">The size and format of this input tensor depends on the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span></span>

<span data-ttu-id="3724d-117">Por **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, esse tensor deve ser do tipo **UINT32** e ter tamanhos `{1,1,1,6}` .</span><span class="sxs-lookup"><span data-stu-id="3724d-117">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, this tensor must be of type **UINT32**, and have sizes `{1,1,1,6}`.</span></span> <span data-ttu-id="3724d-118">Os primeiros valores de 4 32 bits contêm um contador de 128 bits com um aumento monotônico.</span><span class="sxs-lookup"><span data-stu-id="3724d-118">The first four 32-bit values contain a monotonically increasing 128-bit counter.</span></span> <span data-ttu-id="3724d-119">Os últimos valores de 2 32 bits contêm o valor de chave de 64 bits para o gerador.</span><span class="sxs-lookup"><span data-stu-id="3724d-119">The last two 32-bit values contain the 64-bit key value for the generator.</span></span>

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

<span data-ttu-id="3724d-120">Ao inicializar o estado de entrada do gerador pela primeira vez, normalmente o contador de 128 bits (os primeiros valores UINT32 de 4 32 bits) deve ser inicializado como 0.</span><span class="sxs-lookup"><span data-stu-id="3724d-120">When initializing the generator's input state for the first time, typically the 128-bit counter (the first four 32-bit UINT32 values) should be initialized to 0.</span></span> <span data-ttu-id="3724d-121">A chave pode ser escolhida arbitrariamente; valores de chave diferentes produzirão sequências diferentes de números.</span><span class="sxs-lookup"><span data-stu-id="3724d-121">The key can be arbitrarily chosen; different key values will produce different sequences of numbers.</span></span> <span data-ttu-id="3724d-122">O valor da chave geralmente é gerado usando uma *semente* fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3724d-122">The value for the key is usually generated using a user-provided *seed*.</span></span>

`OutputTensor`

<span data-ttu-id="3724d-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3724d-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3724d-124">Um tensor de saída que contém os valores pseudo aleatórios resultantes.</span><span class="sxs-lookup"><span data-stu-id="3724d-124">An output tensor which holds the resulting pseudo-random values.</span></span> <span data-ttu-id="3724d-125">Esse tensor pode ser de qualquer tamanho.</span><span class="sxs-lookup"><span data-stu-id="3724d-125">This tensor can be of any size.</span></span>

`OutputStateTensor`

<span data-ttu-id="3724d-126">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3724d-126">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3724d-127">Um tensor de saída opcional que contém o estado do gerador interno atualizado.</span><span class="sxs-lookup"><span data-stu-id="3724d-127">An optional output tensor THAT holds the updated internal generator state.</span></span> <span data-ttu-id="3724d-128">Se fornecido, esse operador usa o *InputStateTensor* para computar um estado de gerador atualizado apropriado e grava o resultado em *OutputStateTensor*.</span><span class="sxs-lookup"><span data-stu-id="3724d-128">If supplied, this operator uses the *InputStateTensor* to compute an appropriate updated generator state, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="3724d-129">Normalmente, os chamadores salvariam esse resultado e o forneceriam como o estado de entrada em uma execução subsequente desse operador.</span><span class="sxs-lookup"><span data-stu-id="3724d-129">Typically, callers would save this result and supply it as the input state on a subsequent execution of this operator.</span></span>

`Type`

<span data-ttu-id="3724d-130">Tipo: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span><span class="sxs-lookup"><span data-stu-id="3724d-130">Type: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span></span>

<span data-ttu-id="3724d-131">Um dos valores da enumeração [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) , que indica o tipo de gerador a ser usado.</span><span class="sxs-lookup"><span data-stu-id="3724d-131">One of the values from the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) enum, indicating the type of generator to use.</span></span> <span data-ttu-id="3724d-132">Atualmente, o único valor válido é **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, que gera números pseudo aleatórios de acordo com o [algoritmo PHILOX 4X32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span><span class="sxs-lookup"><span data-stu-id="3724d-132">Currently the only valid value is **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, which generates pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span>

## <a name="remarks"></a><span data-ttu-id="3724d-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="3724d-133">Remarks</span></span>
<span data-ttu-id="3724d-134">Em cada execução desse operador, o contador de 128 bits deve ser incrementado.</span><span class="sxs-lookup"><span data-stu-id="3724d-134">On each execution of this operator, the 128-bit counter should be incremented.</span></span> <span data-ttu-id="3724d-135">Se o *OutputStateTensor* for fornecido, esse operador incrementará o contador com o valor correto em seu nome e gravará o resultado no *OutputStateTensor*.</span><span class="sxs-lookup"><span data-stu-id="3724d-135">If the *OutputStateTensor* is supplied, THEN this operator increments the counter with the correct value on your behalf, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="3724d-136">A quantidade que deve ser incrementada depende do número de elementos de saída de 32 bits gerados e do tipo do gerador.</span><span class="sxs-lookup"><span data-stu-id="3724d-136">The amount it should be incremented by depends on the number of 32-bit output elements generated, and the type of the generator.</span></span>

<span data-ttu-id="3724d-137">Por **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, o contador de 128 bits deve ser incrementado `ceil(outputSize / 4)` em cada execução, em que `outputSize` é o número de elementos no *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="3724d-137">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, the 128-bit counter should be incremented by `ceil(outputSize / 4)` on each execution, where `outputSize` is the number of elements in the *OutputTensor*.</span></span>

<span data-ttu-id="3724d-138">Considere um exemplo em que o valor do contador de 128 bits é atualmente `0x48656c6c'6f46726f'6d536561'74746c65` , e o tamanho do OutputTensor é `{3,3,20,7219}` .</span><span class="sxs-lookup"><span data-stu-id="3724d-138">Consider an example where the value of the 128-bit counter is currently `0x48656c6c'6f46726f'6d536561'74746c65`, and the OutputTensor's size is `{3,3,20,7219}`.</span></span> <span data-ttu-id="3724d-139">Depois de executar esse operador uma vez, o contador deve ser incrementado por 324.855 (o número de elementos de saída gerados dividido por 4, arredondado) resultando em um valor de contador de `0x48656c6c'6f46726f'6d536561'746f776e` .</span><span class="sxs-lookup"><span data-stu-id="3724d-139">After executing this operator once, the counter should be incremented by 324,855 (the number of output elements generated divided by 4, rounded up) resulting in a counter value of `0x48656c6c'6f46726f'6d536561'746f776e`.</span></span> <span data-ttu-id="3724d-140">Esse valor atualizado deve então ser fornecido como uma entrada para a próxima execução desse operador.</span><span class="sxs-lookup"><span data-stu-id="3724d-140">This updated value should then be supplied as an input for the next execution of this operator.</span></span>

## <a name="availability"></a><span data-ttu-id="3724d-141">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="3724d-141">Availability</span></span>
<span data-ttu-id="3724d-142">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="3724d-142">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3724d-143">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="3724d-143">Tensor constraints</span></span>
<span data-ttu-id="3724d-144">`InputStateTensor` e `OutputStateTensor` devem ter os mesmos *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="3724d-144">`InputStateTensor` and `OutputStateTensor` must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3724d-145">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="3724d-145">Tensor support</span></span>
| <span data-ttu-id="3724d-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="3724d-146">Tensor</span></span> | <span data-ttu-id="3724d-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="3724d-147">Kind</span></span> | <span data-ttu-id="3724d-148">Dimensões</span><span class="sxs-lookup"><span data-stu-id="3724d-148">Dimensions</span></span> | <span data-ttu-id="3724d-149">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="3724d-149">Supported dimension counts</span></span> | <span data-ttu-id="3724d-150">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="3724d-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="3724d-151">InputStateTensor</span><span class="sxs-lookup"><span data-stu-id="3724d-151">InputStateTensor</span></span> | <span data-ttu-id="3724d-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="3724d-152">Input</span></span> | <span data-ttu-id="3724d-153">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="3724d-153">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="3724d-154">4</span><span class="sxs-lookup"><span data-stu-id="3724d-154">4</span></span> | <span data-ttu-id="3724d-155">UINT32</span><span class="sxs-lookup"><span data-stu-id="3724d-155">UINT32</span></span> |
| <span data-ttu-id="3724d-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="3724d-156">OutputTensor</span></span> | <span data-ttu-id="3724d-157">Saída</span><span class="sxs-lookup"><span data-stu-id="3724d-157">Output</span></span> | <span data-ttu-id="3724d-158">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="3724d-158">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="3724d-159">4</span><span class="sxs-lookup"><span data-stu-id="3724d-159">4</span></span> | <span data-ttu-id="3724d-160">UINT32</span><span class="sxs-lookup"><span data-stu-id="3724d-160">UINT32</span></span> |
| <span data-ttu-id="3724d-161">OutputStateTensor</span><span class="sxs-lookup"><span data-stu-id="3724d-161">OutputStateTensor</span></span> | <span data-ttu-id="3724d-162">Saída opcional</span><span class="sxs-lookup"><span data-stu-id="3724d-162">Optional output</span></span> | <span data-ttu-id="3724d-163">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="3724d-163">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="3724d-164">4</span><span class="sxs-lookup"><span data-stu-id="3724d-164">4</span></span> | <span data-ttu-id="3724d-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="3724d-165">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="3724d-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3724d-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3724d-167">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="3724d-167">**Header**</span></span> | <span data-ttu-id="3724d-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="3724d-168">directml.h</span></span> |