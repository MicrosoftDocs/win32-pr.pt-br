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
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365341"
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
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |
