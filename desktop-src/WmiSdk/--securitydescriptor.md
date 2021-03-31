---
description: Representa um descritor de segurança.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: Classe __SecurityDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169810"
---
# <a name="__securitydescriptor-class"></a><span data-ttu-id="fa2d3-103">\_\_Classe SecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="fa2d3-103">\_\_SecurityDescriptor class</span></span>

<span data-ttu-id="fa2d3-104">A classe de sistema abstrata **\_ \_ SecurityDescriptor** representa um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="fa2d3-104">The **\_\_SecurityDescriptor** abstract system class represents a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="fa2d3-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fa2d3-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa2d3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa2d3-107">Syntax</span></span>

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="fa2d3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="fa2d3-108">Members</span></span>

<span data-ttu-id="fa2d3-109">A classe **\_ \_ SecurityDescriptor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fa2d3-109">The **\_\_SecurityDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="fa2d3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa2d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa2d3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa2d3-111">Properties</span></span>

<span data-ttu-id="fa2d3-112">A classe **\_ \_ SecurityDescriptor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-112">The **\_\_SecurityDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa2d3-113">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-113">**ControlFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2d3-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa2d3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa2d3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa2d3-116">Sinalizadores de bits que fornecem informações sobre o conteúdo e o formato do descritor.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-116">Bit flags that provide information about the descriptor's contents and format.</span></span> <span data-ttu-id="fa2d3-117">Consulte a propriedade **ControlFlags** na classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) para obter uma descrição dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-117">See the **ControlFlags** property in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class for a description of the flags.</span></span>

</dd> <dt>

<span data-ttu-id="fa2d3-118">**DACL**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-118">**DACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2d3-119">Tipo de dados: matriz **[**\_ \_ Ace**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-119">Data type: **[**\_\_ACE**](--ace.md)** array</span></span>
</dt> <dt>

<span data-ttu-id="fa2d3-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa2d3-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa2d3-121">Uma matriz de entradas de [**\_ \_ Ace**](--ace.md) que especificam o acesso ao objeto.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-121">An array of [**\_\_ACE**](--ace.md) entries that specify access to the object.</span></span>

</dd> <dt>

<span data-ttu-id="fa2d3-122">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-122">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2d3-123">Tipo de dados: **[ **\_ \_ Ace**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-123">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fa2d3-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa2d3-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa2d3-125">ACE que identifica os objetos de confiança que representam o grupo do objeto.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-125">ACE that identifies the trustee representing the group of the object.</span></span>

</dd> <dt>

<span data-ttu-id="fa2d3-126">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-126">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2d3-127">Tipo de dados: **[ **\_ \_ Ace**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-127">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fa2d3-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa2d3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa2d3-129">ACE que identifica os objetos de confiança que representam o proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-129">ACE that identifies the trustee representing the owner of the object.</span></span>

</dd> <dt>

<span data-ttu-id="fa2d3-130">**Right**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-130">**SACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2d3-131">Tipo de dados: **[ **\_ \_ Ace**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-131">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fa2d3-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa2d3-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa2d3-133">Uma matriz de entradas de [**\_ \_ Ace**](--ace.md) que identifica usuários e grupos para os quais as informações de auditoria são coletadas.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-133">An array of [**\_\_ACE**](--ace.md) entries that identifies users and groups for which auditing information is gathered.</span></span>

</dd> <dt>

<span data-ttu-id="fa2d3-134">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2d3-135">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa2d3-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa2d3-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa2d3-137">Hora no formato [de \_ data e hora CIM](cim-datetime.md) quando o descritor de segurança foi criado.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-137">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa2d3-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa2d3-138">Remarks</span></span>

<span data-ttu-id="fa2d3-139">Essa classe fornece propriedades herdadas por [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="fa2d3-139">This class provides properties inherited by [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="fa2d3-140">Para obter mais informações, consulte [objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fa2d3-140">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="fa2d3-141">Para obter mais informações sobre ACEs, consulte [componentes de controle de acesso](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="fa2d3-141">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2d3-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa2d3-142">Requirements</span></span>



| <span data-ttu-id="fa2d3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa2d3-143">Requirement</span></span> | <span data-ttu-id="fa2d3-144">Valor</span><span class="sxs-lookup"><span data-stu-id="fa2d3-144">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fa2d3-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa2d3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2d3-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa2d3-146">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fa2d3-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa2d3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2d3-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa2d3-148">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="fa2d3-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa2d3-149">Namespace</span></span><br/>                | <span data-ttu-id="fa2d3-150">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="fa2d3-150">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="fa2d3-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa2d3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2d3-152">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="fa2d3-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="fa2d3-153">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-153">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="fa2d3-154">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="fa2d3-154">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

