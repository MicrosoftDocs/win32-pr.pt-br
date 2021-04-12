---
title: Método ProvisioningJobExecute da classe Win32_RDMSVirtualDesktopCollection
description: Executa um trabalho de provisionamento de área de trabalho virtual.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ProvisioningJobExecute
- Método ProvisioningJobExecute Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método ProvisioningJobExecute
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455864"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="5865c-106">Método ProvisioningJobExecute da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="5865c-106">ProvisioningJobExecute method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="5865c-107">Executa um trabalho de provisionamento de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="5865c-107">Runs a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="5865c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5865c-108">Syntax</span></span>


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="5865c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5865c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5865c-110">*JobInputXml* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5865c-110">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5865c-111">Uma cadeia de caracteres que contém as informações de provisionamento em formato XML.</span><span class="sxs-lookup"><span data-stu-id="5865c-111">A string that contains the provisioning information in XML format.</span></span>

</dd> <dt>

<span data-ttu-id="5865c-112">*JobGuid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5865c-112">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5865c-113">O **GUID** que identifica exclusivamente o trabalho de provisionamento a ser executado.</span><span class="sxs-lookup"><span data-stu-id="5865c-113">The **GUID** that uniquely identifies the provisioning job to run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5865c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5865c-114">Return value</span></span>

<span data-ttu-id="5865c-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="5865c-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5865c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5865c-116">Requirements</span></span>



| <span data-ttu-id="5865c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5865c-117">Requirement</span></span> | <span data-ttu-id="5865c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5865c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5865c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5865c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5865c-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5865c-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5865c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5865c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5865c-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5865c-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5865c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="5865c-123">Namespace</span></span><br/>                | <span data-ttu-id="5865c-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="5865c-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5865c-125">MOF</span><span class="sxs-lookup"><span data-stu-id="5865c-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5865c-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5865c-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5865c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5865c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5865c-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5865c-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5865c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5865c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5865c-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="5865c-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





