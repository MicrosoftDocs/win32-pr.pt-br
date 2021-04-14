---
title: Método Join da classe Win32_RDMSJoinedNode
description: Adiciona um nó a serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de junção
- Método Join Serviços de Área de Trabalho Remota, classe Win32_RDMSJoinedNode
- Serviços de Área de Trabalho Remota de classe Win32_RDMSJoinedNode, método Join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369364"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="fae37-106">Método Join da classe Win32 \_ RDMSJoinedNode</span><span class="sxs-lookup"><span data-stu-id="fae37-106">Join method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="fae37-107">Adiciona um nó a serviços de gerenciamento de Área de Trabalho Remota (RDMS).</span><span class="sxs-lookup"><span data-stu-id="fae37-107">Adds a node to Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="fae37-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fae37-108">Syntax</span></span>


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a><span data-ttu-id="fae37-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fae37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae37-110">*NodeFQDN* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fae37-110">*NodeFQDN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fae37-111">O nome de domínio totalmente qualificado do nó.</span><span class="sxs-lookup"><span data-stu-id="fae37-111">The fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="fae37-112">*NodeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fae37-112">*NodeSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fae37-113">O identificador de segurança (SID) do nó.</span><span class="sxs-lookup"><span data-stu-id="fae37-113">The security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae37-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fae37-114">Return value</span></span>

<span data-ttu-id="fae37-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="fae37-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fae37-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fae37-116">Requirements</span></span>



| <span data-ttu-id="fae37-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae37-117">Requirement</span></span> | <span data-ttu-id="fae37-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fae37-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae37-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fae37-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fae37-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fae37-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fae37-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fae37-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fae37-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fae37-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fae37-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="fae37-123">Namespace</span></span><br/>                | <span data-ttu-id="fae37-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="fae37-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fae37-125">MOF</span><span class="sxs-lookup"><span data-stu-id="fae37-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fae37-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fae37-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fae37-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fae37-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fae37-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fae37-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fae37-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fae37-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae37-130">**\_RDMSJoinedNode Win32**</span><span class="sxs-lookup"><span data-stu-id="fae37-130">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





