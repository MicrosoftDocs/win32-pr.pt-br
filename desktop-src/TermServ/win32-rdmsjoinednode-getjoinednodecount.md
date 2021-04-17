---
title: Método GetJoinedNodeCount da classe Win32_RDMSJoinedNode
description: Obtém o número de servidores que têm as funções especificadas instaladas.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetJoinedNodeCount
- Método GetJoinedNodeCount Serviços de Área de Trabalho Remota, classe Win32_RDMSJoinedNode
- Classe Win32_RDMSJoinedNode Serviços de Área de Trabalho Remota, método GetJoinedNodeCount
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754161"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="9d892-106">Método GetJoinedNodeCount da classe Win32 \_ RDMSJoinedNode</span><span class="sxs-lookup"><span data-stu-id="9d892-106">GetJoinedNodeCount method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="9d892-107">Obtém o número de servidores que têm as funções especificadas instaladas.</span><span class="sxs-lookup"><span data-stu-id="9d892-107">Get number of servers that have the specified roles installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d892-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d892-108">Syntax</span></span>


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a><span data-ttu-id="9d892-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d892-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d892-110">*RoleType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d892-110">*roleType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d892-111">Um campo de bits que especifica os tipos de função.</span><span class="sxs-lookup"><span data-stu-id="9d892-111">A bitfield that specifies the role types.</span></span>

<dt>

<span data-ttu-id="9d892-112">0</span><span class="sxs-lookup"><span data-stu-id="9d892-112">0</span></span>
</dt> <dd>

<span data-ttu-id="9d892-113">Tudo</span><span class="sxs-lookup"><span data-stu-id="9d892-113">All</span></span>

</dd> <dt>

<span data-ttu-id="9d892-114">1</span><span class="sxs-lookup"><span data-stu-id="9d892-114">1</span></span>
</dt> <dd>

<span data-ttu-id="9d892-115">Agente de Conexão de Área de Trabalho Remota (RDCB)</span><span class="sxs-lookup"><span data-stu-id="9d892-115">Remote Desktop Connection Broker (RDCB)</span></span>

</dd> <dt>

<span data-ttu-id="9d892-116">2</span><span class="sxs-lookup"><span data-stu-id="9d892-116">2</span></span>
</dt> <dd>

<span data-ttu-id="9d892-117">Host da Sessão da Área de Trabalho Remota (RDSH)</span><span class="sxs-lookup"><span data-stu-id="9d892-117">Remote Desktop Session Host (RDSH)</span></span>

</dd> <dt>

<span data-ttu-id="9d892-118">4</span><span class="sxs-lookup"><span data-stu-id="9d892-118">4</span></span>
</dt> <dd>

<span data-ttu-id="9d892-119">Host de Virtualização de Área de Trabalho Remota (RDVH)</span><span class="sxs-lookup"><span data-stu-id="9d892-119">Remote Desktop Virtualization Host (RDVH)</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9d892-120">*Contagem* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="9d892-120">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d892-121">Em caso de sucesso, retorna o número de servidores com as funções especificadas instaladas.</span><span class="sxs-lookup"><span data-stu-id="9d892-121">On success, returns the number of servers with the specified roles installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d892-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d892-122">Return value</span></span>

<span data-ttu-id="9d892-123">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="9d892-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d892-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d892-124">Requirements</span></span>



| <span data-ttu-id="9d892-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d892-125">Requirement</span></span> | <span data-ttu-id="9d892-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9d892-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d892-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d892-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9d892-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9d892-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9d892-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d892-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9d892-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9d892-130">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="9d892-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d892-131">Namespace</span></span><br/>                | <span data-ttu-id="9d892-132">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="9d892-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9d892-133">MOF</span><span class="sxs-lookup"><span data-stu-id="9d892-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d892-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d892-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d892-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9d892-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d892-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d892-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9d892-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d892-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d892-138">**\_RDMSJoinedNode Win32**</span><span class="sxs-lookup"><span data-stu-id="9d892-138">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





