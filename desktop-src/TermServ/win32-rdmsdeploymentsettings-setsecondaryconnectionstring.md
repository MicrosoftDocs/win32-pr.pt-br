---
title: Método SetSecondaryConnectionString da classe Win32_RDMSDeploymentSettings
description: Define a cadeia de conexão secundária do banco de dados de nível de implantação.
ms.assetid: 154c495e-564e-4d90-a4ff-de683d41aa73
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSecondaryConnectionString
- Método SetSecondaryConnectionString Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método SetSecondaryConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8060a6f2676b5599bf44672e79ebf48e64e354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644550"
---
# <a name="setsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="f5327-106">Método SetSecondaryConnectionString da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="f5327-106">SetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="f5327-107">Define a cadeia de conexão secundária do banco de dados de nível de implantação.</span><span class="sxs-lookup"><span data-stu-id="f5327-107">Sets the deployment level database secondary connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5327-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5327-108">Syntax</span></span>


```mof
uint32 SetSecondaryConnectionString(
  [in] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="f5327-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5327-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5327-110">*SecondaryConnectionString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5327-110">*SecondaryConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5327-111">A cadeia de conexão a ser definida</span><span class="sxs-lookup"><span data-stu-id="f5327-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5327-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5327-112">Return value</span></span>

<span data-ttu-id="f5327-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="f5327-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5327-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5327-114">Requirements</span></span>



| <span data-ttu-id="f5327-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5327-115">Requirement</span></span> | <span data-ttu-id="f5327-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f5327-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5327-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5327-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f5327-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f5327-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f5327-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5327-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f5327-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f5327-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="f5327-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5327-121">Namespace</span></span><br/>                | <span data-ttu-id="f5327-122">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="f5327-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f5327-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f5327-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5327-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5327-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5327-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f5327-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5327-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5327-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f5327-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5327-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5327-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="f5327-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





