---
title: IDXCoreAdapter::IsPropertySupported
description: Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à propriedade de adaptador especificada.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812420"
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

Retorna  `true`   se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à propriedade de adaptador especificada. Caso contrário, retorna  `false` .

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)