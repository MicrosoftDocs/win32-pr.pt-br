---
title: 'Método IDODownload:: Start'
description: Inicia ou retoma um download.
keywords:
- 'Método IDODownload:: Start'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b2a06de8319ac07983fd13cb8523fa1dcf92365ca9275da80b699b290a4a6435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736253"
---
# <a name="idodownloadstart-method"></a>Método IDODownload:: Start

Inicia ou retoma um download, passando intervalos opcionais como um ponteiro para [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) estrutura.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>Parâmetros

`ranges`

Opcional. Um ponteiro para uma estrutura de [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (para baixar apenas intervalos específicos do arquivo). Passe `nullptr` para baixar o arquivo inteiro.

## <a name="return-value"></a>Valor Retornado

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | Do. h |
