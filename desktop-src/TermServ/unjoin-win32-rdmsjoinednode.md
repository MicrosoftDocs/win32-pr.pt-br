---
title: Método Unjoin da classe Win32_RDMSJoinedNode
description: Remove um nó de serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método Unjoin
- Método Unjoin Serviços de Área de Trabalho Remota, classe Win32_RDMSJoinedNode
- Classe Win32_RDMSJoinedNode Serviços de Área de Trabalho Remota, método Unjoin
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Unjoin
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234f7cc3ad8a797fff51661528f4545ed9fea3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810427"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="0c7b9-106">Método Unjoin da classe Win32 \_ RDMSJoinedNode</span><span class="sxs-lookup"><span data-stu-id="0c7b9-106">Unjoin method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="0c7b9-107">Remove um nó de serviços de gerenciamento de Área de Trabalho Remota (RDMS).</span><span class="sxs-lookup"><span data-stu-id="0c7b9-107">Removes a node from Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c7b9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c7b9-108">Syntax</span></span>


```mof
uint32 Unjoin();
```



## <a name="parameters"></a><span data-ttu-id="0c7b9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c7b9-109">Parameters</span></span>

<span data-ttu-id="0c7b9-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0c7b9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c7b9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c7b9-111">Return value</span></span>

<span data-ttu-id="0c7b9-112">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="0c7b9-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c7b9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c7b9-113">Requirements</span></span>



| <span data-ttu-id="0c7b9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c7b9-114">Requirement</span></span> | <span data-ttu-id="0c7b9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0c7b9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c7b9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c7b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0c7b9-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0c7b9-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0c7b9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c7b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0c7b9-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c7b9-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0c7b9-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c7b9-120">Namespace</span></span><br/>                | <span data-ttu-id="0c7b9-121">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="0c7b9-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0c7b9-122">MOF</span><span class="sxs-lookup"><span data-stu-id="0c7b9-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c7b9-123"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c7b9-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c7b9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0c7b9-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c7b9-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c7b9-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0c7b9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c7b9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c7b9-127">**\_RDMSJoinedNode Win32**</span><span class="sxs-lookup"><span data-stu-id="0c7b9-127">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





