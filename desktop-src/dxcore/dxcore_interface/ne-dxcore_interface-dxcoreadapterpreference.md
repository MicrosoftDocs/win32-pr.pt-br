---
title: DXCoreAdapterPreference
description: Define constantes que especificam as preferências do adaptador DXCore a serem usadas como critérios de classificação de lista.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: a58f2c948751d5217a89e52bc862057ac6a67c85bdf2fabed96c2b5ad68364cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117726"
---
# <a name="dxcoreadapterpreference-enum"></a>Enum DXCoreAdapterPreference

## <a name="description"></a>Descrição

Define constantes que especificam as preferências do adaptador DXCore a serem usadas como critérios de classificação de lista. Você pode classificar uma lista de adaptadores DXCore passando uma matriz **de DXCoreAdapterPreference** para [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>Campos de enum

### <a name="hardware"></a>Hardware

Especifica uma preferência para adaptadores de hardware (em vez de adaptadores de software).

### <a name="minimumpower"></a>MinimumPower

Especifica uma preferência para a GPU de potência mínima (como um processador gráfico integrado ou iGPU).

### <a name="highperformance"></a>HighPerformance

Especifica uma preferência para a GPU de alto desempenho, como um xGPU (processador gráfico externo), se disponível, ou dGPU (processador gráfico discreto), se disponível.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)