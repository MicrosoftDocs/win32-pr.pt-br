---
title: Método GetClientAccessName da classe Win32_RDMSEnvironment
description: Recupera o nome do registro de recurso (DNS) do sistema de nomes de domínio (RR) do ambiente dos serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetClientAccessName
- Método GetClientAccessName Serviços de Área de Trabalho Remota, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Serviços de Área de Trabalho Remota, método GetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760132"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="e5f39-106">Método GetClientAccessName da classe Win32 \_ RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="e5f39-106">GetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="e5f39-107">Recupera o nome do registro de recurso (DNS) do sistema de nomes de domínio (RR) do ambiente dos serviços de gerenciamento de Área de Trabalho Remota (RDMS).</span><span class="sxs-lookup"><span data-stu-id="e5f39-107">Retrieves the Domain Name System (DNS) resource record (RR) name of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f39-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5f39-108">Syntax</span></span>


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="e5f39-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5f39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5f39-110">*ClientAccessName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e5f39-110">*ClientAccessName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f39-111">Recebe o nome do RR recuperado.</span><span class="sxs-lookup"><span data-stu-id="e5f39-111">Receives the retrieved RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5f39-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5f39-112">Return value</span></span>

<span data-ttu-id="e5f39-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="e5f39-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5f39-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5f39-114">Requirements</span></span>



| <span data-ttu-id="e5f39-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5f39-115">Requirement</span></span> | <span data-ttu-id="e5f39-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e5f39-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5f39-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5f39-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e5f39-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e5f39-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e5f39-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5f39-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e5f39-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5f39-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e5f39-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5f39-121">Namespace</span></span><br/>                | <span data-ttu-id="e5f39-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="e5f39-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e5f39-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e5f39-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5f39-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5f39-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5f39-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e5f39-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5f39-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5f39-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e5f39-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5f39-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5f39-128">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="e5f39-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





