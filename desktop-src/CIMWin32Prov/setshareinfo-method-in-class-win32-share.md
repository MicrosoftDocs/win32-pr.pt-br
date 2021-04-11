---
description: SetShareInfo&\# 8194; O método de classe WMI define os parâmetros de um recurso compartilhado.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Método SetShareInfo da classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164172"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a><span data-ttu-id="2657d-103">Método SetShareInfo da classe de \_ compartilhamento do Win32</span><span class="sxs-lookup"><span data-stu-id="2657d-103">SetShareInfo method of the Win32\_Share class</span></span>

<span data-ttu-id="2657d-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** define os parâmetros de um recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="2657d-104">The **SetShareInfo** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the parameters of a shared resource.</span></span>

<span data-ttu-id="2657d-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2657d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2657d-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2657d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2657d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2657d-107">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="2657d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2657d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2657d-109">*MaximumAllowed* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2657d-109">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2657d-110">Limite do número máximo de usuários com permissão para usar este recurso simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="2657d-110">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

<span data-ttu-id="2657d-111">Exemplo: 10.</span><span class="sxs-lookup"><span data-stu-id="2657d-111">Example: 10.</span></span> <span data-ttu-id="2657d-112">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2657d-112">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="2657d-113">*Descrição* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2657d-113">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2657d-114">Comentário opcional para descrever o recurso que está sendo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="2657d-114">Optional comment to describe the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="2657d-115">*Acesso* \[ ao em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2657d-115">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2657d-116">Descritor de segurança para permissões de nível de usuário.</span><span class="sxs-lookup"><span data-stu-id="2657d-116">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="2657d-117">Um descritor de segurança contém informações sobre a permissão, o proprietário e os recursos de acesso do recurso.</span><span class="sxs-lookup"><span data-stu-id="2657d-117">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="2657d-118">Para obter mais informações, consulte [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="2657d-118">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2657d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2657d-119">Return value</span></span>

<span data-ttu-id="2657d-120">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="2657d-120">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2657d-121">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="2657d-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-122">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="2657d-122">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-123">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="2657d-123">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-124">**Nome inválido** (9)</span><span class="sxs-lookup"><span data-stu-id="2657d-124">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-125">**Nível inválido** (10)</span><span class="sxs-lookup"><span data-stu-id="2657d-125">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-126">**Parâmetro inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="2657d-126">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-127">**Compartilhamento duplicado** (22)</span><span class="sxs-lookup"><span data-stu-id="2657d-127">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-128">**Caminho Redirecionado** (23)</span><span class="sxs-lookup"><span data-stu-id="2657d-128">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-129">**Dispositivo ou diretório desconhecido** (24)</span><span class="sxs-lookup"><span data-stu-id="2657d-129">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-130">**Nome de rede não encontrado** (25)</span><span class="sxs-lookup"><span data-stu-id="2657d-130">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="2657d-131">**Outro** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="2657d-131">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2657d-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="2657d-132">Remarks</span></span>

<span data-ttu-id="2657d-133">O método **SetShareInfo** é um método de objeto dinâmico e é usado em uma ocorrência dessa classe.</span><span class="sxs-lookup"><span data-stu-id="2657d-133">**SetShareInfo** method is a dynamic object method and is used on an occurrence of this class.</span></span>

<span data-ttu-id="2657d-134">Somente os membros do grupo local Administradores ou operadores de contas ou aqueles com associação de grupo de operador de servidor, impressão ou comunicação podem executar **SetShareInfo** com êxito.</span><span class="sxs-lookup"><span data-stu-id="2657d-134">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **SetShareInfo**.</span></span> <span data-ttu-id="2657d-135">O operador Print só pode definir filas de impressora.</span><span class="sxs-lookup"><span data-stu-id="2657d-135">The print operator can only set printer queues.</span></span> <span data-ttu-id="2657d-136">O operador de comunicação só pode definir filas do dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="2657d-136">The Communication operator can only set communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="2657d-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2657d-137">Examples</span></span>

<span data-ttu-id="2657d-138">O exemplo do PowerShell a seguir atualiza o nome do compartilhamento **newShare** .</span><span class="sxs-lookup"><span data-stu-id="2657d-138">The following PowerShell sample updates the name of the **newShare** share.</span></span>


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



## <a name="requirements"></a><span data-ttu-id="2657d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2657d-139">Requirements</span></span>



| <span data-ttu-id="2657d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="2657d-140">Requirement</span></span> | <span data-ttu-id="2657d-141">Valor</span><span class="sxs-lookup"><span data-stu-id="2657d-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2657d-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2657d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2657d-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2657d-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2657d-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2657d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2657d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2657d-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2657d-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="2657d-146">Namespace</span></span><br/>                | <span data-ttu-id="2657d-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2657d-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2657d-148">MOF</span><span class="sxs-lookup"><span data-stu-id="2657d-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2657d-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2657d-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2657d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2657d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2657d-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2657d-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2657d-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="2657d-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="2657d-153">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2657d-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2657d-154">**Compartilhamento do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="2657d-154">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

