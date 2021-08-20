---
title: 'Método IDODownloadInternal:: GetPropertyEx'
description: Recupera um ponteiro para uma **variante** que contém um valor de propriedade de download estendido específico.
keywords:
- 'Método IDODownloadInternal:: GetPropertyEx'
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e812c82d1159651f7ad8567f0039555835f32911c9f5a8a92b6cedd3fb84dcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101668"
---
# <a name="idodownloadinternalgetpropertyex-method"></a>Método IDODownloadInternal:: GetPropertyEx

> [!IMPORTANT]
> A interface **IDODownloadInternal** foi preterida. Em vez disso, use a interface [IDODownload](../do/nn-do-idodownload.md) .

Recupera um ponteiro para uma **variante** que contém um valor de propriedade de download estendido específico.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parâmetros

`propId`

A ID de propriedade necessária para Get (do tipo **DODownloadPropertyEx**).

`propVal`

O valor da propriedade resultante, armazenado em uma **variante**.

## <a name="return-value"></a>Valor Retornado

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

|Valor retornado|Descrição|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* é desconhecido.|
|DO_E_WRITE_ONLY_PROPERTY|A propriedade é somente gravação e não pode ser lida.|
|E_NOT_SET|Essa propriedade não foi definida por meio de **SetPropertyEx**.|

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | DODownloadInternal. h |