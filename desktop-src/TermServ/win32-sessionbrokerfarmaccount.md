---
title: Classe Win32_SessionBrokerFarmAccount
description: A \_ classe Win32 SessionBrokerFarmAccount não está mais disponível para uso a partir do Windows Server 2012. | Classe Win32_SessionBrokerFarmAccount
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionBrokerFarmAccount Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionBrokerFarmAccount classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663939"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="eaaab-106">\_Classe Win32 SessionBrokerFarmAccount</span><span class="sxs-lookup"><span data-stu-id="eaaab-106">Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="eaaab-107">\[A classe **Win32 \_ SessionBrokerFarmAccount** não está mais disponível para uso a partir do Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="eaaab-107">\[The **Win32\_SessionBrokerFarmAccount** class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="eaaab-108">Define uma conta do farm do agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="eaaab-108">Defines a session broker farm account.</span></span>

<span data-ttu-id="eaaab-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="eaaab-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaaab-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaaab-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a><span data-ttu-id="eaaab-111">Membros</span><span class="sxs-lookup"><span data-stu-id="eaaab-111">Members</span></span>

<span data-ttu-id="eaaab-112">A classe **Win32 \_ SessionBrokerFarmAccount** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="eaaab-112">The **Win32\_SessionBrokerFarmAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="eaaab-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="eaaab-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="eaaab-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eaaab-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eaaab-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="eaaab-115">Methods</span></span>

<span data-ttu-id="eaaab-116">A classe **Win32 \_ SessionBrokerFarmAccount** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="eaaab-116">The **Win32\_SessionBrokerFarmAccount** class has these methods.</span></span>



| <span data-ttu-id="eaaab-117">Método</span><span class="sxs-lookup"><span data-stu-id="eaaab-117">Method</span></span>                                                      | <span data-ttu-id="eaaab-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="eaaab-118">Description</span></span>                          |
|:------------------------------------------------------------|:-------------------------------------|
| [<span data-ttu-id="eaaab-119">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="eaaab-119">**DeleteEx**</span></span>](deleteex-win32-sessionbrokerfarmaccount.md) | <span data-ttu-id="eaaab-120">Exclui a conta do farm.</span><span class="sxs-lookup"><span data-stu-id="eaaab-120">Deletes the farm account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="eaaab-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eaaab-121">Properties</span></span>

<span data-ttu-id="eaaab-122">A classe **Win32 \_ SessionBrokerFarmAccount** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="eaaab-122">The **Win32\_SessionBrokerFarmAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eaaab-123">**AccountDomain**</span><span class="sxs-lookup"><span data-stu-id="eaaab-123">**AccountDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaab-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaab-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaab-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaab-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eaaab-126">O nome do domínio ao qual a conta do farm pertence.</span><span class="sxs-lookup"><span data-stu-id="eaaab-126">The name of the domain the farm account belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="eaaab-127">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="eaaab-127">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaab-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaab-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaab-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaab-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eaaab-130">O nome da conta do farm.</span><span class="sxs-lookup"><span data-stu-id="eaaab-130">The name of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="eaaab-131">**AccountPassword**</span><span class="sxs-lookup"><span data-stu-id="eaaab-131">**AccountPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaab-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaab-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaab-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaab-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eaaab-134">A senha da conta do farm.</span><span class="sxs-lookup"><span data-stu-id="eaaab-134">The password of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="eaaab-135">**AccountSPN1**</span><span class="sxs-lookup"><span data-stu-id="eaaab-135">**AccountSPN1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaab-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaab-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaab-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eaaab-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaaab-138">O primeiro SPN (nome da entidade de serviço) associado à conta do farm.</span><span class="sxs-lookup"><span data-stu-id="eaaab-138">The first service principal name (SPN) associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="eaaab-139">**AccountSPN2**</span><span class="sxs-lookup"><span data-stu-id="eaaab-139">**AccountSPN2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaab-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaab-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaab-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eaaab-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaaab-142">O segundo SPN associado à conta do farm.</span><span class="sxs-lookup"><span data-stu-id="eaaab-142">The second SPN associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="eaaab-143">**ComputerDNSName**</span><span class="sxs-lookup"><span data-stu-id="eaaab-143">**ComputerDNSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaab-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaab-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaab-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaab-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eaaab-146">O nome DNS do computador associado à conta do farm.</span><span class="sxs-lookup"><span data-stu-id="eaaab-146">The DNS name of the computer associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="eaaab-147">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="eaaab-147">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaab-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaab-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaab-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eaaab-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaaab-150">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eaaab-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eaaab-151">O nome do farm do agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="eaaab-151">The name of the session broker farm.</span></span>

</dd> <dt>

<span data-ttu-id="eaaab-152">**Manual**</span><span class="sxs-lookup"><span data-stu-id="eaaab-152">**Manual**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaab-153">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="eaaab-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eaaab-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaab-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eaaab-155">Indica se a senha da conta é atualizada manualmente.</span><span class="sxs-lookup"><span data-stu-id="eaaab-155">Indicates if the password for the account is updated manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eaaab-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaaab-156">Requirements</span></span>



| <span data-ttu-id="eaaab-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaaab-157">Requirement</span></span> | <span data-ttu-id="eaaab-158">Valor</span><span class="sxs-lookup"><span data-stu-id="eaaab-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaaab-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaaab-159">Minimum supported client</span></span><br/> | <span data-ttu-id="eaaab-160">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eaaab-160">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eaaab-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaaab-161">Minimum supported server</span></span><br/> | <span data-ttu-id="eaaab-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eaaab-162">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="eaaab-163">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="eaaab-163">End of client support</span></span><br/>    | <span data-ttu-id="eaaab-164">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eaaab-164">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eaaab-165">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="eaaab-165">End of server support</span></span><br/>    | <span data-ttu-id="eaaab-166">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eaaab-166">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="eaaab-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="eaaab-167">Namespace</span></span><br/>                | <span data-ttu-id="eaaab-168">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="eaaab-168">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="eaaab-169">MOF</span><span class="sxs-lookup"><span data-stu-id="eaaab-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaaab-170"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaaab-170"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaaab-171">DLL</span><span class="sxs-lookup"><span data-stu-id="eaaab-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaaab-172"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaaab-172"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

