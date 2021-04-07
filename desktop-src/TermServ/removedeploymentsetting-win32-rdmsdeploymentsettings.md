---
title: Método RemoveDeploymentSetting da classe Win32_RDMSDeploymentSettings
description: Exclui as configurações de implantação para uma coleção de áreas de trabalho virtuais.
ms.assetid: 68e102a3-8f3f-4997-bdf0-c2ae3640ed42
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveDeploymentSetting
- Método RemoveDeploymentSetting Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método RemoveDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.RemoveDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336b93f86d6b96074341dde4851813b26eb66fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824775"
---
# <a name="removedeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="0fff1-106">Método RemoveDeploymentSetting da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="0fff1-106">RemoveDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="0fff1-107">Exclui as configurações de implantação para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="0fff1-107">Deletes the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fff1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fff1-108">Syntax</span></span>


```mof
uint32 RemoveDeploymentSetting(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="0fff1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fff1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fff1-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0fff1-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fff1-111">O alias da coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="0fff1-111">The alias of the virtual desktop collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fff1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fff1-112">Requirements</span></span>



| <span data-ttu-id="0fff1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fff1-113">Requirement</span></span> | <span data-ttu-id="0fff1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0fff1-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fff1-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fff1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0fff1-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0fff1-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0fff1-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fff1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0fff1-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0fff1-118">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0fff1-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fff1-119">Namespace</span></span><br/>                | <span data-ttu-id="0fff1-120">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="0fff1-120">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0fff1-121">MOF</span><span class="sxs-lookup"><span data-stu-id="0fff1-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fff1-122"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fff1-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fff1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0fff1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fff1-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fff1-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0fff1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fff1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fff1-126">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="0fff1-126">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





