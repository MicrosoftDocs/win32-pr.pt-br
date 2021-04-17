---
title: Classe Win32_TSIssuedLicense
description: Descreve instâncias de Serviços de Área de Trabalho Remota licenças de acesso para cliente por dispositivo (RDS \ 160; CALs por dispositivo) emitidas de um servidor de licença Área de Trabalho Remota.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSIssuedLicense Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSIssuedLicense classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784056"
---
# <a name="win32_tsissuedlicense-class"></a><span data-ttu-id="ba47e-105">\_Classe Win32 TSIssuedLicense</span><span class="sxs-lookup"><span data-stu-id="ba47e-105">Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="ba47e-106">Descreve instâncias de Serviços de Área de Trabalho Remota licenças de acesso para cliente por dispositivo (RDS CALs por dispositivo) emitidas de um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ba47e-106">Describes instances of Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are issued from a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba47e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba47e-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a><span data-ttu-id="ba47e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ba47e-108">Members</span></span>

<span data-ttu-id="ba47e-109">A classe **Win32 \_ TSIssuedLicense** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ba47e-109">The **Win32\_TSIssuedLicense** class has these types of members:</span></span>

-   [<span data-ttu-id="ba47e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ba47e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ba47e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ba47e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ba47e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ba47e-112">Methods</span></span>

<span data-ttu-id="ba47e-113">A classe **Win32 \_ TSIssuedLicense** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ba47e-113">The **Win32\_TSIssuedLicense** class has these methods.</span></span>



| <span data-ttu-id="ba47e-114">Método</span><span class="sxs-lookup"><span data-stu-id="ba47e-114">Method</span></span>                                         | <span data-ttu-id="ba47e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba47e-115">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba47e-116">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="ba47e-116">**Revoke**</span></span>](revoke-win32-tsissuedlicense.md) | <span data-ttu-id="ba47e-117">Revoga as CALs de RDS por dispositivo que são representadas pelo **objeto \_ TSIssuedLicense do Win32** .</span><span class="sxs-lookup"><span data-stu-id="ba47e-117">Revokes the RDS Per Device CALs that are represented by the **Win32\_TSIssuedLicense** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ba47e-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ba47e-118">Properties</span></span>

<span data-ttu-id="ba47e-119">A classe **Win32 \_ TSIssuedLicense** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ba47e-119">The **Win32\_TSIssuedLicense** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba47e-120">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="ba47e-120">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba47e-121">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ba47e-121">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba47e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba47e-123">Identifica a data em que a licença irá expirar.</span><span class="sxs-lookup"><span data-stu-id="ba47e-123">Identifies the date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-124">**Emitido**</span><span class="sxs-lookup"><span data-stu-id="ba47e-124">**IssueDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba47e-125">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ba47e-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba47e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba47e-127">Identifica a data em que a licença foi emitida.</span><span class="sxs-lookup"><span data-stu-id="ba47e-127">Identifies the date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-128">**Pacote de chaves**</span><span class="sxs-lookup"><span data-stu-id="ba47e-128">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba47e-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba47e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba47e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ba47e-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ba47e-132">Identifica o pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ba47e-132">Identifies the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-133">**Licenseid**</span><span class="sxs-lookup"><span data-stu-id="ba47e-133">**LicenseId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba47e-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba47e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba47e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-136">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ba47e-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ba47e-137">Identificador exclusivo desta licença.</span><span class="sxs-lookup"><span data-stu-id="ba47e-137">Unique identifier for this license.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-138">**StatusLicença**</span><span class="sxs-lookup"><span data-stu-id="ba47e-138">**LicenseStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba47e-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba47e-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba47e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba47e-141">Status da licença.</span><span class="sxs-lookup"><span data-stu-id="ba47e-141">Status of the license.</span></span>

<dt>

<span data-ttu-id="ba47e-142">0</span><span class="sxs-lookup"><span data-stu-id="ba47e-142">0</span></span>
</dt> <dd>

<span data-ttu-id="ba47e-143">O status da licença é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="ba47e-143">The license status is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-144">1</span><span class="sxs-lookup"><span data-stu-id="ba47e-144">1</span></span>
</dt> <dd>

<span data-ttu-id="ba47e-145">A licença é uma licença temporária.</span><span class="sxs-lookup"><span data-stu-id="ba47e-145">The license is a temporary license.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-146">2</span><span class="sxs-lookup"><span data-stu-id="ba47e-146">2</span></span>
</dt> <dd>

<span data-ttu-id="ba47e-147">A licença está ativa.</span><span class="sxs-lookup"><span data-stu-id="ba47e-147">The license is active.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-148">3</span><span class="sxs-lookup"><span data-stu-id="ba47e-148">3</span></span>
</dt> <dd>

<span data-ttu-id="ba47e-149">A licença é uma licença de atualização.</span><span class="sxs-lookup"><span data-stu-id="ba47e-149">The license is an upgrade license.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-150">4</span><span class="sxs-lookup"><span data-stu-id="ba47e-150">4</span></span>
</dt> <dd>

<span data-ttu-id="ba47e-151">A licença foi revogada.</span><span class="sxs-lookup"><span data-stu-id="ba47e-151">The license has been revoked.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-152">5</span><span class="sxs-lookup"><span data-stu-id="ba47e-152">5</span></span>
</dt> <dd>

<span data-ttu-id="ba47e-153">O status da licença está pendente.</span><span class="sxs-lookup"><span data-stu-id="ba47e-153">The license status is pending.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-154">6</span><span class="sxs-lookup"><span data-stu-id="ba47e-154">6</span></span>
</dt> <dd>

<span data-ttu-id="ba47e-155">A licença é uma licença simultânea.</span><span class="sxs-lookup"><span data-stu-id="ba47e-155">The license is a concurrent license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ba47e-156">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="ba47e-156">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba47e-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ba47e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba47e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba47e-159">Identificador de hardware para o qual a licença foi emitida.</span><span class="sxs-lookup"><span data-stu-id="ba47e-159">Hardware identifier for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-160">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="ba47e-160">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba47e-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ba47e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba47e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba47e-163">Nome do computador para o qual a licença foi emitida.</span><span class="sxs-lookup"><span data-stu-id="ba47e-163">Computer name for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="ba47e-164">**sIssuedToUser**</span><span class="sxs-lookup"><span data-stu-id="ba47e-164">**sIssuedToUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba47e-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ba47e-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba47e-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba47e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba47e-167">Nome de usuário para o qual a licença foi emitida.</span><span class="sxs-lookup"><span data-stu-id="ba47e-167">User name for which the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba47e-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba47e-168">Remarks</span></span>

<span data-ttu-id="ba47e-169">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="ba47e-169">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="ba47e-170">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ba47e-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ba47e-171">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ba47e-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ba47e-172">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ba47e-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ba47e-173">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ba47e-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba47e-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba47e-174">Requirements</span></span>



| <span data-ttu-id="ba47e-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba47e-175">Requirement</span></span> | <span data-ttu-id="ba47e-176">Valor</span><span class="sxs-lookup"><span data-stu-id="ba47e-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba47e-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba47e-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ba47e-178">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ba47e-178">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ba47e-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba47e-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ba47e-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba47e-180">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ba47e-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba47e-181">Namespace</span></span><br/>                | <span data-ttu-id="ba47e-182">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ba47e-182">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ba47e-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ba47e-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba47e-184"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba47e-184"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba47e-185">DLL</span><span class="sxs-lookup"><span data-stu-id="ba47e-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba47e-186"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba47e-186"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba47e-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba47e-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba47e-188">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="ba47e-188">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="ba47e-189">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="ba47e-189">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="ba47e-190">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="ba47e-190">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="ba47e-191">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="ba47e-191">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

