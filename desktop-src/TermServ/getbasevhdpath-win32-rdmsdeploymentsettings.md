---
title: Método GetBaseVHDPath da classe Win32_RDMSDeploymentSettings
description: Recupera o caminho base para o diretório no qual os VHDs do conjunto de áreas de trabalho virtuais são implantados. | Método GetBaseVHDPath da classe Win32_RDMSDeploymentSettings
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetBaseVHDPath
- Método GetBaseVHDPath Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método GetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595c6459148a0270bed2328c70e15ef74a69acf3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930393"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="9f74b-107">Método GetBaseVHDPath da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="9f74b-107">GetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="9f74b-108">Recupera o caminho base para o diretório no qual os VHDs do conjunto de áreas de trabalho virtuais são implantados.</span><span class="sxs-lookup"><span data-stu-id="9f74b-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f74b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f74b-109">Syntax</span></span>


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="9f74b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f74b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f74b-111">*DirectoryPath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9f74b-111">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f74b-112">Recebe o caminho de implantação do VHD.</span><span class="sxs-lookup"><span data-stu-id="9f74b-112">Receives the VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f74b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f74b-113">Return value</span></span>

<span data-ttu-id="9f74b-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="9f74b-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f74b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f74b-115">Requirements</span></span>



| <span data-ttu-id="9f74b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f74b-116">Requirement</span></span> | <span data-ttu-id="9f74b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9f74b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f74b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f74b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9f74b-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9f74b-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9f74b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f74b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9f74b-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f74b-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9f74b-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f74b-122">Namespace</span></span><br/>                | <span data-ttu-id="9f74b-123">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="9f74b-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9f74b-124">MOF</span><span class="sxs-lookup"><span data-stu-id="9f74b-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f74b-125"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f74b-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f74b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9f74b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f74b-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f74b-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9f74b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f74b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f74b-129">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="9f74b-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





