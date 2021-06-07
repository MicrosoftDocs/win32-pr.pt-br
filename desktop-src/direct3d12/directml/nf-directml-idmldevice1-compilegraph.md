---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compila um grafo de operadores DirectML em um objeto que pode ser expedido para a GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416918"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>Método IDMLDevice1::CompileGraph (directml.h)

Compila um grafo de operadores DirectML em um objeto que pode ser expedido para a GPU.

Um operador compilado representa a forma eficiente e cozida de um operador adequado para execução na GPU. Um operador compilado mantém o estado (como sombreadores e outros objetos) necessário para execução. Como um operador compilado implementa a interface [IDMLPageable,](/windows/win32/api/directml/nn-directml-idmlpageable) você poderá rebaí-la da memória da GPU, se desejar. Consulte [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) para obter mais informações.

O operador compilado não usa nem referencia os [objetos IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) fornecidos na descrição do grafo depois que esse método retorna.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a>Parâmetros

`desc`

Tipo: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***

Uma descrição do grafo a ser compilado. Consulte [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).

`flags`

Tipo: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

Todos os sinalizadores para controlar a execução desse operador.

`riid`

Tipo: <b>REFIID</b>

Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar no <i>ppv.</i> Espera-se que esse seja o GUID [de IDMLCompiledOperator.](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)

`ppv`

Tipo: <b>void**</b>

Um ponteiro para um bloco de memória que recebe um ponteiro para o operador compilado. Esse é o endereço de um ponteiro para [um IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), que representa o operador compilado criado.


## <a name="return-value"></a>Retornar valor

Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Se esse método for bem-sucedido, ele **retornará S_OK**. Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

A API do grafo do operador DirectML fornece uma maneira abstrata de usar o DirectML com eficiência em vários hardwares. O DirectML aplica otimizações de nível tensor, como escolher o layout tensor mais eficiente com base no adaptador que está sendo usado. Ele também aplica otimizações como a remoção de operadores Join ou Split.

Recomendamos que você aplique otimizações de alto nível antes de criar um grafo DirectML. Por exemplo, fusão de operadores convolução com BatchNorm, dobramento constante e eliminação de subexpressão comum. As otimizações no otimizador de grafo do DirectML destinam-se a complementar essas otimizações independentes de dispositivo, que normalmente são tratadas genericamente por estruturas de aprendizado de máquina.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | directml.h |
| **Biblioteca** | DirectML.lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Confira também

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)