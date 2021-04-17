---
title: Método setint32property da classe Win32_RDMSDeploymentSettings
description: Atualiza uma propriedade de inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- Método setint32property Serviços de Área de Trabalho Remota
- Método setint32property Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método setint32property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761931"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="0d1bd-106">Método setint32property da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="0d1bd-106">SetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="0d1bd-107">Atualiza uma propriedade de inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="0d1bd-107">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d1bd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d1bd-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="0d1bd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d1bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d1bd-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d1bd-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d1bd-111">O alias para a coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="0d1bd-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="0d1bd-112">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0d1bd-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d1bd-113">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0d1bd-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d1bd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d1bd-114">Requirements</span></span>



| <span data-ttu-id="0d1bd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d1bd-115">Requirement</span></span> | <span data-ttu-id="0d1bd-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0d1bd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1bd-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d1bd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1bd-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0d1bd-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0d1bd-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d1bd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1bd-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d1bd-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0d1bd-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d1bd-121">Namespace</span></span><br/>                | <span data-ttu-id="0d1bd-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="0d1bd-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0d1bd-123">MOF</span><span class="sxs-lookup"><span data-stu-id="0d1bd-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d1bd-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d1bd-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d1bd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0d1bd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d1bd-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d1bd-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0d1bd-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d1bd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1bd-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="0d1bd-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





