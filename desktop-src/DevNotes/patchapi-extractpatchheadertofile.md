---
description: Extrai as informações de cabeçalho de um Delta.
title: Função ExtractPatchHeaderToFileA/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 626bd53e3361f4d29cc76e17ae2788ddea3bc8b99b580196bcbf77c27a6983d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571796"
---
# <a name="extractpatchheadertofileaw-function"></a>Função ExtractPatchHeaderToFileA/W

As funções **ExtractPatchHeaderToFileA** e **ExtractPatchHeaderToFileW** extraem as informações de cabeçalho de um Delta. O Delta é fornecido como um caminho de arquivo. O cabeçalho de saída também é gravado em um caminho fornecido.

## <a name="syntax"></a>Sintaxe

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a>Parâmetros

*PatchFileName*

O nome do Delta que contém o cabeçalho.

*PatchHeaderFileName*

O nome do arquivo de cabeçalho a ser criado.

## <a name="return-value"></a>Valor retornado

Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| parâmetro | patchapi. h |
| DLL | mspatchc.dll |
| Unicode | Implementado como ExtractPatchHeaderToFileW (Unicode) e ExtractPatchHeaderToFileA (ANSI) |

## <a name="see-also"></a>Confira também

[PatchAPI](patchapi.md)
