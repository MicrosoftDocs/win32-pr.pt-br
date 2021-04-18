---
title: Método FetchReportPerDeviceEntries da classe Win32_TSLicenseReport
description: Recupera informações de Serviços de Área de Trabalho Remota emitidos por licenças de acesso para cliente por dispositivo (RDS \ 160; CALs por dispositivo) do relatório.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método FetchReportPerDeviceEntries
- Método FetchReportPerDeviceEntries Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método FetchReportPerDeviceEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce77fce941dd0a24fb6ee17e0aeb67b4e78bdae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755164"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="e7054-106">Método FetchReportPerDeviceEntries da classe Win32 \_ TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="e7054-106">FetchReportPerDeviceEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="e7054-107">Recupera informações de Serviços de Área de Trabalho Remota emitidos por licenças de acesso para cliente por dispositivo (RDS CALs por dispositivo) do relatório.</span><span class="sxs-lookup"><span data-stu-id="e7054-107">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7054-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7054-108">Syntax</span></span>


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="e7054-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7054-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7054-110">*StartIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7054-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7054-111">O índice da primeira entrada de relatório a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="e7054-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="e7054-112">A primeira entrada de relatório tem um índice de zero.</span><span class="sxs-lookup"><span data-stu-id="e7054-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="e7054-113">*Contagem* \[ de entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e7054-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7054-114">O número de entradas de relatório a serem recuperadas do objeto de relatório.</span><span class="sxs-lookup"><span data-stu-id="e7054-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="e7054-115">Um valor de zero indica que todas as entradas de relatório começando em *startIndex* devem ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e7054-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="e7054-116">No retorno, contém o número de entradas na matriz *ReportPerDeviceEntries* .</span><span class="sxs-lookup"><span data-stu-id="e7054-116">On return, contains the number of entries in the *ReportPerDeviceEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="e7054-117">*ReportPerDeviceEntries* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e7054-117">*ReportPerDeviceEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7054-118">Uma matriz de [**classes \_ TSLicenseReportPerDeviceEntry do Win32**](win32-tslicensereportperdeviceentry.md) representa as entradas de licença recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e7054-118">An array of [**Win32\_TSLicenseReportPerDeviceEntry**](win32-tslicensereportperdeviceentry.md) classes the represent the license entries retrieved.</span></span> <span data-ttu-id="e7054-119">O parâmetro *Count* contém o número de elementos nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="e7054-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7054-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7054-120">Return value</span></span>

<span data-ttu-id="e7054-121">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e7054-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e7054-122">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e7054-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e7054-123">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e7054-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7054-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7054-124">Requirements</span></span>



| <span data-ttu-id="e7054-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7054-125">Requirement</span></span> | <span data-ttu-id="e7054-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e7054-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7054-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7054-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e7054-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e7054-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e7054-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7054-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e7054-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7054-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="e7054-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7054-131">Namespace</span></span><br/>                | <span data-ttu-id="e7054-132">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e7054-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e7054-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e7054-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7054-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7054-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7054-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e7054-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7054-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7054-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7054-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7054-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7054-138">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="e7054-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





