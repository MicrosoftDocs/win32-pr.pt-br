---
title: Método GetPendingStartServerList da classe Win32_RDSHServer
description: Recupera uma lista de servidores que estão aguardando para serem iniciados.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetPendingStartServerList
- Método GetPendingStartServerList Serviços de Área de Trabalho Remota, classe Win32_RDSHServer
- Classe Win32_RDSHServer Serviços de Área de Trabalho Remota, método GetPendingStartServerList
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369665"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="e8170-106">Método GetPendingStartServerList da classe Win32 \_ RDSHServer</span><span class="sxs-lookup"><span data-stu-id="e8170-106">GetPendingStartServerList method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="e8170-107">Recupera uma lista de servidores que estão aguardando para serem iniciados.</span><span class="sxs-lookup"><span data-stu-id="e8170-107">Retrieves a list of server waiting to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8170-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8170-108">Syntax</span></span>


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a><span data-ttu-id="e8170-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8170-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8170-110">*maxServers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8170-110">*maxServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8170-111">O número máximo de servidores a serem retornados na lista.</span><span class="sxs-lookup"><span data-stu-id="e8170-111">The maximum number of servers to return in the list.</span></span>

</dd> <dt>

<span data-ttu-id="e8170-112">*ServerFQDNs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e8170-112">*ServerFQDNs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8170-113">Em caso de sucesso, contém uma coleção de nomes de domínio totalmente qualificados dos servidores que estão aguardando para iniciar.</span><span class="sxs-lookup"><span data-stu-id="e8170-113">On success, contains a collection of fully-qualified domain names of the servers waiting to start.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8170-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8170-114">Remarks</span></span>

<span data-ttu-id="e8170-115">A lista de servidores é redefinida após cada chamada, para que a próxima chamada não obtenha um servidor duplicado.</span><span class="sxs-lookup"><span data-stu-id="e8170-115">The list of servers is reset after every call, so that the next call will not get a duplicate server.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8170-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8170-116">Requirements</span></span>



| <span data-ttu-id="e8170-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8170-117">Requirement</span></span> | <span data-ttu-id="e8170-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e8170-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8170-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8170-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8170-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e8170-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e8170-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8170-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8170-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e8170-122">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="e8170-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8170-123">Namespace</span></span><br/>                | <span data-ttu-id="e8170-124">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="e8170-124">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e8170-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e8170-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8170-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8170-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8170-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e8170-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8170-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8170-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e8170-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8170-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8170-130">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="e8170-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





