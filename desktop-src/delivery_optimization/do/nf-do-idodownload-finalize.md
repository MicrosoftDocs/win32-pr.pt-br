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
ms.openlocfilehash: 6befc9a7e64fb0963d45257d68d6bb8d2ba7a2cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105762222"
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
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |
