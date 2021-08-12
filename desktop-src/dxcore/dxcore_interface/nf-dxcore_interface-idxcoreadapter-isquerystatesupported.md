---
title: IDXCoreAdapter::IsQueryStateSupported
description: Determina se esse objeto de adaptador DXCore e o sistema operacional atual são suportados para consultar o valor do estado do adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8ae77c308cb251982947d91e23eaef8f6d828c1233df442cb013bf9737e3c57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279217"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a>Método IDXCoreAdapter::IsQueryStateSupported

Determina se esse objeto de adaptador DXCore e o sistema operacional atual são suportados para consultar o valor do estado do adaptador especificado.

## <a name="syntax"></a>Sintaxe

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

O tipo de item de estado para o qual você está consultando o suporte. Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado do adaptador.

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna se esse objeto de adaptador DXCore e o sistema operacional atual são suportados para consultar o `true` estado do adaptador especificado. Caso contrário, retorna `false`.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [Referência de DXCore,](../dxcore-reference.md)atributo de adaptador [DXCore GUIDs](../dxcore-adapter-attribute-guids.md), usando [DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)