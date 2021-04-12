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
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a><span data-ttu-id="386d6-107">Método IDeviceBroker:: OpenDeviceFromInterfacePath</span><span class="sxs-lookup"><span data-stu-id="386d6-107">IDeviceBroker::OpenDeviceFromInterfacePath method</span></span>

> [!Important]  
> <span data-ttu-id="386d6-108">Essas interfaces não têm suporte e não devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="386d6-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="386d6-109">Em vez disso, use as APIs na [referência de programação C++ de API de acesso ao dispositivo](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="386d6-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="386d6-110">Tenta abrir uma instância de interface de dispositivo em nome de um cliente.</span><span class="sxs-lookup"><span data-stu-id="386d6-110">Attempts to open a device interface instance on behalf of a client.</span></span> <span data-ttu-id="386d6-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span><span class="sxs-lookup"><span data-stu-id="386d6-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span></span>

## <a name="syntax"></a><span data-ttu-id="386d6-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="386d6-112">Syntax</span></span>

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a><span data-ttu-id="386d6-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="386d6-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="386d6-114">*pszDeviceInterfacePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="386d6-114">*pszDeviceInterfacePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386d6-115">Instância da interface do dispositivo a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="386d6-115">Device interface instance to open.</span></span>

</dd> <dt>

<span data-ttu-id="386d6-116">*desiredAccess* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="386d6-116">*desiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386d6-117">Acesso desejado a ser passado para abrir.</span><span class="sxs-lookup"><span data-stu-id="386d6-117">Desired access to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="386d6-118">*ShareMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="386d6-118">*shareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386d6-119">Modo de compartilhamento a ser passado para abrir.</span><span class="sxs-lookup"><span data-stu-id="386d6-119">Share mode to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="386d6-120">*flagsAndAttributes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="386d6-120">*flagsAndAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386d6-121">Sinalizadores e atributos a serem passados para abrir.</span><span class="sxs-lookup"><span data-stu-id="386d6-121">Flags and attributes to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="386d6-122">*\* phDevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="386d6-122">*\*phDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="386d6-123">Identificador resultante se abrir foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="386d6-123">Resulting handle if open was successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="386d6-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="386d6-124">Return value</span></span>

<span data-ttu-id="386d6-125">Se essa função for realizada com sucesso, ela retornará S_OK.</span><span class="sxs-lookup"><span data-stu-id="386d6-125">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="386d6-126">Caso contrário, ele retorna um código de erro HRESULT.</span><span class="sxs-lookup"><span data-stu-id="386d6-126">Otherwise, it returns an HRESULT error code.</span></span>
