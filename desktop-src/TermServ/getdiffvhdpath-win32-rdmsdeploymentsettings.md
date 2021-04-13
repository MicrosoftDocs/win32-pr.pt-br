---
title: Método GetDiffVHDPath da classe Win32_RDMSDeploymentSettings
description: Recupera o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetDiffVHDPath
- Método GetDiffVHDPath Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método GetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369314"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="5ef85-106">Método GetDiffVHDPath da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="5ef85-106">GetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="5ef85-107">Recupera o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="5ef85-107">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef85-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ef85-108">Syntax</span></span>


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="5ef85-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ef85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ef85-110">*DirectoryPath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5ef85-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ef85-111">Recebe o novo caminho de disco diferencial.</span><span class="sxs-lookup"><span data-stu-id="5ef85-111">Receives the new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ef85-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ef85-112">Return value</span></span>

<span data-ttu-id="5ef85-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="5ef85-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef85-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ef85-114">Requirements</span></span>



| <span data-ttu-id="5ef85-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ef85-115">Requirement</span></span> | <span data-ttu-id="5ef85-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5ef85-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef85-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ef85-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef85-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5ef85-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5ef85-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ef85-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef85-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ef85-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5ef85-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ef85-121">Namespace</span></span><br/>                | <span data-ttu-id="5ef85-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="5ef85-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5ef85-123">MOF</span><span class="sxs-lookup"><span data-stu-id="5ef85-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ef85-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ef85-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ef85-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5ef85-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ef85-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ef85-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5ef85-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ef85-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef85-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="5ef85-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





