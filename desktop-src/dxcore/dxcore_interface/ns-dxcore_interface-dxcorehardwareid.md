---
title: DXCoreHardwareID
description: Representa as partes de ID de hardware de PnP para um adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084609"
---
# <a name="dxcorehardwareid-structure"></a>Estrutura DXCoreHardwareID

Representa as partes de ID de hardware de PnP para um adaptador.

## <a name="syntax"></a>Sintaxe

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a>Membros

### <a name="vendorid"></a>vendorId

Tipo: **uint32_t \***

A ID de PCI do fornecedor de hardware do adaptador.

### <a name="deviceid"></a>deviceId

Tipo: **uint32_t \***

A ID de PCI do dispositivo de hardware do adaptador.

### <a name="subsysid"></a>subSysId

Tipo: **uint32_t \***

A ID de PCI do subsistema de hardware do adaptador.

### <a name="revision"></a>revisão

Tipo: **uint32_t \***

A ID de PCI do número de revisão do adaptador.

## <a name="see-also"></a>Confira também

[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)