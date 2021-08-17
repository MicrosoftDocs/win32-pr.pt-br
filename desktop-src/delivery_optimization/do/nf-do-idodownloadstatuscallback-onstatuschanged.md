---
title: Método IDODownloadStatusCallback::OnStatusChange
description: O DO chama sua implementação desse método sempre que um status de download é alterado.
keywords:
- Método IDODownloadStatusCallback::OnStatusChange
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0395b6bc64ad3abe102a0a4f0dc7afd8e8d59f336949a3b97eaf683a4f4900cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736204"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>Método IDODownloadStatusCallback::OnStatusChange

O DO chama sua implementação desse método sempre que um status de download é alterado.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parâmetros

`download`

Um ponteiro para a interface **IDODownload** cujo status foi alterado.

`status`

Um ponteiro para uma **DO_DOWNLOAD_STATUS** que contém o status do download.

## <a name="return-value"></a>Valor Retornado

Se a função for bem-sucedida, ela **retornará S_OK**. Caso contrário, retornará um [**código de erro HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [.](/windows/desktop/com/com-error-codes-10)

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | \[Windows 10, versão 1809 Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Servidor, versão 1809 \[ Somente aplicativos Win32\] |
| **Cabeçalho** | Do.h |
