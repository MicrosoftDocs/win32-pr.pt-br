---
title: Método ProvisioningEnumerateJobs da classe Win32_RDMSVirtualDesktopCollection
description: Enumera os trabalhos de provisionamento de área de trabalho virtual para este serviço.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ProvisioningEnumerateJobs
- Método ProvisioningEnumerateJobs Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método ProvisioningEnumerateJobs
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499781"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="2b5f6-106">Método ProvisioningEnumerateJobs da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="2b5f6-106">ProvisioningEnumerateJobs method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="2b5f6-107">Enumera os trabalhos de provisionamento de área de trabalho virtual para este serviço.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-107">Enumerates virtual desktop provisioning jobs for this service.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b5f6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b5f6-108">Syntax</span></span>


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a><span data-ttu-id="2b5f6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b5f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b5f6-110">*JobType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b5f6-110">*JobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5f6-111">Um inteiro que especifica o tipo de trabalho a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-111">An integer that specifies the type of job to enumerate.</span></span>

<span data-ttu-id="2b5f6-112">Esse parâmetro pode ser definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="2b5f6-112">This parameter can be set to one of the following values:</span></span>

<dt>

<span data-ttu-id="2b5f6-113">0</span><span class="sxs-lookup"><span data-stu-id="2b5f6-113">0</span></span>
</dt> <dd>

<span data-ttu-id="2b5f6-114">Executando trabalhos</span><span class="sxs-lookup"><span data-stu-id="2b5f6-114">Running jobs</span></span>

</dd> <dt>

<span data-ttu-id="2b5f6-115">1</span><span class="sxs-lookup"><span data-stu-id="2b5f6-115">1</span></span>
</dt> <dd>

<span data-ttu-id="2b5f6-116">Trabalhos concluídos</span><span class="sxs-lookup"><span data-stu-id="2b5f6-116">Completed jobs</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2b5f6-117">*CollectionAlias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b5f6-117">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5f6-118">O alias da coleção de áreas de trabalho virtuais a ser enumerada.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-118">The alias of the virtual desktop collection to enumerate.</span></span> <span data-ttu-id="2b5f6-119">O valor padrão para esse parâmetro é FALSE, que especifica que todos os trabalhos em execução devem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-119">The default value for this parameter is FALSE, which specifies that all running jobs are to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="2b5f6-120">*JobGuids* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b5f6-120">*JobGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5f6-121">Uma matriz que contém os **GUIDs** de trabalhos de provisionamento a serem enumerados.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-121">An array that contains the **GUIDs** of provisioning jobs to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b5f6-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b5f6-122">Return value</span></span>

<span data-ttu-id="2b5f6-123">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b5f6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b5f6-124">Requirements</span></span>



| <span data-ttu-id="2b5f6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b5f6-125">Requirement</span></span> | <span data-ttu-id="2b5f6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2b5f6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b5f6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b5f6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2b5f6-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2b5f6-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2b5f6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b5f6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2b5f6-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b5f6-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2b5f6-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b5f6-131">Namespace</span></span><br/>                | <span data-ttu-id="2b5f6-132">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="2b5f6-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2b5f6-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2b5f6-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b5f6-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b5f6-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b5f6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2b5f6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b5f6-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b5f6-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2b5f6-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b5f6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b5f6-138">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="2b5f6-138">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





