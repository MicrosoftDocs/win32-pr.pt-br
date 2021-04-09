---
title: Classe Win32_TSLicenseReport
description: Fornece instâncias de Serviços de Área de Trabalho Remota licença de acesso para cliente por usuário (RDS \ 160; CAL por usuário) relatórios de uso que são gerados no servidor de licença Área de Trabalho Remota e métodos para operações de geração de relatório de licença, busca e exclusão.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReport Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReport classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824210"
---
# <a name="win32_tslicensereport-class"></a><span data-ttu-id="67ad8-105">\_Classe Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="67ad8-105">Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="67ad8-106">Fornece instâncias de Serviços de Área de Trabalho Remota relatórios de uso de licença de acesso para cliente por usuário (RDS por CAL) que são geradas no servidor de licença Área de Trabalho Remota e métodos para operações de geração de relatório de licença, busca e exclusão.</span><span class="sxs-lookup"><span data-stu-id="67ad8-106">Provides instances of Remote Desktop Services Per User client access license (RDS Per User CAL) usage reports that are generated on the Remote Desktop license server, and methods for license report generation, fetch, and delete operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ad8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67ad8-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="67ad8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="67ad8-108">Members</span></span>

<span data-ttu-id="67ad8-109">A classe **Win32 \_ TSLicenseReport** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="67ad8-109">The **Win32\_TSLicenseReport** class has these types of members:</span></span>

-   [<span data-ttu-id="67ad8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="67ad8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="67ad8-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67ad8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="67ad8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="67ad8-112">Methods</span></span>

<span data-ttu-id="67ad8-113">A classe **Win32 \_ TSLicenseReport** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="67ad8-113">The **Win32\_TSLicenseReport** class has these methods.</span></span>



| <span data-ttu-id="67ad8-114">Método</span><span class="sxs-lookup"><span data-stu-id="67ad8-114">Method</span></span>                                                                                                         | <span data-ttu-id="67ad8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="67ad8-115">Description</span></span>                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67ad8-116">**DeleteReport**</span><span class="sxs-lookup"><span data-stu-id="67ad8-116">**DeleteReport**</span></span>](deletereport-win32-tslicensereport.md)                                                     | <span data-ttu-id="67ad8-117">Exclui um objeto de relatório no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="67ad8-117">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="67ad8-118">Esse não é um método estático.</span><span class="sxs-lookup"><span data-stu-id="67ad8-118">This is not a static method.</span></span><br/>                                                                                           |
| [<span data-ttu-id="67ad8-119">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="67ad8-119">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)                                         | <span data-ttu-id="67ad8-120">Recupera entradas no objeto de relatório.</span><span class="sxs-lookup"><span data-stu-id="67ad8-120">Retrieves entries in the report object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="67ad8-121">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="67ad8-121">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)               | <span data-ttu-id="67ad8-122">Recupera detalhes das licenças de acesso para cliente por usuário com falha Serviços de Área de Trabalho Remota (RDS CALs por usuário) do relatório.</span><span class="sxs-lookup"><span data-stu-id="67ad8-122">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                             |
| [<span data-ttu-id="67ad8-123">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="67ad8-123">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | <span data-ttu-id="67ad8-124">Recupera informações resumidas de falhas de Serviços de Área de Trabalho Remota por licenças de acesso para cliente por usuário (RDS CALs por usuário) do relatório.</span><span class="sxs-lookup"><span data-stu-id="67ad8-124">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                 |
| [<span data-ttu-id="67ad8-125">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="67ad8-125">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)                       | <span data-ttu-id="67ad8-126">Recupera informações de Serviços de Área de Trabalho Remota emitidos por licenças de acesso para cliente por dispositivo (RDS CALs por dispositivo) do relatório.</span><span class="sxs-lookup"><span data-stu-id="67ad8-126">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span><br/>                                                     |
| [<span data-ttu-id="67ad8-127">**FetchReportSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="67ad8-127">**FetchReportSummaryEntries**</span></span>](win32-tslicensereport-fetchreportsummaryentries.md)                           | <span data-ttu-id="67ad8-128">Recupera resumos de licenças do objeto de relatório.</span><span class="sxs-lookup"><span data-stu-id="67ad8-128">Retrieves license summaries from the report object.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="67ad8-129">**GenerateReport**</span><span class="sxs-lookup"><span data-stu-id="67ad8-129">**GenerateReport**</span></span>](generatereport-win32-tslicensereport.md)                                                 | <span data-ttu-id="67ad8-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="67ad8-130">This method is not supported.</span></span><br/> <span data-ttu-id="67ad8-131">**Windows server 2008 R2 e Windows server 2008:** Gera um relatório de uso de licença por usuário atual no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="67ad8-131">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="67ad8-132">**GenerateReportEx**</span><span class="sxs-lookup"><span data-stu-id="67ad8-132">**GenerateReportEx**</span></span>](generatereportex-win32-tslicensereport.md)                                             | <span data-ttu-id="67ad8-133">Gera um relatório de uso de licença por usuário atual no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="67ad8-133">Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="67ad8-134">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67ad8-134">Properties</span></span>

