---
description: A \_ \_ classe de sistema abstrata de confiança representa um confiável. Um nome ou um SID (matriz de bytes) pode ser usado.
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: Classe __Trustee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
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
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506299"
---
# <a name="__trustee-class"></a><span data-ttu-id="6d233-104">\_\_Classe de confiança</span><span class="sxs-lookup"><span data-stu-id="6d233-104">\_\_Trustee class</span></span>

<span data-ttu-id="6d233-105">A classe de sistema abstrata de [**\_ \_ confiança**](--securitydescriptor.md) representa um [*confiável*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="6d233-105">The [**\_\_Trustee**](--securitydescriptor.md) abstract system class represents a [*trustee*](/windows/desktop/SecGloss/t-gly).</span></span> <span data-ttu-id="6d233-106">Um nome ou um SID (matriz de bytes) pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="6d233-106">Either a name or an SID (byte array) can be used.</span></span>

<span data-ttu-id="6d233-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6d233-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6d233-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6d233-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d233-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d233-109">Syntax</span></span>

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="6d233-110">Membros</span><span class="sxs-lookup"><span data-stu-id="6d233-110">Members</span></span>

<span data-ttu-id="6d233-111">A classe **\_ \_ Trustee** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6d233-111">The **\_\_Trustee** class has these types of members:</span></span>

-   [<span data-ttu-id="6d233-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6d233-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d233-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6d233-113">Properties</span></span>

<span data-ttu-id="6d233-114">A classe **\_ \_ Trustee** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6d233-114">The **\_\_Trustee** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d233-115">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="6d233-115">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d233-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6d233-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d233-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6d233-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d233-118">Parte do domínio da conta.</span><span class="sxs-lookup"><span data-stu-id="6d233-118">Domain portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="6d233-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6d233-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d233-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6d233-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d233-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6d233-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d233-122">Nome da parte da conta.</span><span class="sxs-lookup"><span data-stu-id="6d233-122">Name portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="6d233-123">**SID**</span><span class="sxs-lookup"><span data-stu-id="6d233-123">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d233-124">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="6d233-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6d233-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6d233-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d233-126">O SID do confiável no formulário da matriz de bytes binários.</span><span class="sxs-lookup"><span data-stu-id="6d233-126">The SID of the trustee in the binary byte array form.</span></span>

</dd> <dt>

<span data-ttu-id="6d233-127">**SidLength**</span><span class="sxs-lookup"><span data-stu-id="6d233-127">**SidLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d233-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d233-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d233-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6d233-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d233-130">O comprimento do SID em bytes.</span><span class="sxs-lookup"><span data-stu-id="6d233-130">The length of the SID in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6d233-131">**SidString**</span><span class="sxs-lookup"><span data-stu-id="6d233-131">**SidString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d233-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6d233-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d233-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6d233-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d233-134">O SID do Trustee no formato de cadeia de caracteres, por exemplo, "S-1-1-0".</span><span class="sxs-lookup"><span data-stu-id="6d233-134">The SID of the trustee in the string format, for example, "S-1-1-0".</span></span>

</dd> <dt>

<span data-ttu-id="6d233-135">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="6d233-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d233-136">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6d233-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6d233-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6d233-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d233-138">Hora no formato [de \_ data e hora CIM](cim-datetime.md) quando o descritor de segurança foi criado.</span><span class="sxs-lookup"><span data-stu-id="6d233-138">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d233-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d233-139">Remarks</span></span>

<span data-ttu-id="6d233-140">Essa classe fornece propriedades que são herdadas pela classe de [**\_ confiança do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , que é um membro da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="6d233-140">This class provides properties that are inherited by the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="6d233-141">Para obter mais informações, consulte [objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6d233-141">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="6d233-142">Para obter mais informações sobre ACEs, consulte [componentes de controle de acesso](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="6d233-142">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d233-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d233-143">Requirements</span></span>



| <span data-ttu-id="6d233-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d233-144">Requirement</span></span> | <span data-ttu-id="6d233-145">Valor</span><span class="sxs-lookup"><span data-stu-id="6d233-145">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6d233-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d233-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6d233-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d233-147">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6d233-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d233-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6d233-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d233-149">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6d233-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d233-150">Namespace</span></span><br/>                | <span data-ttu-id="6d233-151">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="6d233-151">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6d233-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d233-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d233-153">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="6d233-153">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="6d233-154">**Confiança do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="6d233-154">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[<span data-ttu-id="6d233-155">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="6d233-155">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

