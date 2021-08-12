---
title: Método IDOManager::CreateDownload
description: Cria um novo download.
keywords:
- Método IDOManager::CreateDownload
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 87b78afdf5687bb60efb77815898274a8fb405f588f28b263eb1b01a752a9bc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543833"
---
# <a name="idomanagercreatedownload-method"></a>Método IDOManager::CreateDownload

Cria um novo download.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a>Parâmetros

`download`

O endereço de um ponteiro de interface **IDODownload.**

## <a name="return-value"></a>Valor Retornado

Se a função for bem-sucedida, ela **retornará S_OK**. Caso contrário, retornará um [**código de erro HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [.](/windows/desktop/com/com-error-codes-10)

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | \[Windows 10, versão 1809 Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Servidor, versão 1809 \[ Somente aplicativos Win32\] |
| **Cabeçalho** | Do.h |
