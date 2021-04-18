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
ms.openlocfilehash: 19e01ec8dc47e65ace996deef5954c35e21bf5bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105793771"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>Estrutura de DML_RANDOM_GENERATOR_OPERATOR_DESC (directml. h)

Preenche um tensor de saída com bits gerados de forma determinística, pseudo aleatória e distribuído uniformemente. Opcionalmente, esse operador também pode gerar um estado de gerador interno atualizado, que pode ser usado durante as execuções subsequentes do operador.

Esse operador é determinístico e se comporta como se fosse uma função pura &mdash; , ou seja, sua execução não produz efeitos colaterais e não usa nenhum estado global. A saída pseudo aleatória produzida por esse operador é exclusivamente dependente dos valores fornecidos no *InputStateTensor*.

Os geradores implementados por esse operador não são criptograficamente seguros; Portanto, esse operador não deve ser usado para criptografia, geração de chave ou outros aplicativos que exijam a geração de números aleatórios criptograficamente seguros.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a>Membros

`InputStateTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de entrada que contém o estado do gerador interno. O tamanho e o formato dessa entrada tensor dependem do [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).

Por **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, esse tensor deve ser do tipo **UINT32** e ter tamanhos `{1,1,1,6}` . Os primeiros valores de 4 32 bits contêm um contador de 128 bits com um aumento monotônico. Os últimos valores de 2 32 bits contêm o valor de chave de 64 bits para o gerador.

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

Ao inicializar o estado de entrada do gerador pela primeira vez, normalmente o contador de 128 bits (os primeiros valores UINT32 de 4 32 bits) deve ser inicializado como 0. A chave pode ser escolhida arbitrariamente; valores de chave diferentes produzirão sequências diferentes de números. O valor da chave geralmente é gerado usando uma *semente* fornecida pelo usuário.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída que contém os valores pseudo aleatórios resultantes. Esse tensor pode ser de qualquer tamanho.

`OutputStateTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída opcional que contém o estado do gerador interno atualizado. Se fornecido, esse operador usa o *InputStateTensor* para computar um estado de gerador atualizado apropriado e grava o resultado em *OutputStateTensor*. Normalmente, os chamadores salvariam esse resultado e o forneceriam como o estado de entrada em uma execução subsequente desse operador.

`Type`

Tipo: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

Um dos valores da enumeração [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) , que indica o tipo de gerador a ser usado. Atualmente, o único valor válido é **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, que gera números pseudo aleatórios de acordo com o [algoritmo PHILOX 4X32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).

## <a name="remarks"></a>Comentários
Em cada execução desse operador, o contador de 128 bits deve ser incrementado. Se o *OutputStateTensor* for fornecido, esse operador incrementará o contador com o valor correto em seu nome e gravará o resultado no *OutputStateTensor*. A quantidade que deve ser incrementada depende do número de elementos de saída de 32 bits gerados e do tipo do gerador.

Por **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, o contador de 128 bits deve ser incrementado `ceil(outputSize / 4)` em cada execução, em que `outputSize` é o número de elementos no *OutputTensor*.

Considere um exemplo em que o valor do contador de 128 bits é atualmente `0x48656c6c'6f46726f'6d536561'74746c65` , e o tamanho do OutputTensor é `{3,3,20,7219}` . Depois de executar esse operador uma vez, o contador deve ser incrementado por 324.855 (o número de elementos de saída gerados dividido por 4, arredondado) resultando em um valor de contador de `0x48656c6c'6f46726f'6d536561'746f776e` . Esse valor atualizado deve então ser fornecido como uma entrada para a próxima execução desse operador.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições de tensor
`InputStateTensor` e `OutputStateTensor` devem ter os mesmos *tamanhos*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Dimensões | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputStateTensor | Entrada | {1, 1, 1, 6} | 4 | UINT32 |
| OutputTensor | Saída | {D0, D1, D2, D3} | 4 | UINT32 |
| OutputStateTensor | Saída opcional | {1, 1, 1, 6} | 4 | UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |