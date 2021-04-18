---
description: Representa a associação entre elementos gerenciados e seus recursos.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Classe Msvm_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758647"
---
# <a name="msvm_elementcapabilities-class"></a><span data-ttu-id="9fb05-103">\_Classe Msvm ElementCapabilities</span><span class="sxs-lookup"><span data-stu-id="9fb05-103">Msvm\_ElementCapabilities class</span></span>

<span data-ttu-id="9fb05-104">Representa a associação entre elementos gerenciados e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="9fb05-104">Represents the association between managed elements and their capabilities.</span></span>

<span data-ttu-id="9fb05-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9fb05-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb05-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fb05-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="9fb05-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9fb05-107">Members</span></span>

<span data-ttu-id="9fb05-108">A classe **Msvm \_ ElementCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9fb05-108">The **Msvm\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="9fb05-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9fb05-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fb05-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9fb05-110">Properties</span></span>

<span data-ttu-id="9fb05-111">A classe **Msvm \_ ElementCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9fb05-111">The **Msvm\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fb05-112">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="9fb05-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb05-113">Tipo de dados: **[ **\_ recursos CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9fb05-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="9fb05-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9fb05-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb05-115">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="9fb05-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9fb05-116">O objeto Capabilities associado ao elemento.</span><span class="sxs-lookup"><span data-stu-id="9fb05-116">The capabilities object associated with the element.</span></span> <span data-ttu-id="9fb05-117">Essa propriedade é herdada do [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="9fb05-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="9fb05-118">**Características**</span><span class="sxs-lookup"><span data-stu-id="9fb05-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb05-119">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fb05-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9fb05-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9fb05-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fb05-121">Fornece informações descritivas sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="9fb05-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="9fb05-122">Essa propriedade é herdada do [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="9fb05-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="9fb05-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9fb05-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="9fb05-124">Significado</span><span class="sxs-lookup"><span data-stu-id="9fb05-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="9fb05-125"><dt>**Padrão**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9fb05-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="9fb05-126">Os recursos associados representam os recursos padrão do elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9fb05-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="9fb05-127"><dt>**Atual**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9fb05-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="9fb05-128">Os recursos associados representam os recursos atuais do elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9fb05-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9fb05-129">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="9fb05-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb05-130">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="9fb05-130">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="9fb05-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9fb05-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb05-132">Qualificadores: **chave**, **mín** . (1)</span><span class="sxs-lookup"><span data-stu-id="9fb05-132">Qualifiers: **Key**, **Min** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="9fb05-133">O elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9fb05-133">The managed element.</span></span> <span data-ttu-id="9fb05-134">Essa propriedade é herdada do [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="9fb05-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fb05-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fb05-135">Remarks</span></span>

<span data-ttu-id="9fb05-136">O acesso à classe **Msvm \_ ElementCapabilities** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="9fb05-136">Access to the **Msvm\_ElementCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9fb05-137">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9fb05-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fb05-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fb05-138">Requirements</span></span>



| <span data-ttu-id="9fb05-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb05-139">Requirement</span></span> | <span data-ttu-id="9fb05-140">Valor</span><span class="sxs-lookup"><span data-stu-id="9fb05-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb05-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb05-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb05-142">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9fb05-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9fb05-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb05-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb05-144">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9fb05-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9fb05-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fb05-145">Namespace</span></span><br/>                | <span data-ttu-id="9fb05-146">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9fb05-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9fb05-147">MOF</span><span class="sxs-lookup"><span data-stu-id="9fb05-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fb05-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fb05-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fb05-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9fb05-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fb05-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9fb05-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9fb05-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fb05-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb05-152">**\_ELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="9fb05-152">**CIM\_ElementCapabilities**</span></span>](cim-elementcapabilities.md)
</dt> <dt>

[<span data-ttu-id="9fb05-153">**\_ELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="9fb05-153">**CIM\_ElementCapabilities**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[<span data-ttu-id="9fb05-154">**Msvm \_ ElementCapabilities (v1)**</span><span class="sxs-lookup"><span data-stu-id="9fb05-154">**Msvm\_ElementCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

