---
description: Usa o Delta e a origem (fornecidos como buffers) para criar uma nova cópia dos dados de destino. Os dados de saída são retornados em um buffer MSDelta alocado.
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
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812434"
---
# <a name="applydeltab-function"></a>Função ApplyDeltaB

Usa o Delta e a origem (fornecidos como buffers) para criar uma nova cópia dos dados de destino. Os dados de saída são retornados em um buffer MSDelta alocado.

> [!NOTE]
> Você deve chamar [DeltaFree](msdelta-deltafree.md) para liberar o buffer de saída após a conclusão dessa função.

> [!NOTE]
> Se o Delta especificado tiver sido criado usando [PatchAPI](patchapi.md)e o sinalizador [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) for definido, MSDelta chamará PatchAPI para aplicar o Delta.

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

no [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) ou [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Origem*

no Uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados de origem.

*Delta*

no Uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados Delta.

*lpTarget*

fora Ponteiro para a estrutura de [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) onde o destino deve ser gravado.

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**. Quando a função retorna **false**, você pode chamar [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o código de erro do sistema Win32 correspondente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| parâmetro | msdelta. h |
| DLL | msdelta.dll |
| Unicode | Não aplicável |

## <a name="see-also"></a>Confira também

[MSDelta](msdelta.md)

[DeltaFree](msdelta-deltafree.md)
