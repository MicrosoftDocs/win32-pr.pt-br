---
title: Método SetBaseVHDPath da classe Win32_RDMSDeploymentSettings
description: Recupera o caminho base para o diretório no qual os VHDs do conjunto de áreas de trabalho virtuais são implantados. | Método SetBaseVHDPath da classe Win32_RDMSDeploymentSettings
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetBaseVHDPath
- Método SetBaseVHDPath Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método SetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7907640a9641cff3c94475318bf499415b25184
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105766942"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="06071-107">Método SetBaseVHDPath da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="06071-107">SetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="06071-108">Recupera o caminho base para o diretório no qual os VHDs do conjunto de áreas de trabalho virtuais são implantados.</span><span class="sxs-lookup"><span data-stu-id="06071-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="06071-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06071-109">Syntax</span></span>


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="06071-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06071-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06071-111">*DirectoryPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06071-111">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06071-112">O novo caminho de implantação do VHD.</span><span class="sxs-lookup"><span data-stu-id="06071-112">The new VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06071-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06071-113">Return value</span></span>

<span data-ttu-id="06071-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="06071-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="06071-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06071-115">Requirements</span></span>



| <span data-ttu-id="06071-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06071-116">Requirement</span></span> | <span data-ttu-id="06071-117">Valor</span><span class="sxs-lookup"><span data-stu-id="06071-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="06071-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06071-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06071-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="06071-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="06071-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06071-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06071-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06071-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="06071-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="06071-122">Namespace</span></span><br/>                | <span data-ttu-id="06071-123">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="06071-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="06071-124">MOF</span><span class="sxs-lookup"><span data-stu-id="06071-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06071-125"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06071-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="06071-126">DLL</span><span class="sxs-lookup"><span data-stu-id="06071-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06071-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06071-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="06071-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="06071-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06071-129">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="06071-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





