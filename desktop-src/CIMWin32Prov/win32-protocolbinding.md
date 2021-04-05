---
description: A \_ classe WMI de associação de protocolo win32binding relaciona um driver de nível de sistema, protocolo de rede e adaptador de rede.
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Classe Win32_ProtocolBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826176"
---
# <a name="win32_protocolbinding-class"></a><span data-ttu-id="f521d-103">\_Classe de protocolobinding Win32</span><span class="sxs-lookup"><span data-stu-id="f521d-103">Win32\_ProtocolBinding class</span></span>

<span data-ttu-id="f521d-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação de **\_ protocolo win32binding** relaciona um driver de nível de sistema, protocolo de rede e adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="f521d-104">The **Win32\_ProtocolBinding** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system-level driver, network protocol, and network adapter.</span></span>

<span data-ttu-id="f521d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f521d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f521d-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="f521d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f521d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f521d-107">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a><span data-ttu-id="f521d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f521d-108">Members</span></span>

<span data-ttu-id="f521d-109">A classe de **\_ protocolo do win32binding** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f521d-109">The **Win32\_ProtocolBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="f521d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f521d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f521d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f521d-111">Properties</span></span>

<span data-ttu-id="f521d-112">A classe de **\_ Protocolobinding do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f521d-112">The **Win32\_ProtocolBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f521d-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="f521d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f521d-114">Tipo de dados: **Win32 \_ NetworkProtocol**</span><span class="sxs-lookup"><span data-stu-id="f521d-114">Data type: **Win32\_NetworkProtocol**</span></span>
</dt> <dt>

<span data-ttu-id="f521d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f521d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f521d-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkProtocol")</span><span class="sxs-lookup"><span data-stu-id="f521d-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="f521d-117">Referência à instância que representa o protocolo que é usado com o driver do sistema e no adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="f521d-117">Reference to the instance representing the protocol that is used with the system driver and on the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f521d-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="f521d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f521d-119">Tipo de dados **: \_ systemdrive do Win32**</span><span class="sxs-lookup"><span data-stu-id="f521d-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="f521d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f521d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f521d-121">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="f521d-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="f521d-122">Referência à instância que representa o driver de sistema que usa o adaptador de rede por meio do protocolo de rede dessa classe.</span><span class="sxs-lookup"><span data-stu-id="f521d-122">Reference to the instance representing the system driver that uses the network adapter through the network protocol of this class.</span></span>

</dd> <dt>

<span data-ttu-id="f521d-123">**Dispositivo**</span><span class="sxs-lookup"><span data-stu-id="f521d-123">**Device**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f521d-124">Tipo de dados: **Win32 \_ adaptador**</span><span class="sxs-lookup"><span data-stu-id="f521d-124">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="f521d-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f521d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f521d-126">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ adaptador")</span><span class="sxs-lookup"><span data-stu-id="f521d-126">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="f521d-127">Propriedades do adaptador de rede que está sendo usado no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="f521d-127">Properties of the network adapter being used on the computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f521d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f521d-128">Requirements</span></span>



| <span data-ttu-id="f521d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f521d-129">Requirement</span></span> | <span data-ttu-id="f521d-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f521d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f521d-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f521d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f521d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f521d-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f521d-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f521d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f521d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f521d-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f521d-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="f521d-135">Namespace</span></span><br/>                | <span data-ttu-id="f521d-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f521d-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f521d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f521d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f521d-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f521d-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f521d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f521d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f521d-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f521d-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f521d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f521d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f521d-142">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="f521d-142">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
