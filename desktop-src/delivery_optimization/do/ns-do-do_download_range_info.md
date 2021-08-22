---
title: Estrutura de DO_DOWNLOAD_RANGE_INFO
description: Identifica uma matriz de intervalos de bytes a serem baixados de um arquivo.
keywords:
- Estrutura de DO_DOWNLOAD_RANGE_INFO
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 30df22c7232ad1d28315e8152396ddd92bdab9a7cbf67d748af134c0f0760c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543740"
---
# <a name="do_download_range_info-structure"></a>Estrutura de DO_DOWNLOAD_RANGE_INFO

A estrutura de **DO_DOWNLOAD_RANGE_INFO** identifica uma matriz de intervalos de bytes a serem baixados de um arquivo. Normalmente, ele é passado como um argumento opcional para a função **IDODownload:: Start** .

## <a name="syntax"></a>Sintaxe
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a>Membros

`RangeCount`

Número de elementos em intervalos.

`Ranges`

Matriz de uma ou mais estruturas de **DO_DOWNLOAD_RANGE** que especificam os intervalos a serem baixados.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | Do. h |
