---
title: Classe Win32_RDMSEnvironment
description: Gerencia um ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSEnvironment Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSEnvironment classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754162"
---
# <a name="win32_rdmsenvironment-class"></a><span data-ttu-id="55045-105">\_Classe Win32 RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="55045-105">Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="55045-106">Gerencia um ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).</span><span class="sxs-lookup"><span data-stu-id="55045-106">Manages a Remote Desktop Management Services (RDMS) environment.</span></span>

<span data-ttu-id="55045-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="55045-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="55045-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55045-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a><span data-ttu-id="55045-109">Membros</span><span class="sxs-lookup"><span data-stu-id="55045-109">Members</span></span>

<span data-ttu-id="55045-110">A classe **Win32 \_ RDMSEnvironment** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="55045-110">The **Win32\_RDMSEnvironment** class has these types of members:</span></span>

-   [<span data-ttu-id="55045-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="55045-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="55045-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="55045-112">Methods</span></span>

<span data-ttu-id="55045-113">A classe **Win32 \_ RDMSEnvironment** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="55045-113">The **Win32\_RDMSEnvironment** class has these methods.</span></span>



| <span data-ttu-id="55045-114">Método</span><span class="sxs-lookup"><span data-stu-id="55045-114">Method</span></span>                                                                   | <span data-ttu-id="55045-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="55045-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55045-116">**GetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="55045-116">**GetActiveServer**</span></span>](getactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="55045-117">Recupera o FQDN (nome de domínio totalmente qualificado) do ambiente de RDMS.</span><span class="sxs-lookup"><span data-stu-id="55045-117">Retrieves the fully qualified domain name (FQDN) of the RDMS environment.</span></span><br/>                 |
| [<span data-ttu-id="55045-118">**GetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="55045-118">**GetClientAccessName**</span></span>](getclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="55045-119">Recupera o nome do registro de recurso (DNS) do sistema de nome de domínio (RR) do ambiente de RDMS.</span><span class="sxs-lookup"><span data-stu-id="55045-119">Retrieves the Domain Name System (DNS) resource record (RR) name of the RDMS environment.</span></span><br/> |
| [<span data-ttu-id="55045-120">**SetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="55045-120">**SetActiveServer**</span></span>](setactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="55045-121">Define o FQDN do ambiente de RDMS para o nó atual.</span><span class="sxs-lookup"><span data-stu-id="55045-121">Sets the FQDN of the RDMS environment to the current node.</span></span><br/>                                |
| [<span data-ttu-id="55045-122">**SetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="55045-122">**SetClientAccessName**</span></span>](setclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="55045-123">Atualiza o nome do RR DNS do ambiente de RDMS.</span><span class="sxs-lookup"><span data-stu-id="55045-123">Updates the DNS RR name of the RDMS environment.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="55045-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55045-124">Requirements</span></span>



| <span data-ttu-id="55045-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="55045-125">Requirement</span></span> | <span data-ttu-id="55045-126">Valor</span><span class="sxs-lookup"><span data-stu-id="55045-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="55045-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55045-127">Minimum supported client</span></span><br/> | <span data-ttu-id="55045-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="55045-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="55045-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55045-129">Minimum supported server</span></span><br/> | <span data-ttu-id="55045-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55045-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="55045-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="55045-131">Namespace</span></span><br/>                | <span data-ttu-id="55045-132">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="55045-132">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="55045-133">MOF</span><span class="sxs-lookup"><span data-stu-id="55045-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55045-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55045-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="55045-135">DLL</span><span class="sxs-lookup"><span data-stu-id="55045-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55045-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55045-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="55045-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="55045-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55045-138">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="55045-138">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





