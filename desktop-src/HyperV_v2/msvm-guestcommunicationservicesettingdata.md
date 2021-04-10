---
description: Representa as configurações do serviço de comunicação de convidado.
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Classe Msvm_GuestCommunicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5506689f5b266c428a790774c1fb98a1b0413b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090672"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a><span data-ttu-id="71310-103">\_Classe Msvm GuestCommunicationServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="71310-103">Msvm\_GuestCommunicationServiceSettingData class</span></span>

<span data-ttu-id="71310-104">Representa as configurações do serviço de comunicação de convidado.</span><span class="sxs-lookup"><span data-stu-id="71310-104">Represents the settings of the guest communication service.</span></span>

<span data-ttu-id="71310-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="71310-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="71310-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71310-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a><span data-ttu-id="71310-107">Membros</span><span class="sxs-lookup"><span data-stu-id="71310-107">Members</span></span>

<span data-ttu-id="71310-108">A classe **Msvm \_ GuestCommunicationServiceSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="71310-108">The **Msvm\_GuestCommunicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="71310-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71310-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71310-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71310-110">Properties</span></span>

<span data-ttu-id="71310-111">A classe **Msvm \_ GuestCommunicationServiceSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="71310-111">The **Msvm\_GuestCommunicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71310-112">**EnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="71310-112">**EnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71310-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71310-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71310-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="71310-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="71310-115">EnabledStatePolicy é uma enumeração de inteiro que indica o estado habilitado, desabilitado ou padrão do **Msvm \_ GuestCommunicationServiceSettingData**.</span><span class="sxs-lookup"><span data-stu-id="71310-115">EnabledStatePolicy is an integer enumeration that indicates the enabled, disabled or default state of the **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="71310-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="71310-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="71310-117">O serviço de comunicação é definido como o estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="71310-117">The communication service is set to the enabled state.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="71310-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="71310-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="71310-119">O serviço de comunicação é definido como o estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="71310-119">The communication service is set to the disabled state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="71310-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Adiado** (8)</span><span class="sxs-lookup"><span data-stu-id="71310-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="71310-121">O estado do serviço de comunicação depende de **DefaultEnabledStatePolicy** em **Msvm \_ GuestCommunicationServiceSettingData**.</span><span class="sxs-lookup"><span data-stu-id="71310-121">The communication service state depends on **DefaultEnabledStatePolicy** in **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71310-122">**Nome**</span><span class="sxs-lookup"><span data-stu-id="71310-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71310-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71310-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71310-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71310-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71310-125">O GUID do serviço.</span><span class="sxs-lookup"><span data-stu-id="71310-125">The GUID of the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71310-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71310-126">Requirements</span></span>



| <span data-ttu-id="71310-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="71310-127">Requirement</span></span> | <span data-ttu-id="71310-128">Valor</span><span class="sxs-lookup"><span data-stu-id="71310-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71310-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71310-129">Minimum supported client</span></span><br/> | <span data-ttu-id="71310-130">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="71310-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="71310-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71310-131">Minimum supported server</span></span><br/> | <span data-ttu-id="71310-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="71310-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="71310-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="71310-133">Namespace</span></span><br/>                | <span data-ttu-id="71310-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="71310-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="71310-135">MOF</span><span class="sxs-lookup"><span data-stu-id="71310-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71310-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71310-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71310-137">DLL</span><span class="sxs-lookup"><span data-stu-id="71310-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71310-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71310-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="71310-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="71310-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71310-140">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="71310-140">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




