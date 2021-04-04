---
description: Representa os dados de configuração do recurso RDMA da porta.
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Classe Msvm_EthernetSwitchPortRdmaSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837516"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a><span data-ttu-id="ba290-103">\_Classe Msvm EthernetSwitchPortRdmaSettingData</span><span class="sxs-lookup"><span data-stu-id="ba290-103">Msvm\_EthernetSwitchPortRdmaSettingData class</span></span>

<span data-ttu-id="ba290-104">Representa os dados de configuração do recurso RDMA da porta.</span><span class="sxs-lookup"><span data-stu-id="ba290-104">Represents the port RDMA feature setting data.</span></span>

<span data-ttu-id="ba290-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ba290-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba290-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba290-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="ba290-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ba290-107">Members</span></span>

<span data-ttu-id="ba290-108">A classe **Msvm \_ EthernetSwitchPortRdmaSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ba290-108">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ba290-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ba290-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba290-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ba290-110">Properties</span></span>

<span data-ttu-id="ba290-111">A classe **Msvm \_ EthernetSwitchPortRdmaSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ba290-111">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba290-112">**RdmaOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="ba290-112">**RdmaOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba290-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba290-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba290-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ba290-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba290-115">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ba290-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ba290-116">O peso atribuído a essa porta para RDMA de convidado.</span><span class="sxs-lookup"><span data-stu-id="ba290-116">The weight assigned to this port for Guest RDMA.</span></span> <span data-ttu-id="ba290-117">O peso é a importância relativa ao atribuir recursos RDMA.</span><span class="sxs-lookup"><span data-stu-id="ba290-117">The weight is the relative importance when assigning RDMA resources.</span></span> <span data-ttu-id="ba290-118">Definir a propriedade **RdmaOffloadWeight** como 0 DESABILITA o RDMA na porta.</span><span class="sxs-lookup"><span data-stu-id="ba290-118">Setting the **RdmaOffloadWeight** property to 0 disables RDMA on the port.</span></span> <span data-ttu-id="ba290-119">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="ba290-119">The default is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba290-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba290-120">Requirements</span></span>



| <span data-ttu-id="ba290-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba290-121">Requirement</span></span> | <span data-ttu-id="ba290-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ba290-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba290-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba290-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ba290-124">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="ba290-124">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ba290-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba290-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ba290-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ba290-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ba290-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba290-127">Namespace</span></span><br/>                | <span data-ttu-id="ba290-128">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ba290-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ba290-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ba290-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba290-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba290-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba290-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ba290-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba290-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba290-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ba290-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba290-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba290-134">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="ba290-134">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

 




