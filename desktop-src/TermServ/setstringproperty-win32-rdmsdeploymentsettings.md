---
title: Método setstringproperty da classe Win32_RDMSDeploymentSettings (CertEnroll. h)
description: Atualiza uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- Método setstringproperty Serviços de Área de Trabalho Remota
- Método setstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método setstringproperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138f6d91ed428caabf8da69e3d958675f879dd15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085864"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="b65cc-106">Método setstringproperty da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="b65cc-106">SetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="b65cc-107">Atualiza uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b65cc-107">Updates a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b65cc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b65cc-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="b65cc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b65cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b65cc-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b65cc-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b65cc-111">O alias para a coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b65cc-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="b65cc-112">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b65cc-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b65cc-113">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="b65cc-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b65cc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b65cc-114">Requirements</span></span>



| <span data-ttu-id="b65cc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b65cc-115">Requirement</span></span> | <span data-ttu-id="b65cc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b65cc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b65cc-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b65cc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b65cc-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b65cc-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b65cc-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b65cc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b65cc-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b65cc-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b65cc-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b65cc-121">Namespace</span></span><br/>                | <span data-ttu-id="b65cc-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="b65cc-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b65cc-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b65cc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b65cc-124"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="b65cc-124"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="b65cc-125">MOF</span><span class="sxs-lookup"><span data-stu-id="b65cc-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b65cc-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b65cc-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b65cc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b65cc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b65cc-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b65cc-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b65cc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b65cc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b65cc-130">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b65cc-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





