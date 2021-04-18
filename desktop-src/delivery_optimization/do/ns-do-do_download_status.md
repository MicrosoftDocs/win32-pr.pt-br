---
title: Estrutura de DO_DOWNLOAD_STATUS
description: Usado para obter o status de um download específico.
keywords:
- Estrutura de DO_DOWNLOAD_STATUS
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105785975"
---
# <a name="do_download_status-structure"></a>Estrutura de DO_DOWNLOAD_STATUS

A estrutura de **DO_DOWNLOAD_STATUS** é usada para obter o status de um download específico. É obtido chamando a função **IDODownload:: GetStatus** .

## <a name="syntax"></a>Sintaxe
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a>Membros

`BytesTotal`

O número total de bytes a serem baixados.

`BytesTransferred`

O número de bytes que já foram baixados.

`State`

O estado de download atual, conforme definido pela enumeração **Dodownloadstate** .

`Error`

As informações de erro (se houver) que estão associadas ao download atual.

`ExtendedError`

As informações de erro estendidas (se existir) que estão associadas ao download atual.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |
