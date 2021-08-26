---
title: Símbolo de D3D12SDKVersion
description: O número de versão do SDK do Direct3D 12.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/25/2021
req.lib: ''
req.dll: d3d12core.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d12core.dll
api_name:
- D3D12SDKVersion
targetos: Windows
ms.openlocfilehash: 0bf0aa17e16a4274b69e80580c0615ed055dd97a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917876"
---
# <a name="d3d12sdkversion-symbol"></a>Símbolo de D3D12SDKVersion

O número de versão do SDK do Direct3D 12.

## <a name="syntax"></a>Sintaxe

```cpp
extern "C" { _declspec(dllexport) extern const UINT D3D12SDKVersion = n;}
```

## <a name="return-value"></a>Valor retornado

Um [uint](/windows/win32/winprog/windows-data-types) que contém o número de versão do SDK do Direct3D 12.

## <a name="remarks"></a>Comentários

**D3D12SDKVersion** não está associado a uma biblioteca de importação nem a um arquivo de cabeçalho.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | N/D |
| **Biblioteca** | N/D |
| **DLL** | d3d12core.dll |

## <a name="see-also"></a>Confira também
