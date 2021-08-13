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
ms.openlocfilehash: 8775b7daf55d58698d00bcaa2820b909e302933c9f407d1cb6416d6b095a872b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543730"
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
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | Do. h |
