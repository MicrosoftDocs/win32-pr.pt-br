---
title: Método SetExportPath da classe Win32_RDMSDeploymentSettings
description: Atualiza o caminho do diretório para o qual as máquinas virtuais são implantadas para uma coleção de áreas de trabalho virtuais.
ms.assetid: e52b79c8-6724-4264-93d5-4a2a14c89b6b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetExportPath
- Método SetExportPath Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método SetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32dbc844aecf86d4c62fada6c5cd68d514a69272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759024"
---
# <a name="setexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="5b19a-106">Método SetExportPath da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="5b19a-106">SetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="5b19a-107">Atualiza o caminho do diretório para o qual as máquinas virtuais são implantadas para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="5b19a-107">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b19a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b19a-108">Syntax</span></span>


```mof
uint32 SetExportPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="5b19a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b19a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b19a-110">*DirectoryPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5b19a-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b19a-111">O novo caminho de diretório.</span><span class="sxs-lookup"><span data-stu-id="5b19a-111">The new directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b19a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b19a-112">Return value</span></span>

<span data-ttu-id="5b19a-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="5b19a-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b19a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b19a-114">Requirements</span></span>



| <span data-ttu-id="5b19a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b19a-115">Requirement</span></span> | <span data-ttu-id="5b19a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5b19a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b19a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b19a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5b19a-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5b19a-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5b19a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b19a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5b19a-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b19a-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5b19a-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b19a-121">Namespace</span></span><br/>                | <span data-ttu-id="5b19a-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="5b19a-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5b19a-123">MOF</span><span class="sxs-lookup"><span data-stu-id="5b19a-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b19a-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b19a-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b19a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5b19a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b19a-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b19a-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5b19a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b19a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b19a-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="5b19a-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





