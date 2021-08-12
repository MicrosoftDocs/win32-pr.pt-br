---
title: IDXCoreAdapter::IsPropertySupported
description: Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à propriedade de adaptador especificada.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ddee6bea5af8fb64dfa2bfc15392e92239e7326b34cbd93cbd112559a6027912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279227"
---
# <a name="idxcoreadapterispropertysupported-method"></a>Método IDXCoreAdapter:: IsPropertySupported

Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à propriedade de adaptador especificada.

## <a name="syntax"></a>Sintaxe

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="property"></a>propriedade

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

O tipo de propriedade que você está consultando sobre o suporte para. Consulte a tabela em [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) para obter mais informações sobre cada propriedade de adaptador.

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna `true` se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à propriedade de adaptador especificada. Caso contrário, retorna `false`.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)