---
title: Estrutura de DO_DOWNLOAD_RANGE
description: Identifica um único intervalo de bytes para baixar de um arquivo.
keywords:
- Estrutura de DO_DOWNLOAD_RANGE
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 39672bff2e3a7194f7d674b2184d5de8c9c3c601e4a7777ef31ace80f5f9f327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047114"
---
# <a name="do_download_range-structure"></a>Estrutura de DO_DOWNLOAD_RANGE

A estrutura de **DO_DOWNLOAD_RANGE** identifica um único intervalo de bytes para baixar de um arquivo. A estrutura de **DO_DOWNLOAD_RANGE** está incluída na estrutura **DO_DOWNLOAD_RANGES_INFO** para fornecer uma matriz de intervalos para download.

## <a name="syntax"></a>Sintaxe
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a>Membros

`Offset`

Deslocamento de base zero para o início do intervalo de bytes a ser baixado de um arquivo.

`Length`

O comprimento do intervalo, em bytes. Não especifique um comprimento de zero byte. Para indicar que o intervalo se estende até o final do arquivo, especifique **DO_LENGTH_TO_EOF**.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | DeliveryOptimizationDownloadTypes. h |
