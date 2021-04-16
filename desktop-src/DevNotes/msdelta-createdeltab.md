---
description: Cria um Delta entre a origem e o destino (fornecidos como buffers) e retorna o Delta de saída como um buffer MSDelta.
title: Função CreateDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772766"
---
# <a name="createdeltab-function"></a>Função CreateDeltaB

Cria um Delta entre a origem e o destino (fornecidos como buffers) e retorna o Delta de saída como um buffer MSDelta.

> [!NOTE]
> Você deve chamar [DeltaFree](msdelta-deltafree.md) para liberar o buffer de saída após a conclusão dessa função.

## <a name="syntax"></a>Sintaxe

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a>Parâmetros

*Filetypeset*

no O valor [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) que indica o conjunto de tipos de arquivo a ser usado para o processo de criação.

*SetFlags*

no Um ou mais valores de [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especificam os sinalizadores a serem usados durante o processo de criação, além dos sinalizadores padrão.

*ResetFlags*

no Um ou mais valores de [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especificam os sinalizadores padrão a serem redefinidos durante o processo de criação.

*Origem*

no Uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados de origem.

*Target (destino)*

no Uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados de destino.

*Origemoptions*

[in] Reservado. Passe uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) com *editável* definido como **false**, *lpStart* definido como **nulo** e *uSize* definido como 0.

*Targetoptions*

[in] Reservado. Passe uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) com *editável* definido como **false**, *lpStart* definido como **nulo** e *uSize* definido como 0.

*GlobalOptions*

[in] Reservado. Passe uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) com *LpStart* definido como **nulo** e *uSize* definido como 0.

*lpTargetFileTime*

no O carimbo de data/hora definido no arquivo de destino após a aplicação Delta. Se for **NULL**, o carimbo de data/hora de destino será a hora atual durante o processo de criação.

*HashAlgId*

no ALG_ID do algoritmo a ser usado para gerar a assinatura de destino. Alguns valores especiais são:

- 0 = sem assinatura
- 32 = CRC de 32 bits definida em msdelta.dll

*lpDelta*

fora Ponteiro para a estrutura de [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) onde o Delta deve ser gravado.

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
