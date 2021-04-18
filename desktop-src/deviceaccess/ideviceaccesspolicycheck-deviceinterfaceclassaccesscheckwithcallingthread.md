---
title: Método IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread
description: Essa API determinará se o token para o contexto atual tem acesso à classe de interface do dispositivo especificada. 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B DE IID.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- API do agente de acesso ao dispositivo do método DeviceInterfaceClassAccessCheckWithCallingThread
- Método DeviceInterfaceClassAccessCheckWithCallingThread API do agente de acesso ao dispositivo, interface IDeviceAccessPolicyCheck
- API do agente de acesso ao dispositivo da interface IDeviceAccessPolicyCheck, método DeviceInterfaceClassAccessCheckWithCallingThread
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44eb44a83175cf8f735abfeb8cfec4de83f46bd2
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "105792890"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>IDeviceAccessPolicyCheck: método eviceInterfaceClassAccessCheckWithCallingThread de:D

> [!Important]  
> Essas interfaces não têm suporte e não devem ser usadas. Em vez disso, use as APIs na [referência de programação C++ de API de acesso ao dispositivo](device-access-api-c---programming-reference.md) .

Essa API determinará se o token para o contexto atual tem acesso à classe de interface do dispositivo especificada. IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszDeviceInterfaceClassGuid* \[ no\]
</dt> <dd>

GUID de classe da interface do dispositivo para o qual o acesso deve ser verificado.

</dd> <dt>

*dwClientThreadId* \[ no\]
</dt> <dd>

ID de thread do cliente em que qualquer interface do usuário associada deve ser mostrada, se necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for realizada com sucesso, ela retornará S_OK. Caso contrário, ele retorna um código de erro HRESULT.
