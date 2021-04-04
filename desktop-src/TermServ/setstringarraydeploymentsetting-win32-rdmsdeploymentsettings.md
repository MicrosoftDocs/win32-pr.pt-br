---
title: Método SetStringArrayDeploymentSetting da classe Win32_RDMSDeploymentSettings
description: Atualiza as configurações de implantação para uma coleção de áreas de trabalho virtuais.
ms.assetid: 386594bd-a793-4e5d-ad2c-217951bee9f6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetStringArrayDeploymentSetting
- Método SetStringArrayDeploymentSetting Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método SetStringArrayDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb5ecc6d1238b739f8fe19d02e96ba427ed09b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645147"
---
# <a name="setstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="4ee84-106">Método SetStringArrayDeploymentSetting da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="4ee84-106">SetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="4ee84-107">Atualiza as configurações de implantação para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="4ee84-107">Updates the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee84-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ee84-108">Syntax</span></span>


```mof
uint32 SetStringArrayDeploymentSetting(
  [in] string Key,
  [in] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="4ee84-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ee84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee84-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ee84-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee84-111">O alias da coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="4ee84-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="4ee84-112">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4ee84-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee84-113">Uma matriz de cadeias de caracteres que contém as novas configurações de implantação.</span><span class="sxs-lookup"><span data-stu-id="4ee84-113">An array of strings that contains the new deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ee84-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ee84-114">Requirements</span></span>



| <span data-ttu-id="4ee84-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ee84-115">Requirement</span></span> | <span data-ttu-id="4ee84-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee84-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee84-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ee84-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4ee84-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4ee84-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4ee84-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ee84-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4ee84-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ee84-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="4ee84-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ee84-121">Namespace</span></span><br/>                | <span data-ttu-id="4ee84-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="4ee84-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4ee84-123">MOF</span><span class="sxs-lookup"><span data-stu-id="4ee84-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ee84-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ee84-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ee84-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4ee84-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ee84-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ee84-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4ee84-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ee84-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee84-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="4ee84-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





