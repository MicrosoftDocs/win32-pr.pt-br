---
description: Representa as configurações de um sistema virtual a ser importado. Usado pelo método de desmontagem da \_ classe Msvm AssignableDeviceService.
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Classe Msvm_AssignableDeviceDismountSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5783ed9611c16d875211f29d364fe3eaff29b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750848"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a><span data-ttu-id="1294b-104">\_Classe Msvm AssignableDeviceDismountSettingData</span><span class="sxs-lookup"><span data-stu-id="1294b-104">Msvm\_AssignableDeviceDismountSettingData class</span></span>

<span data-ttu-id="1294b-105">Representa as configurações de um sistema virtual a ser importado.</span><span class="sxs-lookup"><span data-stu-id="1294b-105">Represents the settings of a virtual system to import.</span></span> <span data-ttu-id="1294b-106">Usado pelo método de [**desmontagem**](msvm-assignabledeviceservice-dismountassignabledevice.md) da classe [**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1294b-106">Used by the [**Dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) method of the [**Msvm\_AssignableDeviceService**](msvm-assignabledeviceservice.md) class.</span></span>

<span data-ttu-id="1294b-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1294b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1294b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1294b-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a><span data-ttu-id="1294b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="1294b-109">Members</span></span>

<span data-ttu-id="1294b-110">A classe **Msvm \_ AssignableDeviceDismountSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1294b-110">The **Msvm\_AssignableDeviceDismountSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1294b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1294b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1294b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1294b-112">Properties</span></span>

<span data-ttu-id="1294b-113">A classe **Msvm \_ AssignableDeviceDismountSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1294b-113">The **Msvm\_AssignableDeviceDismountSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1294b-114">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="1294b-114">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1294b-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1294b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1294b-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1294b-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1294b-117">ID da instância do dispositivo PNP.</span><span class="sxs-lookup"><span data-stu-id="1294b-117">PNP device instance ID.</span></span>

</dd> <dt>

<span data-ttu-id="1294b-118">**DeviceLocationPath**</span><span class="sxs-lookup"><span data-stu-id="1294b-118">**DeviceLocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1294b-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1294b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1294b-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1294b-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1294b-121">Caminho do local do dispositivo PNP.</span><span class="sxs-lookup"><span data-stu-id="1294b-121">PNP device location path.</span></span>

</dd> <dt>

<span data-ttu-id="1294b-122">**RequireAcsSupport**</span><span class="sxs-lookup"><span data-stu-id="1294b-122">**RequireAcsSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1294b-123">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1294b-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1294b-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1294b-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1294b-125">Indica se o suporte do ACS de requisito deve estar em vigor antes de permitir a desmontagem.</span><span class="sxs-lookup"><span data-stu-id="1294b-125">Indicates if the requisite ACS support should be in place before permitting the dismount.</span></span>

</dd> <dt>

<span data-ttu-id="1294b-126">**RequireDeviceMitigations**</span><span class="sxs-lookup"><span data-stu-id="1294b-126">**RequireDeviceMitigations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1294b-127">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1294b-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1294b-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1294b-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1294b-129">Indica se as atenuações de dispositivo devem estar em vigor antes de permitir a desmontagem.</span><span class="sxs-lookup"><span data-stu-id="1294b-129">Indicates if device mitigations should be in place before permitting the dismount.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1294b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1294b-130">Requirements</span></span>



| <span data-ttu-id="1294b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1294b-131">Requirement</span></span> | <span data-ttu-id="1294b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1294b-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1294b-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1294b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1294b-134">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="1294b-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1294b-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1294b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1294b-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1294b-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1294b-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1294b-137">Namespace</span></span><br/>                | <span data-ttu-id="1294b-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1294b-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1294b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1294b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1294b-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1294b-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1294b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1294b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1294b-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1294b-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1294b-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="1294b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1294b-144">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="1294b-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




