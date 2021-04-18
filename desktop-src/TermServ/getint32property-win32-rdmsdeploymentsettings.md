---
title: Método getint32property da classe Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. appanalysis. h)
description: Recupera uma propriedade de número inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Método getint32property Serviços de Área de Trabalho Remota
- Método getint32property Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método getint32property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810986"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="41cc0-106">Método getint32property da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="41cc0-106">GetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="41cc0-107">Recupera uma propriedade de número inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="41cc0-107">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="41cc0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41cc0-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="41cc0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41cc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41cc0-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41cc0-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41cc0-111">O alias para a coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="41cc0-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="41cc0-112">*Valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="41cc0-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41cc0-113">Um inteiro que recebe o valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="41cc0-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41cc0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41cc0-114">Requirements</span></span>



| <span data-ttu-id="41cc0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="41cc0-115">Requirement</span></span> | <span data-ttu-id="41cc0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="41cc0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41cc0-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41cc0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41cc0-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="41cc0-118">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="41cc0-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41cc0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41cc0-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="41cc0-120">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="41cc0-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="41cc0-121">Namespace</span></span><br/>                | <span data-ttu-id="41cc0-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="41cc0-122">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="41cc0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41cc0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="41cc0-124"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="41cc0-124"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="41cc0-125">MOF</span><span class="sxs-lookup"><span data-stu-id="41cc0-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41cc0-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41cc0-126"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="41cc0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="41cc0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41cc0-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41cc0-128"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="41cc0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="41cc0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41cc0-130">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="41cc0-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





