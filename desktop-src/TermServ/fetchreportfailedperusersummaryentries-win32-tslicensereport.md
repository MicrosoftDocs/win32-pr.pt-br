---
title: Método FetchReportFailedPerUserSummaryEntries da classe Win32_TSLicenseReport
description: Recupera informações de Resumo de falhas de Serviços de Área de Trabalho Remota por licenças de acesso para cliente por usuário (RDS \ 160; CALs por usuário) do relatório.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método FetchReportFailedPerUserSummaryEntries
- Método FetchReportFailedPerUserSummaryEntries Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método FetchReportFailedPerUserSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759947"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="85c41-106">Método FetchReportFailedPerUserSummaryEntries da classe Win32 \_ TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="85c41-106">FetchReportFailedPerUserSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="85c41-107">Recupera informações resumidas de falhas de Serviços de Área de Trabalho Remota por licenças de acesso para cliente por usuário (RDS CALs por usuário) do relatório.</span><span class="sxs-lookup"><span data-stu-id="85c41-107">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c41-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85c41-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="85c41-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85c41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85c41-110">*StartIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85c41-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85c41-111">O índice da primeira entrada de relatório a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="85c41-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="85c41-112">A primeira entrada de relatório tem um índice de zero.</span><span class="sxs-lookup"><span data-stu-id="85c41-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="85c41-113">*Contagem* \[ de entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="85c41-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85c41-114">O número de entradas de relatório a serem recuperadas do objeto de relatório.</span><span class="sxs-lookup"><span data-stu-id="85c41-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="85c41-115">Um valor de zero indica que todas as entradas de relatório começando em *startIndex* devem ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="85c41-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="85c41-116">No retorno, contém o número de entradas na matriz *ReportFailedPerUserSummaryEntries* .</span><span class="sxs-lookup"><span data-stu-id="85c41-116">On return, contains the number of entries in the *ReportFailedPerUserSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="85c41-117">*ReportFailedPerUserSummaryEntries* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85c41-117">*ReportFailedPerUserSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85c41-118">Uma matriz de [**classes \_ TSLicenseReportFailedPerUserSummaryEntry do Win32**](win32-tslicensereportfailedperusersummaryentry.md) que representam as entradas de licença recuperadas.</span><span class="sxs-lookup"><span data-stu-id="85c41-118">An array of [**Win32\_TSLicenseReportFailedPerUserSummaryEntry**](win32-tslicensereportfailedperusersummaryentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="85c41-119">O parâmetro *Count* contém o número de elementos nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="85c41-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85c41-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85c41-120">Return value</span></span>

<span data-ttu-id="85c41-121">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="85c41-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="85c41-122">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="85c41-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="85c41-123">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="85c41-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85c41-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85c41-124">Requirements</span></span>



| <span data-ttu-id="85c41-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c41-125">Requirement</span></span> | <span data-ttu-id="85c41-126">Valor</span><span class="sxs-lookup"><span data-stu-id="85c41-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c41-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85c41-127">Minimum supported client</span></span><br/> | <span data-ttu-id="85c41-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="85c41-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="85c41-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85c41-129">Minimum supported server</span></span><br/> | <span data-ttu-id="85c41-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85c41-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="85c41-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="85c41-131">Namespace</span></span><br/>                | <span data-ttu-id="85c41-132">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="85c41-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="85c41-133">MOF</span><span class="sxs-lookup"><span data-stu-id="85c41-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85c41-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85c41-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="85c41-135">DLL</span><span class="sxs-lookup"><span data-stu-id="85c41-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85c41-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85c41-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c41-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="85c41-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c41-138">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="85c41-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





