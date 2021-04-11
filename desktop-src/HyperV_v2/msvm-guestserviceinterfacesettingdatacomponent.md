---
description: Classe de associação entre um componente de interface de serviço de convidado e o recurso de serviço de convidado.
ms.assetid: 4c16c3ab-4137-40ab-be2e-f385d8e36a41
title: Classe Msvm_GuestServiceInterfaceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceSettingDataComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.GroupComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 988975fea1fd519a5e3917faeb73d345334d74b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164641"
---
# <a name="msvm_guestserviceinterfacesettingdatacomponent-class"></a><span data-ttu-id="c1727-103">\_Classe Msvm GuestServiceInterfaceSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="c1727-103">Msvm\_GuestServiceInterfaceSettingDataComponent class</span></span>

<span data-ttu-id="c1727-104">Classe de associação entre um componente de interface de serviço de convidado e o recurso de serviço de convidado.</span><span class="sxs-lookup"><span data-stu-id="c1727-104">Association class between a guest service interface component and the guest service resource.</span></span>

<span data-ttu-id="c1727-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c1727-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1727-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1727-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceSettingDataComponent : CIM_Component
{
  Msvm_GuestServiceInterfaceComponentSettingData REF GroupComponent;
  CIM_SettingData                                REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="c1727-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c1727-107">Members</span></span>

<span data-ttu-id="c1727-108">A classe **Msvm \_ GuestServiceInterfaceSettingDataComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1727-108">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="c1727-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1727-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1727-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1727-110">Properties</span></span>

<span data-ttu-id="c1727-111">A classe **Msvm \_ GuestServiceInterfaceSettingDataComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c1727-111">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1727-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c1727-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1727-113">Tipo de dados: **Msvm \_ GuestServiceInterfaceComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="c1727-113">Data type: **Msvm\_GuestServiceInterfaceComponentSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="c1727-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1727-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1727-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="c1727-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c1727-116">Um [**Msvm \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) referenciando o componente de interface do serviço convidado.</span><span class="sxs-lookup"><span data-stu-id="c1727-116">A [**Msvm\_GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) referencing the guest service interface component.</span></span>

</dd> <dt>

<span data-ttu-id="c1727-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c1727-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1727-118">Tipo de dados: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="c1727-118">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="c1727-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1727-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1727-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="c1727-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c1727-121">Um [**CIM \_ SettingData**](cim-settingdata.md) que faz referência ao recurso de serviço de convidado.</span><span class="sxs-lookup"><span data-stu-id="c1727-121">A [**CIM\_SettingData**](cim-settingdata.md) that references the guest service resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1727-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1727-122">Requirements</span></span>



| <span data-ttu-id="c1727-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1727-123">Requirement</span></span> | <span data-ttu-id="c1727-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c1727-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1727-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1727-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c1727-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c1727-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c1727-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1727-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c1727-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c1727-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c1727-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1727-129">Namespace</span></span><br/>                | <span data-ttu-id="c1727-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c1727-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c1727-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c1727-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1727-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1727-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1727-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c1727-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1727-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1727-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1727-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1727-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1727-136">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="c1727-136">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

