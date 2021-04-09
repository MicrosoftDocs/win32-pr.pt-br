---
description: Define direitos padrão, específicos e genéricos. Esses direitos são usados nas ACEs (entradas de controle de acesso) e são os principais meios de especificar o acesso solicitado ou concedido a um objeto.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091521"
---
# <a name="access_mask"></a><span data-ttu-id="20d6e-104">máscara de acesso \_</span><span class="sxs-lookup"><span data-stu-id="20d6e-104">ACCESS\_MASK</span></span>

<span data-ttu-id="20d6e-105">O tipo de dados **\_ máscara de acesso** é um valor **DWORD** que define direitos padrão, específicos e genéricos.</span><span class="sxs-lookup"><span data-stu-id="20d6e-105">The **ACCESS\_MASK** data type is a **DWORD** value that defines standard, specific, and generic rights.</span></span> <span data-ttu-id="20d6e-106">Esses direitos são usados nas ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) e são os principais meios de especificar o acesso solicitado ou concedido a um objeto.</span><span class="sxs-lookup"><span data-stu-id="20d6e-106">These rights are used in [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and are the primary means of specifying the requested or granted access to an object.</span></span>


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a><span data-ttu-id="20d6e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="20d6e-107">Remarks</span></span>

<span data-ttu-id="20d6e-108">Os bits nesse valor são alocados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="20d6e-108">The bits in this value are allocated as follows.</span></span>



| <span data-ttu-id="20d6e-109">Bits</span><span class="sxs-lookup"><span data-stu-id="20d6e-109">Bits</span></span>             | <span data-ttu-id="20d6e-110">Significado</span><span class="sxs-lookup"><span data-stu-id="20d6e-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d6e-111">0 15</span><span class="sxs-lookup"><span data-stu-id="20d6e-111">0 15</span></span><br/>  | <span data-ttu-id="20d6e-112">Direitos específicos.</span><span class="sxs-lookup"><span data-stu-id="20d6e-112">Specific rights.</span></span> <span data-ttu-id="20d6e-113">Contém a máscara de acesso específica ao tipo de objeto associado à máscara.</span><span class="sxs-lookup"><span data-stu-id="20d6e-113">Contains the access mask specific to the object type associated with the mask.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="20d6e-114">16 23</span><span class="sxs-lookup"><span data-stu-id="20d6e-114">16 23</span></span><br/> | <span data-ttu-id="20d6e-115">Direitos padrão.</span><span class="sxs-lookup"><span data-stu-id="20d6e-115">Standard rights.</span></span> <span data-ttu-id="20d6e-116">Contém os direitos de acesso padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="20d6e-116">Contains the object's standard access rights.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="20d6e-117">24</span><span class="sxs-lookup"><span data-stu-id="20d6e-117">24</span></span><br/>    | <span data-ttu-id="20d6e-118">Acesso à segurança do sistema (**\_ \_ segurança do sistema de acesso**).</span><span class="sxs-lookup"><span data-stu-id="20d6e-118">Access system security (**ACCESS\_SYSTEM\_SECURITY**).</span></span> <span data-ttu-id="20d6e-119">Ele é usado para indicar acesso a uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="20d6e-119">It is used to indicate access to a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="20d6e-120">Esse tipo de acesso requer que o processo de chamada tenha o privilégio **\_ \_ nome de segurança de se** (gerenciar auditoria e log de segurança).</span><span class="sxs-lookup"><span data-stu-id="20d6e-120">This type of access requires the calling process to have the **SE\_SECURITY\_NAME** (Manage auditing and security log) privilege.</span></span> <span data-ttu-id="20d6e-121">Se esse sinalizador for definido na máscara de acesso de uma ACE de acesso de auditoria (acesso bem-sucedido ou malsucedido), o acesso à SACL será auditado.</span><span class="sxs-lookup"><span data-stu-id="20d6e-121">If this flag is set in the access mask of an audit access ACE (successful or unsuccessful access), the SACL access will be audited.</span></span><br/> |
| <span data-ttu-id="20d6e-122">25</span><span class="sxs-lookup"><span data-stu-id="20d6e-122">25</span></span><br/>    | <span data-ttu-id="20d6e-123">Máximo permitido (**máximo \_ permitido**).</span><span class="sxs-lookup"><span data-stu-id="20d6e-123">Maximum allowed (**MAXIMUM\_ALLOWED**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="20d6e-124">26 27</span><span class="sxs-lookup"><span data-stu-id="20d6e-124">26 27</span></span><br/> | <span data-ttu-id="20d6e-125">Reservado.</span><span class="sxs-lookup"><span data-stu-id="20d6e-125">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="20d6e-126">28</span><span class="sxs-lookup"><span data-stu-id="20d6e-126">28</span></span><br/>    | <span data-ttu-id="20d6e-127">Todos genéricos (**\_ todos genéricos**).</span><span class="sxs-lookup"><span data-stu-id="20d6e-127">Generic all (**GENERIC\_ALL**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="20d6e-128">29</span><span class="sxs-lookup"><span data-stu-id="20d6e-128">29</span></span><br/>    | <span data-ttu-id="20d6e-129">Execução genérica (**\_ execução genérica**).</span><span class="sxs-lookup"><span data-stu-id="20d6e-129">Generic execute (**GENERIC\_EXECUTE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="20d6e-130">30</span><span class="sxs-lookup"><span data-stu-id="20d6e-130">30</span></span><br/>    | <span data-ttu-id="20d6e-131">Gravação genérica (**\_ gravação genérica**).</span><span class="sxs-lookup"><span data-stu-id="20d6e-131">Generic write (**GENERIC\_WRITE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="20d6e-132">31</span><span class="sxs-lookup"><span data-stu-id="20d6e-132">31</span></span><br/>    | <span data-ttu-id="20d6e-133">Leitura genérica (**\_ leitura genérica**).</span><span class="sxs-lookup"><span data-stu-id="20d6e-133">Generic read (**GENERIC\_READ**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="20d6e-134">Os bits de direitos padrão, 16 a 23, contêm os direitos de acesso padrão do objeto e podem ser uma combinação dos seguintes sinalizadores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="20d6e-134">Standard rights bits, 16 to 23, contain the object's standard access rights and can be a combination of the following predefined flags.</span></span>



| <span data-ttu-id="20d6e-135">bit</span><span class="sxs-lookup"><span data-stu-id="20d6e-135">Bit</span></span>           | <span data-ttu-id="20d6e-136">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="20d6e-136">Flag</span></span>                         | <span data-ttu-id="20d6e-137">Significado</span><span class="sxs-lookup"><span data-stu-id="20d6e-137">Meaning</span></span>                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d6e-138">16</span><span class="sxs-lookup"><span data-stu-id="20d6e-138">16</span></span><br/> | <span data-ttu-id="20d6e-139">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="20d6e-139">**DELETE**</span></span><br/>        | <span data-ttu-id="20d6e-140">Excluir acesso.</span><span class="sxs-lookup"><span data-stu-id="20d6e-140">Delete access.</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="20d6e-141">17</span><span class="sxs-lookup"><span data-stu-id="20d6e-141">17</span></span><br/> | <span data-ttu-id="20d6e-142">**controle de leitura \_**</span><span class="sxs-lookup"><span data-stu-id="20d6e-142">**READ\_CONTROL**</span></span><br/> | <span data-ttu-id="20d6e-143">Acesso de leitura ao proprietário, grupo e [*lista de controle de acesso discricional*](/windows/desktop/SecGloss/d-gly) (DACL) do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="20d6e-143">Read access to the owner, group, and [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the security descriptor.</span></span><br/> |
| <span data-ttu-id="20d6e-144">18</span><span class="sxs-lookup"><span data-stu-id="20d6e-144">18</span></span><br/> | <span data-ttu-id="20d6e-145">**GRAVAR \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="20d6e-145">**WRITE\_DAC**</span></span><br/>    | <span data-ttu-id="20d6e-146">Acesso de gravação à DACL.</span><span class="sxs-lookup"><span data-stu-id="20d6e-146">Write access to the DACL.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="20d6e-147">19</span><span class="sxs-lookup"><span data-stu-id="20d6e-147">19</span></span><br/> | <span data-ttu-id="20d6e-148">**proprietário da gravação \_**</span><span class="sxs-lookup"><span data-stu-id="20d6e-148">**WRITE\_OWNER**</span></span><br/>  | <span data-ttu-id="20d6e-149">Acesso de gravação ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="20d6e-149">Write access to owner.</span></span><br/>                                                                                                                                                                                                        |
| <span data-ttu-id="20d6e-150">20</span><span class="sxs-lookup"><span data-stu-id="20d6e-150">20</span></span><br/> | <span data-ttu-id="20d6e-151">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="20d6e-151">**SYNCHRONIZE**</span></span><br/>   | <span data-ttu-id="20d6e-152">Sincronizar o acesso.</span><span class="sxs-lookup"><span data-stu-id="20d6e-152">Synchronize access.</span></span><br/>                                                                                                                                                                                                           |



 

<span data-ttu-id="20d6e-153">As constantes a seguir definidas em Winnt. h representam os direitos de acesso padrão e específicos.</span><span class="sxs-lookup"><span data-stu-id="20d6e-153">The following constants defined in Winnt.h represent the specific and standard access rights.</span></span>


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a><span data-ttu-id="20d6e-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20d6e-154">Requirements</span></span>



| <span data-ttu-id="20d6e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="20d6e-155">Requirement</span></span> | <span data-ttu-id="20d6e-156">Valor</span><span class="sxs-lookup"><span data-stu-id="20d6e-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d6e-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20d6e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="20d6e-158">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="20d6e-158">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="20d6e-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20d6e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="20d6e-160">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="20d6e-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="20d6e-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20d6e-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="20d6e-162"><dt>Winnt. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20d6e-162"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20d6e-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="20d6e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d6e-164">Controle de acesso</span><span class="sxs-lookup"><span data-stu-id="20d6e-164">Access Control</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="20d6e-165">Estruturas de controle de acesso básicas</span><span class="sxs-lookup"><span data-stu-id="20d6e-165">Basic Access Control Structures</span></span>](authorization-structures.md)
</dt> <dt>

[<span data-ttu-id="20d6e-166">Direitos de acesso e máscaras de acesso</span><span class="sxs-lookup"><span data-stu-id="20d6e-166">Access Rights and Access Masks</span></span>](access-rights-and-access-masks.md)
</dt> <dt>

[<span data-ttu-id="20d6e-167">**\_mapeamento genérico**</span><span class="sxs-lookup"><span data-stu-id="20d6e-167">**GENERIC\_MAPPING**</span></span>](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

