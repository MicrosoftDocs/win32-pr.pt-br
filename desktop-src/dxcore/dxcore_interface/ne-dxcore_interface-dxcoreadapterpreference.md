---
title: DXCoreAdapterPreference
description: Define constantes que especificam as preferências do adaptador DXCore a serem usadas como critérios de classificação de lista.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366442"
---
# <a name="dxcoreadapterpreference-enum"></a>DXCoreAdapterPreference enum

## <a name="description"></a>Descrição

Define constantes que especificam as preferências do adaptador DXCore a serem usadas como critérios de classificação de lista. Você pode classificar uma lista de adaptadores DXCore passando uma matriz de **DXCoreAdapterPreference** para [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>Campos de enumeração

### <a name="hardware"></a>Hardware

Especifica uma preferência para adaptadores de hardware (em oposição aos adaptadores de software).

### <a name="minimumpower"></a>MinimumPower

Especifica uma preferência para a GPU com capacidade mínima (como um processador gráfico integrado ou iGPU).

### <a name="highperformance"></a>HighPerformance

Especifica uma preferência para a GPU de alto desempenho, como um processador gráfico externo (xGPU), se disponível, ou dGPU (processador gráfico discreto), se disponível.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)