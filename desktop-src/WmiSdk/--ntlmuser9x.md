---
description: Controla o acesso remoto a versões sem suporte do Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: Classe __NTLMUser9X
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813694"
---
# <a name="__ntlmuser9x-class"></a><span data-ttu-id="76f57-103">\_\_Classe NTLMUser9X</span><span class="sxs-lookup"><span data-stu-id="76f57-103">\_\_NTLMUser9X class</span></span>

<span data-ttu-id="76f57-104">A classe de sistema **\_ \_ NTLMUser9X** controla o acesso remoto a versões sem suporte do Windows.</span><span class="sxs-lookup"><span data-stu-id="76f57-104">The **\_\_NTLMUser9X** system class controls remote access to unsupported versions of Windows.</span></span> <span data-ttu-id="76f57-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="76f57-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="76f57-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="76f57-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f57-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76f57-107">Syntax</span></span>

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="76f57-108">Membros</span><span class="sxs-lookup"><span data-stu-id="76f57-108">Members</span></span>

<span data-ttu-id="76f57-109">A classe **\_ \_ NTLMUser9X** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="76f57-109">The **\_\_NTLMUser9X** class has these types of members:</span></span>

-   [<span data-ttu-id="76f57-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="76f57-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76f57-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="76f57-111">Properties</span></span>

<span data-ttu-id="76f57-112">A classe **\_ \_ NTLMUser9X** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="76f57-112">The **\_\_NTLMUser9X** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76f57-113">**Autoridade**</span><span class="sxs-lookup"><span data-stu-id="76f57-113">**Authority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f57-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="76f57-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f57-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="76f57-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76f57-116">Domínio ao qual um nome de usuário se aplica.</span><span class="sxs-lookup"><span data-stu-id="76f57-116">Domain to which a user name applies.</span></span>

</dd> <dt>

<span data-ttu-id="76f57-117">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="76f57-117">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f57-118">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="76f57-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="76f57-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="76f57-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76f57-120">Sinalizadores de herança.</span><span class="sxs-lookup"><span data-stu-id="76f57-120">Inheritance flags.</span></span>

<dt>

<span data-ttu-id="76f57-121">0</span><span class="sxs-lookup"><span data-stu-id="76f57-121">0</span></span>
</dt> <dd>

<span data-ttu-id="76f57-122">Nenhuma herança.</span><span class="sxs-lookup"><span data-stu-id="76f57-122">No inheritance.</span></span>

</dd> <dt>

<span data-ttu-id="76f57-123">2</span><span class="sxs-lookup"><span data-stu-id="76f57-123">2</span></span>
</dt> <dd>

<span data-ttu-id="76f57-124">Aplicar a namespaces filho, além do atual.</span><span class="sxs-lookup"><span data-stu-id="76f57-124">Apply to child namespaces, in addition to the current one.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="76f57-125">**Mask**</span><span class="sxs-lookup"><span data-stu-id="76f57-125">**Mask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f57-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="76f57-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="76f57-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="76f57-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76f57-128">Bitmask que especifica os direitos de acesso ao namespace no repositório Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="76f57-128">Bitmask that specifies access rights to the namespace in the Windows Management Instrumentation (WMI) repository.</span></span> <span data-ttu-id="76f57-129">Para valores de bit, consulte [**constantes de direitos de acesso de namespace**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="76f57-129">For bit values, see [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="76f57-130">**Nome**</span><span class="sxs-lookup"><span data-stu-id="76f57-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f57-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="76f57-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f57-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="76f57-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76f57-133">Nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="76f57-133">User name.</span></span>

</dd> <dt>

<span data-ttu-id="76f57-134">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="76f57-134">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f57-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="76f57-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="76f57-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="76f57-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76f57-137">Acesso permitido.</span><span class="sxs-lookup"><span data-stu-id="76f57-137">Access allowed.</span></span>

<dt>

<span data-ttu-id="76f57-138">0</span><span class="sxs-lookup"><span data-stu-id="76f57-138">0</span></span>
</dt> <dd>

<span data-ttu-id="76f57-139">Acesso permitido.</span><span class="sxs-lookup"><span data-stu-id="76f57-139">Access allowed.</span></span>

</dd> <dt>

<span data-ttu-id="76f57-140">2</span><span class="sxs-lookup"><span data-stu-id="76f57-140">2</span></span>
</dt> <dd>

<span data-ttu-id="76f57-141">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="76f57-141">Access denied.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76f57-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="76f57-142">Remarks</span></span>

<span data-ttu-id="76f57-143">A classe **\_ \_ NTLMUser9X** é usada como um parâmetro de entrada para os métodos [**\_ \_ SystemSecurity:: Get9XUserList**](--systemsecurity-get9xuserlist.md) e [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) .</span><span class="sxs-lookup"><span data-stu-id="76f57-143">The **\_\_NTLMUser9X** class is used as an input parameter for the [**\_\_SystemSecurity::Get9XUserList**](--systemsecurity-get9xuserlist.md) and [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f57-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76f57-144">Requirements</span></span>



| <span data-ttu-id="76f57-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="76f57-145">Requirement</span></span> | <span data-ttu-id="76f57-146">Valor</span><span class="sxs-lookup"><span data-stu-id="76f57-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="76f57-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76f57-147">Minimum supported client</span></span><br/> | <span data-ttu-id="76f57-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76f57-148">Windows Vista</span></span><br/>       |
| <span data-ttu-id="76f57-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76f57-149">Minimum supported server</span></span><br/> | <span data-ttu-id="76f57-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76f57-150">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="76f57-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="76f57-151">Namespace</span></span><br/>                | <span data-ttu-id="76f57-152">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="76f57-152">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="76f57-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="76f57-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f57-154">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="76f57-154">**\_\_SecurityRelatedClass**</span></span>](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[<span data-ttu-id="76f57-155">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="76f57-155">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="76f57-156">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="76f57-156">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

