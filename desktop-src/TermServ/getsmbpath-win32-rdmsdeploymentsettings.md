---
title: Método GetSMBPath da classe Win32_RDMSDeploymentSettings
description: Recupera o caminho UNC para o compartilhamento SMB no qual as máquinas virtuais do conjunto de áreas de trabalho virtuais são implantadas.
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetSMBPath
- Método GetSMBPath Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método GetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369932"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="ab9a3-106">Método GetSMBPath da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="ab9a3-106">GetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="ab9a3-107">Recupera o caminho UNC para o compartilhamento SMB no qual as máquinas virtuais do conjunto de áreas de trabalho virtuais são implantadas.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-107">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab9a3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab9a3-108">Syntax</span></span>


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="ab9a3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab9a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab9a3-110">*DirectoryPath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ab9a3-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9a3-111">Recebe um caminho formatado UNC para o compartilhamento SMB.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-111">Receives a UNC formatted path to the SMB share.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab9a3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab9a3-112">Return value</span></span>

<span data-ttu-id="ab9a3-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="ab9a3-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab9a3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab9a3-114">Requirements</span></span>



| <span data-ttu-id="ab9a3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab9a3-115">Requirement</span></span> | <span data-ttu-id="ab9a3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ab9a3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9a3-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab9a3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ab9a3-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ab9a3-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ab9a3-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab9a3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ab9a3-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab9a3-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ab9a3-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab9a3-121">Namespace</span></span><br/>                | <span data-ttu-id="ab9a3-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="ab9a3-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ab9a3-123">MOF</span><span class="sxs-lookup"><span data-stu-id="ab9a3-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab9a3-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab9a3-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab9a3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ab9a3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab9a3-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab9a3-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ab9a3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab9a3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab9a3-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="ab9a3-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





