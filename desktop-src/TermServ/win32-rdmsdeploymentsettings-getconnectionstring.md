---
title: Método GetConnectionString da classe Win32_RDMSDeploymentSettings
description: Recupera a cadeia de conexão do banco de dados de nível de implantação.
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- Método GetConnectionString Serviços de Área de Trabalho Remota
- Método GetConnectionString Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método GetConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6476c938f62e0cd0e1f9d034c89fded50994946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455268"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="8eb3b-106">Método GetConnectionString da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="8eb3b-106">GetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="8eb3b-107">Recupera a cadeia de conexão do banco de dados de nível de implantação.</span><span class="sxs-lookup"><span data-stu-id="8eb3b-107">Retrieves the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb3b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8eb3b-108">Syntax</span></span>


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="8eb3b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8eb3b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb3b-110">*ConnectionString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8eb3b-110">*ConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8eb3b-111">A cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="8eb3b-111">The connection string</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eb3b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8eb3b-112">Return value</span></span>

<span data-ttu-id="8eb3b-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="8eb3b-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb3b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eb3b-114">Requirements</span></span>



| <span data-ttu-id="8eb3b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb3b-115">Requirement</span></span> | <span data-ttu-id="8eb3b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8eb3b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb3b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eb3b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb3b-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8eb3b-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8eb3b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eb3b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb3b-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8eb3b-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="8eb3b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="8eb3b-121">Namespace</span></span><br/>                | <span data-ttu-id="8eb3b-122">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="8eb3b-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8eb3b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="8eb3b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8eb3b-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8eb3b-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8eb3b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8eb3b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eb3b-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eb3b-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8eb3b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8eb3b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb3b-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="8eb3b-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





