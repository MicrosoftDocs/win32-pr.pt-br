---
description: Representa uma ACE (entrada de controle de acesso).
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: Classe __ACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461318"
---
# <a name="__ace-class"></a><span data-ttu-id="1f25d-103">\_\_Classe ACE</span><span class="sxs-lookup"><span data-stu-id="1f25d-103">\_\_ACE class</span></span>

<span data-ttu-id="1f25d-104">A classe de sistema abstrato **\_ \_ Ace** representa uma [*Ace*](/windows/desktop/SecGloss/a-gly)(entrada de controle de acesso).</span><span class="sxs-lookup"><span data-stu-id="1f25d-104">The **\_\_ACE** abstract system class represents an access control entry ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span></span>

<span data-ttu-id="1f25d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1f25d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1f25d-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1f25d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f25d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f25d-107">Syntax</span></span>

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a><span data-ttu-id="1f25d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1f25d-108">Members</span></span>

<span data-ttu-id="1f25d-109">A classe **\_ \_ Ace** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1f25d-109">The **\_\_ACE** class has these types of members:</span></span>

-   [<span data-ttu-id="1f25d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f25d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f25d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f25d-111">Properties</span></span>

<span data-ttu-id="1f25d-112">A classe **\_ \_ Ace** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1f25d-112">The **\_\_ACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f25d-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="1f25d-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f25d-114">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1f25d-114">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="1f25d-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1f25d-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f25d-116">Sinalizadores de bits que representam direitos que são concedidos ou negados ao confiável.</span><span class="sxs-lookup"><span data-stu-id="1f25d-116">Bit flags representing rights that are granted or denied to the trustee.</span></span> <span data-ttu-id="1f25d-117">Para obter mais informações e uma descrição dos sinalizadores, consulte a propriedade **AccessMask** na classe do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="1f25d-117">For more information and a description of the flags, see **AccessMask** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="1f25d-118">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="1f25d-118">**AceFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f25d-119">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1f25d-119">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="1f25d-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1f25d-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f25d-121">Sinalizadores de bit que especificam a herança da ACE.</span><span class="sxs-lookup"><span data-stu-id="1f25d-121">Bit flags specifying the inheritance of the ACE.</span></span> <span data-ttu-id="1f25d-122">Para obter mais informações e uma descrição dos sinalizadores, consulte Propriedade **AceFlags** na classe do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="1f25d-122">For more information and a description of the flags, see **AceFlags** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="1f25d-123">**AceType**</span><span class="sxs-lookup"><span data-stu-id="1f25d-123">**AceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f25d-124">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1f25d-124">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="1f25d-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1f25d-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f25d-126">O tipo de entrada da ACE que essa instância representa.</span><span class="sxs-lookup"><span data-stu-id="1f25d-126">The type of ACE entry that this instance represents.</span></span>

</dd> <dt>

<span data-ttu-id="1f25d-127">**GuidInheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="1f25d-127">**GuidInheritedObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f25d-128">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1f25d-128">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="1f25d-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1f25d-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f25d-130">O GUID do pai do objeto ao qual os direitos de acesso na propriedade **AccessMask** se aplicam.</span><span class="sxs-lookup"><span data-stu-id="1f25d-130">The GUID of the parent of the object to which the access rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="1f25d-131">**GuidObjectType**</span><span class="sxs-lookup"><span data-stu-id="1f25d-131">**GuidObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f25d-132">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1f25d-132">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="1f25d-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1f25d-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f25d-134">O GUID que indica o tipo de objeto ao qual os direitos na propriedade **AccessMask** se aplicam.</span><span class="sxs-lookup"><span data-stu-id="1f25d-134">The GUID that indicates the type of object to which the rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="1f25d-135">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="1f25d-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f25d-136">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f25d-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f25d-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f25d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f25d-138">A hora, no formato [de \_ data e hora CIM](cim-datetime.md) , quando o descritor de segurança foi criado.</span><span class="sxs-lookup"><span data-stu-id="1f25d-138">The time, in the [CIM\_DATETIME](cim-datetime.md) format, when the security descriptor was created.</span></span>

</dd> <dt>

<span data-ttu-id="1f25d-139">**Confiança**</span><span class="sxs-lookup"><span data-stu-id="1f25d-139">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f25d-140">Tipo de dados: **[ **\_ \_ Trustee**](--trustee.md)**</span><span class="sxs-lookup"><span data-stu-id="1f25d-140">Data type: **[**\_\_Trustee**](--trustee.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1f25d-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1f25d-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f25d-142">O Trustee da entrada Ace representada por essa instância da classe **\_ \_ Ace** .</span><span class="sxs-lookup"><span data-stu-id="1f25d-142">The trustee of the ACE entry represented by this instance of the **\_\_ACE** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f25d-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f25d-143">Remarks</span></span>

<span data-ttu-id="1f25d-144">Essa classe fornece as propriedades que são herdadas pela classe [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , que é um membro da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="1f25d-144">This class provides the properties that are inherited by the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="1f25d-145">Para obter mais informações, consulte [objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1f25d-145">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="1f25d-146">Para obter mais informações sobre ACEs, consulte [componentes de controle de acesso](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="1f25d-146">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f25d-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f25d-147">Requirements</span></span>



| <span data-ttu-id="1f25d-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f25d-148">Requirement</span></span> | <span data-ttu-id="1f25d-149">Valor</span><span class="sxs-lookup"><span data-stu-id="1f25d-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1f25d-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f25d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="1f25d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f25d-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1f25d-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f25d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="1f25d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f25d-153">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1f25d-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f25d-154">Namespace</span></span><br/>                | <span data-ttu-id="1f25d-155">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="1f25d-155">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1f25d-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f25d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f25d-157">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="1f25d-157">**\_\_SecurityRelatedClass**</span></span>](--securityrelatedclass.md)
</dt> <dt>

[<span data-ttu-id="1f25d-158">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="1f25d-158">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="1f25d-159">**Ace do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="1f25d-159">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="1f25d-160">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="1f25d-160">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

