---
description: Conecta uma porta de comutador a uma entrada de encaminhamento dinâmico (endereço MAC aprendido).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Classe Msvm_SwitchPortDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e6dda46302e9e8c58710bad1f4221e14e2c3f4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759401"
---
# <a name="msvm_switchportdynamicforwarding-class"></a><span data-ttu-id="10846-103">\_Classe Msvm SwitchPortDynamicForwarding</span><span class="sxs-lookup"><span data-stu-id="10846-103">Msvm\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="10846-104">Conecta uma porta de comutador a uma entrada de encaminhamento dinâmico (endereço MAC aprendido).</span><span class="sxs-lookup"><span data-stu-id="10846-104">Connects a switch port to a dynamic forward entry (learned MAC address).</span></span> <span data-ttu-id="10846-105">Isso é útil na localização de todos os endereços MAC aprendidos para uma porta especificada.</span><span class="sxs-lookup"><span data-stu-id="10846-105">This is useful in finding all of the learned MAC addresses for a specified port.</span></span>

<span data-ttu-id="10846-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="10846-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="10846-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10846-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="10846-108">Membros</span><span class="sxs-lookup"><span data-stu-id="10846-108">Members</span></span>

<span data-ttu-id="10846-109">A classe **Msvm \_ SwitchPortDynamicForwarding** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="10846-109">The **Msvm\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="10846-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10846-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10846-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10846-111">Properties</span></span>

<span data-ttu-id="10846-112">A classe **Msvm \_ SwitchPortDynamicForwarding** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="10846-112">The **Msvm\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10846-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="10846-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10846-114">Tipo de dados: **[ **Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span><span class="sxs-lookup"><span data-stu-id="10846-114">Data type: **[**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="10846-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10846-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10846-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="10846-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="10846-117">Uma referência a uma instância da classe [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) que representa a porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="10846-117">A reference to an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="10846-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="10846-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10846-119">Tipo de dados: **[ **Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="10846-119">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="10846-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10846-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10846-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="10846-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="10846-122">Uma referência a uma instância da classe [**Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) que representa a entrada de encaminhamento dinâmico do banco de dados de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="10846-122">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10846-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="10846-123">Remarks</span></span>

<span data-ttu-id="10846-124">O acesso à classe **Msvm \_ SwitchPortDynamicForwarding** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="10846-124">Access to the **Msvm\_SwitchPortDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="10846-125">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="10846-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="10846-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10846-126">Examples</span></span>

<span data-ttu-id="10846-127">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="10846-127">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10846-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10846-128">Requirements</span></span>



| <span data-ttu-id="10846-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="10846-129">Requirement</span></span> | <span data-ttu-id="10846-130">Valor</span><span class="sxs-lookup"><span data-stu-id="10846-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10846-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10846-131">Minimum supported client</span></span><br/> | <span data-ttu-id="10846-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="10846-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="10846-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10846-133">Minimum supported server</span></span><br/> | <span data-ttu-id="10846-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="10846-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10846-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="10846-135">Namespace</span></span><br/>                | <span data-ttu-id="10846-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="10846-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="10846-137">MOF</span><span class="sxs-lookup"><span data-stu-id="10846-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10846-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10846-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10846-139">DLL</span><span class="sxs-lookup"><span data-stu-id="10846-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10846-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10846-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="10846-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="10846-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10846-142">**\_SWITCHPORTDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="10846-142">**CIM\_SwitchPortDynamicForwarding**</span></span>](cim-switchportdynamicforwarding.md)
</dt> <dt>

<span data-ttu-id="10846-143">[**\_SWITCHPORTDYNAMICFORWARDING CIM**](/previous-versions//cc136921(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10846-143">[**CIM\_SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))</span></span>
</dt> </dl>

 

