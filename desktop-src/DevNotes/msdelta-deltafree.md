---
description: Libera o bloco de memória especificado.
title: Função DeltaFree
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 606b8d91d20c74f7dd56ff4e09986abec3eef547989990a38bd8b4e3a27382c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079726"
---
# <a name="deltafree-function"></a>Função DeltaFree

Libera o bloco de memória especificado. Você deve chamar essa função após chamadas bem-sucedidas para [CreateDeltaB](msdelta-createdeltab.md) e [ApplyDeltaB](msdelta-applydeltab.md) para liberar o buffer de memória alocado MSDelta.

## <a name="syntax"></a>Sintaxe

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>Parâmetros

*lpMemory*

no Bloco de memória a ser liberado.

## <a name="return-value"></a>Valor retornado

Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**. Quando a função retorna **false**, você pode chamar [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o código de erro do sistema Win32 correspondente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| parâmetro | msdelta. h |
| DLL | msdelta.dll |
| Unicode | Não se aplica |

## <a name="see-also"></a>Confira também

[MSDelta](msdelta.md)

[CreateDeltaB](msdelta-createdeltab.md)

[ApplyDeltaB](msdelta-applydeltab.md)
