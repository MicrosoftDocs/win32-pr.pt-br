---
title: 'Método IDODownload:: GetStatus'
description: Recupera um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** que reflete o status atual do download.
keywords:
- 'Método IDODownload:: GetStatus'
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e3a5aec5e35187a51865e074dae26ff012b75dfa3a41ffd13a8bed7371515fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047104"
---
# <a name="idodownloadgetstatus-method"></a>Método IDODownload:: GetStatus

Recupera um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** que reflete o status atual do download.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parâmetros

`status`

Um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** .

## <a name="return-value"></a>Valor Retornado

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | Do. h |
