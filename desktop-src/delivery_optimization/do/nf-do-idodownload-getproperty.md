---
title: 'Método IDODownload:: GetProperty'
description: Recupera um ponteiro para uma **variante** que contém uma propriedade de download específica.
keywords:
- 'Método IDODownload:: GetProperty'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: f498900e8dd2e87460a5fe4e75ea1269272788488159379d64f5332f2006f97a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736243"
---
# <a name="idodownloadgetproperty-method"></a>Método IDODownload:: GetProperty

Recupera um ponteiro para uma **variante** que contém uma propriedade de download específica.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parâmetros

`propId`

A ID de propriedade necessária para Get (do tipo **Dodownloadproperty**).

`propVal`

O valor da propriedade resultante, armazenado em uma **variante**.

## <a name="return-value"></a>Valor Retornado

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

|Valor retornado|Descrição|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* é desconhecido.|
|DO_E_WRITE_ONLY_PROPERTY|A propriedade é somente gravação e não pode ser lida.|
|E_NOT_SET|Essa propriedade não foi definida por meio de **SetProperty**.|

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | Do. h |
