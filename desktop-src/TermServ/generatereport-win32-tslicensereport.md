---
title: Método GenerateReport da classe Win32_TSLicenseReport (GPMgmt. h)
description: O GenerateReport não está mais disponível para uso a partir do Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GenerateReport
- Método GenerateReport Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método GenerateReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369783"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="84f7c-106">Método GenerateReport da classe Win32 \_ TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="84f7c-106">GenerateReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="84f7c-107">\[O **GenerateReport** não está mais disponível para uso a partir do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="84f7c-107">\[**GenerateReport** is no longer available for use as of Windows Server 2012.</span></span> <span data-ttu-id="84f7c-108">Em vez disso, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span><span class="sxs-lookup"><span data-stu-id="84f7c-108">Instead, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span></span>

<span data-ttu-id="84f7c-109">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="84f7c-109">This method is not supported.</span></span>

<span data-ttu-id="84f7c-110">**Windows server 2008 R2 e Windows server 2008:** Gera um relatório de uso de licença por usuário atual no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="84f7c-110">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f7c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84f7c-111">Syntax</span></span>


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="84f7c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84f7c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f7c-113">*Escopotype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84f7c-113">*ScopeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f7c-114">Escopo do relatório de uso da licença.</span><span class="sxs-lookup"><span data-stu-id="84f7c-114">Scope of the license usage report.</span></span> <span data-ttu-id="84f7c-115">Ele pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="84f7c-115">It can have the following values.</span></span>

<dt>

<span data-ttu-id="84f7c-116">1</span><span class="sxs-lookup"><span data-stu-id="84f7c-116">1</span></span>
</dt> <dd>

<span data-ttu-id="84f7c-117">O relatório será gerado para todo o domínio.</span><span class="sxs-lookup"><span data-stu-id="84f7c-117">The report will be generated for the entire domain.</span></span>

</dd> <dt>

<span data-ttu-id="84f7c-118">2</span><span class="sxs-lookup"><span data-stu-id="84f7c-118">2</span></span>
</dt> <dd>

<span data-ttu-id="84f7c-119">O relatório será gerado para a unidade organizacional (UO) especificada no parâmetro *scopevalue* .</span><span class="sxs-lookup"><span data-stu-id="84f7c-119">The report will be generated for the organizational unit (OU) that is specified in the *ScopeValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="84f7c-120">3</span><span class="sxs-lookup"><span data-stu-id="84f7c-120">3</span></span>
</dt> <dd>

<span data-ttu-id="84f7c-121">O relatório será gerado para todos os domínios confiáveis.</span><span class="sxs-lookup"><span data-stu-id="84f7c-121">The report will be generated for all trusted domains.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="84f7c-122">*Escopovalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84f7c-122">*ScopeValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f7c-123">Se o parâmetro *ScopeType* é 2, *ScopeType* especifica a UO para a qual o relatório será gerado.</span><span class="sxs-lookup"><span data-stu-id="84f7c-123">If the *ScopeType* parameter is 2, *ScopeType* specifies the OU for which the report will be generated.</span></span> <span data-ttu-id="84f7c-124">Você deve especificar *scopevalue* usando o formato **ou =**_OUName1_*_, ou =_*_OUName2_*_..._*.</span><span class="sxs-lookup"><span data-stu-id="84f7c-124">You must specify *ScopeValue* by using the format **OU=**_OUName1_*_,OU=_*_OUName2_*_..._*.</span></span>

</dd> <dt>

<span data-ttu-id="84f7c-125">*Nome do arquivo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="84f7c-125">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84f7c-126">O nome do arquivo do relatório gerado.</span><span class="sxs-lookup"><span data-stu-id="84f7c-126">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f7c-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84f7c-127">Return value</span></span>

<span data-ttu-id="84f7c-128">Retorna o **WBEM \_ E \_ não \_ tem suporte**.</span><span class="sxs-lookup"><span data-stu-id="84f7c-128">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="84f7c-129">**Windows server 2008 R2 e Windows server 2008:** Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="84f7c-129">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="84f7c-130">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="84f7c-130">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="84f7c-131">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="84f7c-131">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="84f7c-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="84f7c-132">Remarks</span></span>

<span data-ttu-id="84f7c-133">Esse é um método estático.</span><span class="sxs-lookup"><span data-stu-id="84f7c-133">This is a static method.</span></span>

<span data-ttu-id="84f7c-134">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="84f7c-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="84f7c-135">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="84f7c-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="84f7c-136">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="84f7c-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="84f7c-137">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="84f7c-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="84f7c-138">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="84f7c-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="84f7c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84f7c-139">Requirements</span></span>



| <span data-ttu-id="84f7c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f7c-140">Requirement</span></span> | <span data-ttu-id="84f7c-141">Valor</span><span class="sxs-lookup"><span data-stu-id="84f7c-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f7c-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84f7c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="84f7c-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="84f7c-143">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="84f7c-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84f7c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="84f7c-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84f7c-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="84f7c-146">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="84f7c-146">End of client support</span></span><br/>    | <span data-ttu-id="84f7c-147">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="84f7c-147">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="84f7c-148">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="84f7c-148">End of server support</span></span><br/>    | <span data-ttu-id="84f7c-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84f7c-149">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="84f7c-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="84f7c-150">Namespace</span></span><br/>                | <span data-ttu-id="84f7c-151">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="84f7c-151">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="84f7c-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84f7c-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f7c-153"><dt>GPMgmt. h</dt></span><span class="sxs-lookup"><span data-stu-id="84f7c-153"><dt>Gpmgmt.h</dt></span></span> </dl>       |
| <span data-ttu-id="84f7c-154">MOF</span><span class="sxs-lookup"><span data-stu-id="84f7c-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84f7c-155"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84f7c-155"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="84f7c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="84f7c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f7c-157"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84f7c-157"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f7c-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="84f7c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f7c-159">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="84f7c-159">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

