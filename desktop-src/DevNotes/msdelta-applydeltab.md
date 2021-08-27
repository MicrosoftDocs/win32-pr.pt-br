---
description: Usa o delta e a origem (fornecidos como buffers) para criar uma nova cópia dos dados de destino. Os dados de saída são retornados em um buffer alocado por MSDelta.
title: Função ApplyDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 2a6034ca101a192be66db1b16a4ac7b27e7288d9453dfaaab5782e55e11d4c67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079756"
---
# <a name="applydeltab-function"></a>Função ApplyDeltaB

Usa o delta e a origem (fornecidos como buffers) para criar uma nova cópia dos dados de destino. Os dados de saída são retornados em um buffer alocado por MSDelta.

> [!NOTE]
> Você deve chamar [DeltaFree para](msdelta-deltafree.md) liberar o buffer de saída depois que essa função tiver sido concluída.

> [!NOTE]
> Se o delta especificado tiver sido criado usando [PatchAPI](patchapi.md)e o [sinalizador DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) estiver definido, msDelta chamará PatchAPI para aplicar o delta.

## <a name="syntax"></a>Sintaxe

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a>Parâmetros

*ApplyFlags*

[in] Ou [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) ou [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Origem*

[in] Uma [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados de origem.

*Delta*

[in] Uma [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados delta.

*lpTarget*

[out] Ponteiro para a [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) local em que o destino deve ser gravado.

## <a name="return-value"></a>Valor retornado

Essa função **retornará TRUE** se for bem-sucedida; caso contrário, retornará **FALSE.** Quando a função retorna **FALSE**, você pode chamar [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o código de erro do sistema Win32 correspondente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| parâmetro | msdelta.h |
| DLL | msdelta.dll |
| Unicode | Não se aplica |

## <a name="see-also"></a>Confira também

[MSDelta](msdelta.md)

[DeltaFree](msdelta-deltafree.md)
