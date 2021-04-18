---
description: Obtém o descritor de segurança que controla o acesso ao namespace do WMI ao qual você está conectado. O descritor de segurança é retornado como uma instância de \_ \_ SecurityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor da classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765684"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="97cba-104">Método GetSecurityDescriptor da \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="97cba-104">GetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="97cba-105">O método **GetSecurityDescriptor** Obtém o descritor de segurança que controla o acesso ao namespace do WMI ao qual você está conectado.</span><span class="sxs-lookup"><span data-stu-id="97cba-105">The **GetSecurityDescriptor** method gets the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="97cba-106">O descritor de segurança é retornado como uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="97cba-106">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="97cba-107">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="97cba-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97cba-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97cba-108">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="97cba-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97cba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97cba-110">*Descritor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="97cba-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97cba-111">O descritor de segurança associado ao namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="97cba-111">The security descriptor associated with the WMI namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97cba-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97cba-112">Return value</span></span>

<span data-ttu-id="97cba-113">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="97cba-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="97cba-114">Para obter mais informações, consulte [códigos de retorno do WMI](wmi-return-codes.md) ou [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="97cba-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="97cba-115">**0**</span><span class="sxs-lookup"><span data-stu-id="97cba-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="97cba-116">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="97cba-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="97cba-117">**2**</span><span class="sxs-lookup"><span data-stu-id="97cba-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="97cba-118">O usuário não tem acesso às informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="97cba-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="97cba-119">**8**</span><span class="sxs-lookup"><span data-stu-id="97cba-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="97cba-120">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="97cba-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="97cba-121">**9**</span><span class="sxs-lookup"><span data-stu-id="97cba-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="97cba-122">O usuário não tem privilégios adequados para executar o método.</span><span class="sxs-lookup"><span data-stu-id="97cba-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="97cba-123">**Abril**</span><span class="sxs-lookup"><span data-stu-id="97cba-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="97cba-124">Um parâmetro especificado na chamada do método não é válido.</span><span class="sxs-lookup"><span data-stu-id="97cba-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97cba-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="97cba-125">Remarks</span></span>

<span data-ttu-id="97cba-126">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="97cba-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="97cba-127">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="97cba-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="97cba-128">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="97cba-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="97cba-129">Para obter mais informações, consulte [**constantes de privilégio**](privilege-constants.md) e [executando operações privilegiadas](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="97cba-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97cba-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97cba-130">Requirements</span></span>



| <span data-ttu-id="97cba-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="97cba-131">Requirement</span></span> | <span data-ttu-id="97cba-132">Valor</span><span class="sxs-lookup"><span data-stu-id="97cba-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="97cba-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97cba-133">Minimum supported client</span></span><br/> | <span data-ttu-id="97cba-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97cba-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="97cba-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97cba-135">Minimum supported server</span></span><br/> | <span data-ttu-id="97cba-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97cba-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="97cba-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="97cba-137">Namespace</span></span><br/>                | <span data-ttu-id="97cba-138">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="97cba-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="97cba-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="97cba-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97cba-140">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="97cba-140">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="97cba-141">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="97cba-141">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

