---
title: Método setconnectionstring da classe Win32_RDMSDeploymentSettings
description: Define a cadeia de conexão do banco de dados de nível de implantação.
ms.assetid: c8902ab9-72a6-4d69-ab22-f6074205deb4
ms.tgt_platform: multiple
keywords:
- Método setconnectionstring Serviços de Área de Trabalho Remota
- Método setconnectionstring Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método setconnectionstring
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ccb3f618f6a08dcb95bb7dc04c1494be6a7b5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369510"
---
# <a name="setconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="53879-106">Método setconnectionstring da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="53879-106">SetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="53879-107">Define a cadeia de conexão do banco de dados de nível de implantação.</span><span class="sxs-lookup"><span data-stu-id="53879-107">Sets the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="53879-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53879-108">Syntax</span></span>


```mof
uint32 SetConnectionString(
  [in] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="53879-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53879-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53879-110">*ConnectionString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53879-110">*ConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53879-111">A cadeia de conexão a ser definida</span><span class="sxs-lookup"><span data-stu-id="53879-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53879-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53879-112">Return value</span></span>

<span data-ttu-id="53879-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="53879-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53879-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53879-114">Requirements</span></span>



| <span data-ttu-id="53879-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="53879-115">Requirement</span></span> | <span data-ttu-id="53879-116">Valor</span><span class="sxs-lookup"><span data-stu-id="53879-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="53879-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53879-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53879-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="53879-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="53879-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53879-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53879-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="53879-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="53879-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="53879-121">Namespace</span></span><br/>                | <span data-ttu-id="53879-122">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="53879-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="53879-123">MOF</span><span class="sxs-lookup"><span data-stu-id="53879-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53879-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53879-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="53879-125">DLL</span><span class="sxs-lookup"><span data-stu-id="53879-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53879-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53879-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="53879-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="53879-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53879-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="53879-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





