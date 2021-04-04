---
title: 'Método IDODownloadInternal:: SetPropertyEx'
description: Define uma propriedade de download estendido. O método aceita um ponteiro para uma **variante** que contém um valor de propriedade específico a ser aplicado ao download.
keywords:
- 'Método IDODownloadInternal:: SetPropertyEx'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917353"
---
# <a name="idodownloadinternalsetpropertyex-method"></a>Método IDODownloadInternal:: SetPropertyEx

> [!IMPORTANT]
> A interface **IDODownloadInternal** foi preterida. Em vez disso, use a interface [IDODownload](../do/nn-do-idodownload.md) .

Define uma propriedade de download estendido. O método aceita um ponteiro para uma **variante** que contém um valor de propriedade específico a ser aplicado ao download.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parâmetros

`propId`

A ID de propriedade necessária a ser definida (do tipo **DODownloadPropertyEx**).

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
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | DODownloadInternal. h |