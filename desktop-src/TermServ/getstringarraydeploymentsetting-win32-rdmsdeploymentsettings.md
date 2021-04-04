---
title: Método GetStringArrayDeploymentSetting da classe Win32_RDMSDeploymentSettings
description: Recupera as configurações de implantação para uma coleção de áreas de trabalho virtuais.
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetStringArrayDeploymentSetting
- Método GetStringArrayDeploymentSetting Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método GetStringArrayDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085308"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="f2bb9-106">Método GetStringArrayDeploymentSetting da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="f2bb9-106">GetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="f2bb9-107">Recupera as configurações de implantação para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="f2bb9-107">Retrieves the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2bb9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2bb9-108">Syntax</span></span>


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="f2bb9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2bb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2bb9-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2bb9-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bb9-111">O alias da coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="f2bb9-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="f2bb9-112">*Valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f2bb9-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bb9-113">Recebe uma matriz de cadeias de caracteres que contém as configurações de implantação.</span><span class="sxs-lookup"><span data-stu-id="f2bb9-113">Receives an array of strings that contains the deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2bb9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2bb9-114">Requirements</span></span>



| <span data-ttu-id="f2bb9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2bb9-115">Requirement</span></span> | <span data-ttu-id="f2bb9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f2bb9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bb9-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2bb9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2bb9-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f2bb9-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f2bb9-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2bb9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2bb9-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2bb9-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f2bb9-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2bb9-121">Namespace</span></span><br/>                | <span data-ttu-id="f2bb9-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="f2bb9-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f2bb9-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f2bb9-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2bb9-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2bb9-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2bb9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f2bb9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2bb9-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2bb9-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f2bb9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2bb9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2bb9-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="f2bb9-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





