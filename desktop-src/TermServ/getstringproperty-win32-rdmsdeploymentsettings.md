---
title: Método getstringproperty da classe Win32_RDMSDeploymentSettings
description: Recupera uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- Método getstringproperty Serviços de Área de Trabalho Remota
- Método getstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método getstringproperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369450"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="05238-106">Método getstringproperty da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="05238-106">GetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="05238-107">Recupera uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="05238-107">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="05238-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05238-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="05238-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05238-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05238-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="05238-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05238-111">O alias para a coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="05238-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="05238-112">*Valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="05238-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05238-113">Uma cadeia de caracteres que recebe o valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="05238-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05238-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05238-114">Requirements</span></span>



| <span data-ttu-id="05238-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="05238-115">Requirement</span></span> | <span data-ttu-id="05238-116">Valor</span><span class="sxs-lookup"><span data-stu-id="05238-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="05238-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05238-117">Minimum supported client</span></span><br/> | <span data-ttu-id="05238-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="05238-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="05238-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05238-119">Minimum supported server</span></span><br/> | <span data-ttu-id="05238-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05238-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="05238-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="05238-121">Namespace</span></span><br/>                | <span data-ttu-id="05238-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="05238-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="05238-123">MOF</span><span class="sxs-lookup"><span data-stu-id="05238-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05238-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05238-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="05238-125">DLL</span><span class="sxs-lookup"><span data-stu-id="05238-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05238-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05238-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="05238-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="05238-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05238-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="05238-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





