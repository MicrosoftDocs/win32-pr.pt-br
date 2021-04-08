---
title: Método SetSMBPath da classe Win32_RDMSDeploymentSettings
description: Atualiza o caminho UNC para o compartilhamento SMB no qual as máquinas virtuais do conjunto de áreas de trabalho virtuais são implantadas.
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSMBPath
- Método SetSMBPath Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método SetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40598a3217ff1ca7c6082b3af09097352962309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918729"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="91987-106">Método SetSMBPath da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="91987-106">SetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="91987-107">Atualiza o caminho UNC para o compartilhamento SMB no qual as máquinas virtuais do conjunto de áreas de trabalho virtuais são implantadas.</span><span class="sxs-lookup"><span data-stu-id="91987-107">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="91987-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91987-108">Syntax</span></span>


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="91987-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91987-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91987-110">*DirectoryPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91987-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91987-111">O novo caminho para o compartilhamento SMB, no formato UNC.</span><span class="sxs-lookup"><span data-stu-id="91987-111">The new path to the SMB share, in UNC format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91987-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91987-112">Return value</span></span>

<span data-ttu-id="91987-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="91987-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="91987-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91987-114">Requirements</span></span>



| <span data-ttu-id="91987-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="91987-115">Requirement</span></span> | <span data-ttu-id="91987-116">Valor</span><span class="sxs-lookup"><span data-stu-id="91987-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="91987-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91987-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91987-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="91987-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="91987-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91987-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91987-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91987-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="91987-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="91987-121">Namespace</span></span><br/>                | <span data-ttu-id="91987-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="91987-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="91987-123">MOF</span><span class="sxs-lookup"><span data-stu-id="91987-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91987-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91987-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="91987-125">DLL</span><span class="sxs-lookup"><span data-stu-id="91987-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91987-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91987-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="91987-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="91987-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91987-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="91987-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





