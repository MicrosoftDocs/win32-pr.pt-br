---
description: Associa um comutador Ethernet virtual às extensões atualmente associadas a ele.
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Classe Msvm_HostedEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cb952d42864fb6130ad6cbec09ef5eb68439f6a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647370"
---
# <a name="msvm_hostedethernetswitchextension-class"></a><span data-ttu-id="8b603-103">\_Classe Msvm HostedEthernetSwitchExtension</span><span class="sxs-lookup"><span data-stu-id="8b603-103">Msvm\_HostedEthernetSwitchExtension class</span></span>

<span data-ttu-id="8b603-104">Associa um comutador Ethernet virtual às extensões atualmente associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="8b603-104">Associates a virtual Ethernet switch to the extensions currently bound to it.</span></span>

<span data-ttu-id="8b603-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8b603-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b603-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b603-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8b603-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8b603-107">Members</span></span>

<span data-ttu-id="8b603-108">A classe **Msvm \_ HostedEthernetSwitchExtension** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8b603-108">The **Msvm\_HostedEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="8b603-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b603-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b603-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b603-110">Properties</span></span>

<span data-ttu-id="8b603-111">A classe **Msvm \_ HostedEthernetSwitchExtension** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8b603-111">The **Msvm\_HostedEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b603-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="8b603-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b603-113">Tipo de dados: **[ **Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="8b603-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="8b603-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b603-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b603-115">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8b603-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8b603-116">Uma referência a uma instância da classe [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa o comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="8b603-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="8b603-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="8b603-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b603-118">Tipo de dados: **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="8b603-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="8b603-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b603-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b603-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8b603-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8b603-121">Uma referência a uma instância da classe [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa a instância de extensão do comutador associada ao comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="8b603-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the switch extension instance bound to the virtual switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b603-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b603-122">Requirements</span></span>



| <span data-ttu-id="8b603-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b603-123">Requirement</span></span> | <span data-ttu-id="8b603-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8b603-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b603-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b603-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8b603-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8b603-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8b603-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b603-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8b603-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8b603-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b603-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b603-129">Namespace</span></span><br/>                | <span data-ttu-id="8b603-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8b603-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8b603-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8b603-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b603-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b603-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b603-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8b603-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b603-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b603-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

