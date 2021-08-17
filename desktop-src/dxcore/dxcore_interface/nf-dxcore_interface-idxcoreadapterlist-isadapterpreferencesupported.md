---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Determina se um valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado é compreendido pelo sistema operacional.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: f8a42040ecd6c5667a3d33fb506fd97cfdfe53e8950c2e42b6068bbed6c19467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502577"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>Método IDXCoreAdapterList:: IsAdapterPreferenceSupported

## <a name="description"></a>Descrição

Determina se um valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado é compreendido pelo sistema operacional atual (SO). Você pode chamar **IsAdapterPreferenceSupported** antes de chamar [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Sintaxe

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a>Parâmetros

### <a name="preference"></a>preferência

Tipo: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**

Um valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) que será verificado para ver se há suporte pelo sistema operacional.

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna `true` se o tipo de classificação é compreendido pelo sistema operacional atual. Caso contrário, retorna `false`.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)