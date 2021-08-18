---
title: Método IDODownload::Abort
description: Anula o download.
keywords:
- Método IDODownload::Abort
topic_type:
- apiref
api_name:
- IDODownload.Abort
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 70ca7d25b702de8cd11214daf5d70491113d2f68959a9d48c5b4d0c97bc97dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543973"
---
# <a name="idodownloadabort-method"></a>Método IDODownload::Abort

Anula o download.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT Abort();
```

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela **retornará S_OK**. Caso contrário, retornará um [**código de erro HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [.](/windows/desktop/com/com-error-codes-10)

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | \[Windows 10, versão 1809 Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Servidor, versão 1809 \[ Somente aplicativos Win32\] |
| **Cabeçalho** | Do.h |
