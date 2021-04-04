---
title: 'Método IDODownloadStatusCallback:: OnStatusChange'
description: O chama sua implementação desse método sempre que um status de download for alterado.
keywords:
- 'Método IDODownloadStatusCallback:: OnStatusChange'
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
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104006950"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>Método IDODownloadStatusCallback:: OnStatusChange

O chama sua implementação desse método sempre que um status de download for alterado.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parâmetros

`download`

Um ponteiro para a interface **IDODownload** cujo status mudou.

`status`

Um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** que contém o status do download.

## <a name="return-value"></a>Valor Retornado

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |
