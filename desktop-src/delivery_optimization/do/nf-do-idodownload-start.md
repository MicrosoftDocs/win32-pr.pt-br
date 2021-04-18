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
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105816042"
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
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |
