---
title: 'Método IDODownload:: Finalize'
description: Finaliza o download.
keywords:
- 'Método IDODownload:: Finalize'
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 620b8cf1671c18f2e4a79a798fac366d61c9e09f5a83ecda2c1ade531c6a558a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636026"
---
# <a name="idodownloadfinalize-method"></a>Método IDODownload:: Finalize

Finaliza o download. Depois de finalizado, um download não pode ser retomado chamando **Start**.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | Do. h |
