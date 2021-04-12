---
title: Método IDeviceBroker OpenDeviceFromInterfacePath
description: Tenta abrir uma instância de interface de dispositivo em nome de um cliente. 8604b268-34A6-4b1A-A59F-CDBD8379FD98 de IID.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- API do agente de acesso ao dispositivo do método OpenDeviceFromInterfacePath
- Método OpenDeviceFromInterfacePath API do agente de acesso ao dispositivo, interface IDeviceBroker
- API do agente de acesso ao dispositivo da interface IDeviceBroker, método OpenDeviceFromInterfacePath
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365511"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>Método IDeviceBroker:: OpenDeviceFromInterfacePath

> [!Important]  
> Essas interfaces não têm suporte e não devem ser usadas. Em vez disso, use as APIs na [referência de programação C++ de API de acesso ao dispositivo](device-access-api-c---programming-reference.md) .

Tenta abrir uma instância de interface de dispositivo em nome de um cliente. IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszDeviceInterfacePath* \[ no\]
</dt> <dd>

Instância da interface do dispositivo a ser aberta.

</dd> <dt>

*desiredAccess* \[ no\]
</dt> <dd>

Acesso desejado a ser passado para abrir.

</dd> <dt>

*ShareMode* \[ no\]
</dt> <dd>

Modo de compartilhamento a ser passado para abrir.

</dd> <dt>

*flagsAndAttributes* \[ no\]
</dt> <dd>

Sinalizadores e atributos a serem passados para abrir.

</dd> <dt>

*\* phDevice* \[ out\]
</dt> <dd>

Identificador resultante se abrir foi bem-sucedido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for realizada com sucesso, ela retornará S_OK. Caso contrário, ele retorna um código de erro HRESULT.
