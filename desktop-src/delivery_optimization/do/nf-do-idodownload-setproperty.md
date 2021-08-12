---
title: 'Método IDODownload:: SetProperty'
description: Define uma propriedade de download.
keywords:
- 'Método IDODownload:: SetProperty'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7d966edb083107b80f0723bce195bfc588797efb8ad1931e0e75a468bec5a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543895"
---
# <a name="idodownloadsetproperty-method"></a>Método IDODownload:: SetProperty

Define uma propriedade de download. O método aceita um ponteiro para uma **variante** que contém uma propriedade específica a ser aplicada ao download.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parâmetros

`propId`

A ID de propriedade necessária a ser definida (do tipo **Dodownloadproperty**).

`propVal`

O valor da propriedade a ser definido, armazenado em uma **variante**.

## <a name="return-value"></a>Valor Retornado

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

|Valor retornado|Descrição|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* é desconhecido.|
|DO_E_INVALID_STATE|O download não está atualmente em um estado que permita a configuração de propriedades.|

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | Do. h |
