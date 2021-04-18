---
title: Método ProvisioningJobGetReport da classe Win32_RDMSVirtualDesktopCollection
description: Obtém um relatório sobre o status de um trabalho de provisionamento de área de trabalho virtual.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ProvisioningJobGetReport
- Método ProvisioningJobGetReport Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método ProvisioningJobGetReport
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764736"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="2d02b-106">Método ProvisioningJobGetReport da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="2d02b-106">ProvisioningJobGetReport method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="2d02b-107">Obtém um relatório sobre o status de um trabalho de provisionamento de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="2d02b-107">Gets a report about the status of a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d02b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d02b-108">Syntax</span></span>


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a><span data-ttu-id="2d02b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d02b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d02b-110">*JobGuid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d02b-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d02b-111">O **GUID** que identifica exclusivamente o trabalho de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="2d02b-111">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="2d02b-112">*JobReportXml* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2d02b-112">*JobReportXml* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d02b-113">Uma cadeia de caracteres que contém o relatório em formato XML.</span><span class="sxs-lookup"><span data-stu-id="2d02b-113">A string that contains the report in XML format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d02b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d02b-114">Return value</span></span>

<span data-ttu-id="2d02b-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="2d02b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d02b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d02b-116">Requirements</span></span>



| <span data-ttu-id="2d02b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d02b-117">Requirement</span></span> | <span data-ttu-id="2d02b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2d02b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d02b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d02b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d02b-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2d02b-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2d02b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d02b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d02b-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d02b-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2d02b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d02b-123">Namespace</span></span><br/>                | <span data-ttu-id="2d02b-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="2d02b-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2d02b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2d02b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d02b-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d02b-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d02b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2d02b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d02b-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d02b-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2d02b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d02b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d02b-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="2d02b-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