<span data-ttu-id="67ad8-135">A classe **Win32 \_ TSLicenseReport** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="67ad8-135">The **Win32\_TSLicenseReport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67ad8-136">**FileName**</span><span class="sxs-lookup"><span data-stu-id="67ad8-136">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ad8-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67ad8-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67ad8-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-139">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="67ad8-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="67ad8-140">O nome do relatório.</span><span class="sxs-lookup"><span data-stu-id="67ad8-140">The report name.</span></span>

</dd> <dt>

<span data-ttu-id="67ad8-141">**GenerationDateTime**</span><span class="sxs-lookup"><span data-stu-id="67ad8-141">**GenerationDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ad8-142">Tipo de dados: **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="67ad8-142">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67ad8-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ad8-144">Data e hora de geração de relatório de Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="67ad8-144">RD Licensing report generation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="67ad8-145">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="67ad8-145">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ad8-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ad8-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67ad8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-148">Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67ad8-148">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67ad8-149">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="67ad8-149">This property is not supported.</span></span>

<span data-ttu-id="67ad8-150">**Windows server 2008 R2 e Windows server 2008:** Número de CALs por usuário do RDS que estão instaladas.</span><span class="sxs-lookup"><span data-stu-id="67ad8-150">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="67ad8-151">**LicenseUsageCount**</span><span class="sxs-lookup"><span data-stu-id="67ad8-151">**LicenseUsageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ad8-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ad8-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67ad8-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-154">Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67ad8-154">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67ad8-155">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="67ad8-155">This property is not supported.</span></span>

<span data-ttu-id="67ad8-156">**Windows server 2008 R2 e Windows server 2008:** Número de CALs por usuário do RDS que estão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="67ad8-156">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are currently in use.</span></span>

</dd> <dt>

<span data-ttu-id="67ad8-157">**ScopeType**</span><span class="sxs-lookup"><span data-stu-id="67ad8-157">**ScopeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ad8-158">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ad8-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67ad8-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-160">Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67ad8-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67ad8-161">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="67ad8-161">This property is not supported.</span></span>

<span data-ttu-id="67ad8-162">**Windows server 2008 R2 e Windows server 2008:** Tipo de escopo do relatório de Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="67ad8-162">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope type.</span></span>

</dd> <dt>

<span data-ttu-id="67ad8-163">**Escopovalue**</span><span class="sxs-lookup"><span data-stu-id="67ad8-163">**ScopeValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ad8-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67ad8-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67ad8-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-166">Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67ad8-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67ad8-167">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="67ad8-167">This property is not supported.</span></span>

<span data-ttu-id="67ad8-168">**Windows server 2008 R2 e Windows server 2008:** Valor de escopo do relatório de Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="67ad8-168">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope value.</span></span>

</dd> <dt>

<span data-ttu-id="67ad8-169">**Versão**</span><span class="sxs-lookup"><span data-stu-id="67ad8-169">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ad8-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ad8-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ad8-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67ad8-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ad8-172">Versão do relatório de Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="67ad8-172">RD Licensing report version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67ad8-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="67ad8-173">Remarks</span></span>

<span data-ttu-id="67ad8-174">Os relatórios gerados usando o WMI são exibidos no Gerenciador de Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="67ad8-174">Reports that are generated by using WMI are displayed in RD Licensing Manager.</span></span> <span data-ttu-id="67ad8-175">Os relatórios excluídos usando o WMI também são excluídos do Gerenciador de Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="67ad8-175">Reports that are deleted by using WMI are also deleted from RD Licensing Manager.</span></span>

<span data-ttu-id="67ad8-176">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="67ad8-176">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="67ad8-177">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="67ad8-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="67ad8-178">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="67ad8-178">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="67ad8-179">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="67ad8-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="67ad8-180">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="67ad8-180">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="67ad8-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67ad8-181">Requirements</span></span>



| <span data-ttu-id="67ad8-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ad8-182">Requirement</span></span> | <span data-ttu-id="67ad8-183">Valor</span><span class="sxs-lookup"><span data-stu-id="67ad8-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ad8-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67ad8-184">Minimum supported client</span></span><br/> | <span data-ttu-id="67ad8-185">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="67ad8-185">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="67ad8-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67ad8-186">Minimum supported server</span></span><br/> | <span data-ttu-id="67ad8-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67ad8-187">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="67ad8-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="67ad8-188">Namespace</span></span><br/>                | <span data-ttu-id="67ad8-189">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="67ad8-189">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="67ad8-190">MOF</span><span class="sxs-lookup"><span data-stu-id="67ad8-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67ad8-191"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67ad8-191"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="67ad8-192">DLL</span><span class="sxs-lookup"><span data-stu-id="67ad8-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67ad8-193"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67ad8-193"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ad8-194">Confira também</span><span class="sxs-lookup"><span data-stu-id="67ad8-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ad8-195">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="67ad8-195">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="67ad8-196">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="67ad8-196">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="67ad8-197">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="67ad8-197">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="67ad8-198">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="67ad8-198">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

