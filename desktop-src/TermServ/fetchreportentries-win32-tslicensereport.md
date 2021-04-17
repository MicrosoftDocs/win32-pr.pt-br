---
title: Método FetchReportEntries da classe Win32_TSLicenseReport
description: Recupera detalhes de Serviços de Área de Trabalho Remota licenças de acesso para cliente por usuário (RDS \ 160; CALs por usuário) do relatório. Cada entrada representa um RDS \ 160; CAL por usuário que está em uso no momento.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método FetchReportEntries
- Método FetchReportEntries Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método FetchReportEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc64c9591444307ba0519da02cf9c6f13d20252e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499731"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="a246d-107">Método FetchReportEntries da classe Win32 \_ TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="a246d-107">FetchReportEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="a246d-108">Recupera detalhes de Serviços de Área de Trabalho Remota licenças de acesso para cliente por usuário (RDS CALs por usuário) do relatório.</span><span class="sxs-lookup"><span data-stu-id="a246d-108">Retrieves details of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span> <span data-ttu-id="a246d-109">Cada entrada representa uma CAL RDS por usuário que está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="a246d-109">Each entry represents a RDS Per User CAL that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="a246d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a246d-110">Syntax</span></span>


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="a246d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a246d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a246d-112">*StartIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a246d-112">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a246d-113">Índice da primeira entrada de relatório a ser recebida.</span><span class="sxs-lookup"><span data-stu-id="a246d-113">Index of the first report entry to be received.</span></span> <span data-ttu-id="a246d-114">A primeira entrada de relatório tem um índice de zero.</span><span class="sxs-lookup"><span data-stu-id="a246d-114">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="a246d-115">*Contagem* \[ de entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a246d-115">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a246d-116">Número de entradas de relatório a serem recuperadas do objeto de relatório.</span><span class="sxs-lookup"><span data-stu-id="a246d-116">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="a246d-117">Um valor de zero indica que todas as entradas de relatório começando em *startIndex* devem ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="a246d-117">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="a246d-118">No retorno, contém o número de entradas na matriz *ReportEntries* .</span><span class="sxs-lookup"><span data-stu-id="a246d-118">On return, contains the number of entries in the *ReportEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="a246d-119">*ReportEntries* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a246d-119">*ReportEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a246d-120">Retorna uma matriz de [**classes \_ TSLicenseReportEntry do Win32**](win32-tslicensereportentry.md) .</span><span class="sxs-lookup"><span data-stu-id="a246d-120">Returns an array of [**Win32\_TSLicenseReportEntry**](win32-tslicensereportentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a246d-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a246d-121">Return value</span></span>

<span data-ttu-id="a246d-122">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a246d-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a246d-123">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a246d-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a246d-124">Um valor de **LSERVER \_ que \_ não \_ mais \_ dados** (0x4001) indica que não há mais entradas de relatório.</span><span class="sxs-lookup"><span data-stu-id="a246d-124">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="a246d-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a246d-125">Remarks</span></span>

<span data-ttu-id="a246d-126">Esse não é um método estático.</span><span class="sxs-lookup"><span data-stu-id="a246d-126">This is not a static method.</span></span> <span data-ttu-id="a246d-127">Esse método deve ser chamado de um objeto de relatório de uso de licença por usuário.</span><span class="sxs-lookup"><span data-stu-id="a246d-127">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="a246d-128">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="a246d-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a246d-129">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a246d-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a246d-130">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a246d-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a246d-131">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a246d-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a246d-132">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a246d-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a246d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a246d-133">Requirements</span></span>



| <span data-ttu-id="a246d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a246d-134">Requirement</span></span> | <span data-ttu-id="a246d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a246d-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a246d-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a246d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a246d-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a246d-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a246d-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a246d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a246d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a246d-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a246d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="a246d-140">Namespace</span></span><br/>                | <span data-ttu-id="a246d-141">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a246d-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a246d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a246d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a246d-143"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a246d-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a246d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a246d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a246d-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a246d-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a246d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="a246d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a246d-147">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="a246d-147">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="a246d-148">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="a246d-148">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

