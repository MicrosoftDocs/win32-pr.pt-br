---
title: IDXCoreAdapter::IsQueryStateSupported
description: Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à consulta do valor do estado do adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d154597f9b3ddbec24cff230317d881b9595bcde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084744"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a>Método IDXCoreAdapter:: IsQueryStateSupported

Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à consulta do valor do estado do adaptador especificado.

## <a name="syntax"></a>Sintaxe

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

O tipo de item de estado que você está consultando sobre o suporte para. Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado de adaptador.

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna  `true`   se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à consulta do estado do adaptador especificado. Caso contrário, retorna  `false` .

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)