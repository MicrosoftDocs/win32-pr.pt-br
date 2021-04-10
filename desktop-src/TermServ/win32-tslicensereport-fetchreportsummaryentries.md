---
title: Método FetchReportSummaryEntries da classe Win32_TSLicenseReport
description: Recupera resumos de Serviços de Área de Trabalho Remota licenças de acesso para cliente por usuário (RDS \ 160; CALs por usuário) do relatório.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método FetchReportSummaryEntries
- Método FetchReportSummaryEntries Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método FetchReportSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085228"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="ad01a-106">Método FetchReportSummaryEntries da classe Win32 \_ TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="ad01a-106">FetchReportSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="ad01a-107">Recupera resumos de Serviços de Área de Trabalho Remota licenças de acesso para cliente por usuário (RDS CALs por usuário) do relatório.</span><span class="sxs-lookup"><span data-stu-id="ad01a-107">Retrieves summaries of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad01a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad01a-108">Syntax</span></span>


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="ad01a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad01a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad01a-110">*StartIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad01a-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad01a-111">Índice da primeira entrada de relatório a ser recebida.</span><span class="sxs-lookup"><span data-stu-id="ad01a-111">Index of the first report entry to be received.</span></span> <span data-ttu-id="ad01a-112">A primeira entrada de relatório tem um índice de zero.</span><span class="sxs-lookup"><span data-stu-id="ad01a-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="ad01a-113">*Contagem* \[ de entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ad01a-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad01a-114">Número de entradas de relatório a serem recuperadas do objeto de relatório.</span><span class="sxs-lookup"><span data-stu-id="ad01a-114">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="ad01a-115">Um valor de zero indica que todas as entradas de relatório começando em *startIndex* devem ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="ad01a-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="ad01a-116">No retorno, contém o número de entradas na matriz *ReportSummaryEntries* .</span><span class="sxs-lookup"><span data-stu-id="ad01a-116">On return, contains the number of entries in the *ReportSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="ad01a-117">*ReportSummaryEntries* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ad01a-117">*ReportSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad01a-118">Retorna uma matriz de [**classes \_ TSLicenseReportSummaryEntry do Win32**](win32-tslicensereportsummaryentry.md) .</span><span class="sxs-lookup"><span data-stu-id="ad01a-118">Returns an array of [**Win32\_TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad01a-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad01a-119">Return value</span></span>

<span data-ttu-id="ad01a-120">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ad01a-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ad01a-121">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ad01a-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ad01a-122">Um valor de **LSERVER \_ que \_ não \_ mais \_ dados** (0x4001) indica que não há mais entradas de relatório.</span><span class="sxs-lookup"><span data-stu-id="ad01a-122">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad01a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad01a-123">Remarks</span></span>

<span data-ttu-id="ad01a-124">Esse não é um método estático.</span><span class="sxs-lookup"><span data-stu-id="ad01a-124">This is not a static method.</span></span> <span data-ttu-id="ad01a-125">Esse método deve ser chamado de um objeto de relatório de uso de licença por usuário.</span><span class="sxs-lookup"><span data-stu-id="ad01a-125">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="ad01a-126">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="ad01a-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ad01a-127">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ad01a-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ad01a-128">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ad01a-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ad01a-129">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ad01a-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ad01a-130">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ad01a-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad01a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad01a-131">Requirements</span></span>



| <span data-ttu-id="ad01a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad01a-132">Requirement</span></span> | <span data-ttu-id="ad01a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ad01a-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad01a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad01a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ad01a-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ad01a-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ad01a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad01a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ad01a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad01a-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ad01a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad01a-138">Namespace</span></span><br/>                | <span data-ttu-id="ad01a-139">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ad01a-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ad01a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ad01a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad01a-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad01a-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad01a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ad01a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad01a-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad01a-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad01a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad01a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad01a-145">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="ad01a-145">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="ad01a-146">**\_TSLicenseReportSummaryEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="ad01a-146">**Win32\_TSLicenseReportSummaryEntry**</span></span>](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

