---
description: Conecta um serviço de ponte transparente a uma entrada de encaminhamento dinâmico (endereço MAC aprendido).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Classe Msvm_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 01b9d9c752d4781864c07ff24fca5f866a57ae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921167"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="fbf02-103">\_Classe Msvm TransparentBridgingDynamicForwarding</span><span class="sxs-lookup"><span data-stu-id="fbf02-103">Msvm\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="fbf02-104">Conecta um serviço de ponte transparente a uma entrada de encaminhamento dinâmico (endereço MAC aprendido).</span><span class="sxs-lookup"><span data-stu-id="fbf02-104">Connects a transparent bridging service to a dynamic forward entry (learned MAC address).</span></span>

<span data-ttu-id="fbf02-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fbf02-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf02-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbf02-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fbf02-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fbf02-107">Members</span></span>

<span data-ttu-id="fbf02-108">A classe **Msvm \_ TransparentBridgingDynamicForwarding** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fbf02-108">The **Msvm\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="fbf02-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fbf02-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fbf02-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fbf02-110">Properties</span></span>

<span data-ttu-id="fbf02-111">A classe **Msvm \_ TransparentBridgingDynamicForwarding** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fbf02-111">The **Msvm\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fbf02-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="fbf02-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf02-113">Tipo de dados: **[ **Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span><span class="sxs-lookup"><span data-stu-id="fbf02-113">Data type: **[**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fbf02-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbf02-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf02-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="fbf02-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fbf02-116">Uma referência a uma instância da classe [**Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) que representa o serviço de ponte transparente.</span><span class="sxs-lookup"><span data-stu-id="fbf02-116">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="fbf02-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="fbf02-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf02-118">Tipo de dados: **[ **Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="fbf02-118">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fbf02-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbf02-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf02-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="fbf02-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fbf02-121">Uma referência a uma instância da classe [**Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) que representa a entrada de encaminhamento dinâmico do banco de dados de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="fbf02-121">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbf02-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbf02-122">Remarks</span></span>

<span data-ttu-id="fbf02-123">O acesso à classe **Msvm \_ TransparentBridgingDynamicForwarding** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="fbf02-123">Access to the **Msvm\_TransparentBridgingDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fbf02-124">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fbf02-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf02-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbf02-125">Requirements</span></span>



| <span data-ttu-id="fbf02-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbf02-126">Requirement</span></span> | <span data-ttu-id="fbf02-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fbf02-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf02-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbf02-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf02-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fbf02-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fbf02-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbf02-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf02-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fbf02-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbf02-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbf02-132">Namespace</span></span><br/>                | <span data-ttu-id="fbf02-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fbf02-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fbf02-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf02-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf02-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbf02-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf02-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf02-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf02-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbf02-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fbf02-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbf02-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf02-139">**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="fbf02-139">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[<span data-ttu-id="fbf02-140">**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="fbf02-140">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

