---
description: Cria um Delta entre o arquivo de origem especificado e o arquivo de destino especificado.
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
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794636"
---
# <a name="createpatchfileexaw-function"></a>Função CreatePatchFileExA/W

As funções **CreatePatchFileExA** e **CreatePatchFileExW** criam um Delta entre o arquivo de origem especificado e o arquivo de destino especificado. Os arquivos de origem e de destino são fornecidos como caminhos. O Delta de saída também é gravado em um caminho fornecido. Essas funções fornecem relatórios de andamento durante o processo de criação.

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

*NewFilename*

O nome do arquivo de destino.

*PatchFileName*

O nome do Delta que é criado.

*OptionFlags*

Sinalizadores de criação.

*ProgressCallback*

Ponteiro para retorno de chamada de progresso definido pelo aplicativo.

*CallbackContext*

Ponteiro para contexto definido pelo aplicativo.

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| parâmetro | patchapi. h |
| DLL | mspatchc.dll |
| Unicode | Implementado como CreatePatchFileExW (Unicode) e CreatePatchFileExA (ANSI) |

## <a name="see-also"></a>Confira também

[PatchAPI](patchapi.md)
