---
title: 'Método IDOManager:: EnumDownloads'
description: Recupera um ponteiro de interface para um objeto enumerador que é usado para enumerar os downloads existentes.
keywords:
- 'Método IDOManager:: EnumDownloads'
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5442196b95e654755b4f84fe85375afb8f5b9372ddae453ca4ddffb567882fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543823"
---
# <a name="idomanagerenumdownloads-method"></a>Método IDOManager:: EnumDownloads

Recupera um ponteiro de interface para um objeto enumerador que é usado para enumerar os downloads existentes.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a>Parâmetros

`category`

Opcional. O nome da propriedade a ser usada como uma categoria a ser enumerada. A passagem `nullptr` irá recuperar todos os downloads existentes. As propriedades a seguir têm suporte como uma categoria.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`ppEnum`

O endereço de um ponteiro de interface para **IEnumUnknown**, que é usado para enumerar os downloads existentes. O conteúdo do enumerador depende do valor da *categoria*. Os downloads incluídos na interface de enumeração são aqueles que foram criados anteriormente pelo mesmo chamador para essa função. 

## <a name="return-value"></a>Valor Retornado

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | Do. h |
