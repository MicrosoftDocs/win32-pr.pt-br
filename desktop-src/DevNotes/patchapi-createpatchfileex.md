---
description: Cria um delta entre o arquivo de origem especificado e o arquivo de destino especificado.
title: Função CreatePatchFileExA/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 7d73b6f4d10c52e9eca147227fdbfece31cba157af84fdf56dbef5cacda516b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690866"
---
# <a name="createpatchfileexaw-function"></a>Função CreatePatchFileExA/W

As **funções CreatePatchFileExA** e **CreatePatchFileExW** criam um delta entre o arquivo de origem especificado e o arquivo de destino especificado. Os arquivos de origem e de destino são fornecidos como caminhos. O delta de saída também é gravado em um caminho fornecido. Essas funções fornecem relatórios de progresso durante o processo de criação.

## <a name="syntax"></a>Sintaxe

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a>Parâmetros

*OldFileCount*

O número total de arquivos de origem. Usado para criar deltas em vários arquivos de origem (máximo de 255).

*OldFileInfoArray*

Ponteiro para a matriz de informações do arquivo de origem.

*NewFileName*

O nome do arquivo de destino.

*PatchFileName*

O nome do delta que é criado.

*OptionFlags*

Sinalizadores de criação.

*ProgressCallback*

Ponteiro para o retorno de chamada de progresso definido pelo aplicativo.

*CallbackContext*

Ponteiro para contexto definido pelo aplicativo.

## <a name="return-value"></a>Valor retornado

Essa função **retornará TRUE** se for bem-sucedida; caso contrário, retornará **FALSE.**

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| parâmetro | patchapi.h |
| DLL | mspatchc.dll |
| Unicode | Implementado como CreatePatchFileExW (Unicode) e CreatePatchFileExA (ANSI) |

## <a name="see-also"></a>Confira também

[PatchAPI](patchapi.md)
