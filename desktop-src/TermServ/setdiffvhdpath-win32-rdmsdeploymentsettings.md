---
title: Método SetDiffVHDPath da classe Win32_RDMSDeploymentSettings
description: Atualiza o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.
ms.assetid: 665ffbf9-0250-4956-9bce-f5a6714b47e4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetDiffVHDPath
- Método SetDiffVHDPath Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método SetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e52d206c9e0cbff19f26e38a2a02f04ea0acc03d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369567"
---
# <a name="setdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="4cff8-106">Método SetDiffVHDPath da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="4cff8-106">SetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="4cff8-107">Atualiza o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="4cff8-107">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cff8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cff8-108">Syntax</span></span>


```mof
uint32 SetDiffVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="4cff8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cff8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cff8-110">*DirectoryPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cff8-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cff8-111">O novo caminho de disco diferencial.</span><span class="sxs-lookup"><span data-stu-id="4cff8-111">The new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cff8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4cff8-112">Return value</span></span>

<span data-ttu-id="4cff8-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="4cff8-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cff8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cff8-114">Requirements</span></span>



| <span data-ttu-id="4cff8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cff8-115">Requirement</span></span> | <span data-ttu-id="4cff8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4cff8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cff8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cff8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4cff8-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4cff8-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4cff8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cff8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4cff8-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4cff8-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="4cff8-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="4cff8-121">Namespace</span></span><br/>                | <span data-ttu-id="4cff8-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="4cff8-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4cff8-123">MOF</span><span class="sxs-lookup"><span data-stu-id="4cff8-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cff8-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4cff8-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4cff8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4cff8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cff8-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cff8-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4cff8-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4cff8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cff8-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="4cff8-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





