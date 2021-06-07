---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Define constantes que especificam a direção de uma operação ao longo do eixo especificado para o operador (por exemplo, somatório, selecionando os elementos de Top-k, selecionando o elemento mínimo).
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
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
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
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
- DML_AXIS_DIRECTION
ms.openlocfilehash: e54d2abed3843ea9b2a22cb3c385f9edd1541ba5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416936"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a>Enumeração de DML_AXIS_DIRECTION (directml. h)

Define constantes que especificam a direção de uma operação ao longo do eixo especificado para o operador (por exemplo, somatório, selecionando os elementos de Top-k, selecionando o elemento mínimo).

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a>Constantes

| Nome | Descrição |
| ---- |:---- |
| DML_AXIS_DIRECTION_INCREASING | Especifica a ordem crescente (do índice baixo para o índice alto). |
| DML_AXIS_DIRECTION_DECREASING | Especifica a ordem decrescente (do índice alto para o índice baixo). |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |