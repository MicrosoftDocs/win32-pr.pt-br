---
title: Método GetSecondaryConnectionString da classe Win32_RDMSDeploymentSettings
description: Recupera a cadeia de conexão secundária do banco de dados no nível da implantação, que pode ser usada para dar suporte à expiração da senha.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetSecondaryConnectionString
- Método GetSecondaryConnectionString Serviços de Área de Trabalho Remota, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota, método GetSecondaryConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295776"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="ae057-106">Método GetSecondaryConnectionString da classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="ae057-106">GetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="ae057-107">Recupera a cadeia de conexão secundária do banco de dados no nível da implantação, que pode ser usada para dar suporte à expiração da senha.</span><span class="sxs-lookup"><span data-stu-id="ae057-107">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae057-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae057-108">Syntax</span></span>


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="ae057-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae057-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae057-110">*SecondaryConnectionString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ae057-110">*SecondaryConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae057-111">A cadeia de conexão a ser recuperada</span><span class="sxs-lookup"><span data-stu-id="ae057-111">The connection string to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae057-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae057-112">Return value</span></span>

<span data-ttu-id="ae057-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="ae057-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae057-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae057-114">Requirements</span></span>



| <span data-ttu-id="ae057-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae057-115">Requirement</span></span> | <span data-ttu-id="ae057-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ae057-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae057-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae057-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ae057-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ae057-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ae057-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae057-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ae057-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ae057-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="ae057-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae057-121">Namespace</span></span><br/>                | <span data-ttu-id="ae057-122">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="ae057-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ae057-123">MOF</span><span class="sxs-lookup"><span data-stu-id="ae057-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae057-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae057-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae057-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ae057-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae057-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae057-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ae057-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae057-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae057-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="ae057-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





