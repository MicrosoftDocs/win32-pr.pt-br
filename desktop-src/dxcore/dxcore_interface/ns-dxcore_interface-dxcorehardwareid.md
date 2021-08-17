---
title: DXCoreHardwareID
description: Representa as partes de ID de hardware de PnP para um adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68cdb130dd6f0c0338e5b94da2f68c58f98bb91d404871e18ac82e817881117c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118623"
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