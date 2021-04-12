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
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365345"
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
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |
