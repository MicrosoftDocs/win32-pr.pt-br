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
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a><span data-ttu-id="bf0ce-107">IDeviceAccessPolicyCheck: método eviceInterfaceClassAccessCheckWithCallingThread de:D</span><span class="sxs-lookup"><span data-stu-id="bf0ce-107">IDeviceAccessPolicyCheck::DeviceInterfaceClassAccessCheckWithCallingThread method</span></span>

> [!Important]  
> <span data-ttu-id="bf0ce-108">Essas interfaces não têm suporte e não devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="bf0ce-109">Em vez disso, use as APIs na [referência de programação C++ de API de acesso ao dispositivo](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="bf0ce-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="bf0ce-110">Essa API determinará se o token para o contexto atual tem acesso à classe de interface do dispositivo especificada.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-110">This API will determine if the token for the current context has access to the device interface class specified.</span></span> <span data-ttu-id="bf0ce-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0ce-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf0ce-112">Syntax</span></span>

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a><span data-ttu-id="bf0ce-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf0ce-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0ce-114">*pszDeviceInterfaceClassGuid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf0ce-114">*pszDeviceInterfaceClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0ce-115">GUID de classe da interface do dispositivo para o qual o acesso deve ser verificado.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-115">Device interface class GUID for which access should be checked.</span></span>

</dd> <dt>

<span data-ttu-id="bf0ce-116">*dwClientThreadId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf0ce-116">*dwClientThreadId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0ce-117">ID de thread do cliente em que qualquer interface do usuário associada deve ser mostrada, se necessário.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-117">Client thread ID where any associated UI should be shown if necessary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0ce-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf0ce-118">Return value</span></span>

<span data-ttu-id="bf0ce-119">Se essa função for realizada com sucesso, ela retornará S_OK.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-119">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="bf0ce-120">Caso contrário, ele retorna um código de erro HRESULT.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-120">Otherwise, it returns an HRESULT error code.</span></span>
