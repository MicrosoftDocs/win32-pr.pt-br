---
description: Representa os dados de configuração do recurso de mapeamento da equipe de porta.
ms.assetid: 7c9a392d-c95e-4b0d-8201-e50adabd21b2
title: Classe Msvm_EthernetSwitchPortTeamMappingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortTeamMappingSettingData
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterName
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterDeviceId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f0d7385499dcdf6e84c361de03950a4e78be0a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755102"
---
# <a name="msvm_ethernetswitchportteammappingsettingdata-class"></a><span data-ttu-id="82e9f-103">\_Classe Msvm EthernetSwitchPortTeamMappingSettingData</span><span class="sxs-lookup"><span data-stu-id="82e9f-103">Msvm\_EthernetSwitchPortTeamMappingSettingData class</span></span>

<span data-ttu-id="82e9f-104">Representa os dados de configuração do recurso de mapeamento da equipe de porta.</span><span class="sxs-lookup"><span data-stu-id="82e9f-104">Represents the port team mapping feature setting data.</span></span>

<span data-ttu-id="82e9f-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="82e9f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e9f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82e9f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8D45D4BD-8C18-435C-98A7-D632A7C618FF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Team Mapping Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortTeamMappingSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string NetAdapterName = "";
  string NetAdapterDeviceId = "";
};
```

## <a name="members"></a><span data-ttu-id="82e9f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="82e9f-107">Members</span></span>

<span data-ttu-id="82e9f-108">A classe **Msvm \_ EthernetSwitchPortTeamMappingSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="82e9f-108">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="82e9f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82e9f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82e9f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82e9f-110">Properties</span></span>

<span data-ttu-id="82e9f-111">A classe **Msvm \_ EthernetSwitchPortTeamMappingSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="82e9f-111">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82e9f-112">**NetAdapterDeviceId**</span><span class="sxs-lookup"><span data-stu-id="82e9f-112">**NetAdapterDeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82e9f-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="82e9f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82e9f-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="82e9f-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="82e9f-115">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="82e9f-115">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="82e9f-116">ID do dispositivo do adaptador físico mapeado preferencial.</span><span class="sxs-lookup"><span data-stu-id="82e9f-116">Device ID of the preferred mapped physical adapter.</span></span>

</dd> <dt>

<span data-ttu-id="82e9f-117">**Netadaptadorname**</span><span class="sxs-lookup"><span data-stu-id="82e9f-117">**NetAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82e9f-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="82e9f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82e9f-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="82e9f-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="82e9f-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="82e9f-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="82e9f-121">Nome do adaptador físico mapeado preferencial.</span><span class="sxs-lookup"><span data-stu-id="82e9f-121">Name of the preferred mapped physical adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82e9f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82e9f-122">Requirements</span></span>



| <span data-ttu-id="82e9f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="82e9f-123">Requirement</span></span> | <span data-ttu-id="82e9f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="82e9f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e9f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82e9f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="82e9f-126">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="82e9f-126">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="82e9f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82e9f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="82e9f-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82e9f-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="82e9f-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="82e9f-129">Namespace</span></span><br/>                | <span data-ttu-id="82e9f-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="82e9f-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="82e9f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="82e9f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82e9f-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82e9f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82e9f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="82e9f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82e9f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82e9f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82e9f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="82e9f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e9f-136">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="82e9f-136">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

