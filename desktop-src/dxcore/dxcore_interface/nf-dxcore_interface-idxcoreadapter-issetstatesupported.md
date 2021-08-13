---
title: IDXCoreAdapter::IsSetStateSupported
description: Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à definição do valor do estado do adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: dc63b541a552f1b01792e9f503acc7aeee03ce5ac6cc92e7b70e271ae62a50ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278974"
---
# <a name="idxcoreadapterissetstatesupported-method"></a>Método IDXCoreAdapter:: IsSetStateSupported

Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à definição do valor do estado do adaptador especificado.

## <a name="syntax"></a>Sintaxe

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

O tipo de item de estado que você está consultando sobre o suporte para. Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado de adaptador.

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna `true` se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à configuração do estado do adaptador especificado. Caso contrário, retorna `false`.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)