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
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105791094"
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
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | DeliveryOptimizationDownloadTypes. h |
