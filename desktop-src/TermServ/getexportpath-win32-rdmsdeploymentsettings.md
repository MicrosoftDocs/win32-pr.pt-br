---
title: Método GetExportPath da classe Win32_RDMSDeploymentSettings
description: Recupera o caminho do diretório para o qual as máquinas virtuais são implantadas para uma coleção de áreas de trabalho virtuais.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetExportPath
- Método GetExportPath Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método GetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baf96d1d71554f1b8ea310759d36d0918a511cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766953"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="ee724-106">Método GetExportPath da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="ee724-106">GetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="ee724-107">Recupera o caminho do diretório para o qual as máquinas virtuais são implantadas para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="ee724-107">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee724-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee724-108">Syntax</span></span>


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="ee724-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee724-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee724-110">*DirectoryPath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee724-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee724-111">Recebe o caminho do diretório.</span><span class="sxs-lookup"><span data-stu-id="ee724-111">Receives the directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee724-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee724-112">Return value</span></span>

<span data-ttu-id="ee724-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="ee724-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee724-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee724-114">Requirements</span></span>



| <span data-ttu-id="ee724-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee724-115">Requirement</span></span> | <span data-ttu-id="ee724-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ee724-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee724-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee724-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ee724-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ee724-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ee724-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee724-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ee724-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee724-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ee724-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee724-121">Namespace</span></span><br/>                | <span data-ttu-id="ee724-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="ee724-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ee724-123">MOF</span><span class="sxs-lookup"><span data-stu-id="ee724-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee724-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee724-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee724-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ee724-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee724-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee724-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ee724-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee724-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee724-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="ee724-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





