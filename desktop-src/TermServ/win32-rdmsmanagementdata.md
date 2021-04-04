---
title: Classe Win32_RDMSManagementData
description: Sincroniza dados de publicação para serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSManagementData Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSManagementData classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008960"
---
# <a name="win32_rdmsmanagementdata-class"></a><span data-ttu-id="17082-105">\_Classe Win32 RDMSManagementData</span><span class="sxs-lookup"><span data-stu-id="17082-105">Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="17082-106">Sincroniza dados de publicação para serviços de gerenciamento de Área de Trabalho Remota (RDMS).</span><span class="sxs-lookup"><span data-stu-id="17082-106">Synchronizes publishing data for Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="17082-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="17082-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17082-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17082-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a><span data-ttu-id="17082-109">Membros</span><span class="sxs-lookup"><span data-stu-id="17082-109">Members</span></span>

<span data-ttu-id="17082-110">A classe **Win32 \_ RDMSManagementData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="17082-110">The **Win32\_RDMSManagementData** class has these types of members:</span></span>

-   [<span data-ttu-id="17082-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="17082-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="17082-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="17082-112">Methods</span></span>

<span data-ttu-id="17082-113">A classe **Win32 \_ RDMSManagementData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="17082-113">The **Win32\_RDMSManagementData** class has these methods.</span></span>



| <span data-ttu-id="17082-114">Método</span><span class="sxs-lookup"><span data-stu-id="17082-114">Method</span></span>                                                                                        | <span data-ttu-id="17082-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="17082-115">Description</span></span>                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="17082-116">**SynchronizeAllPublishingData**</span><span class="sxs-lookup"><span data-stu-id="17082-116">**SynchronizeAllPublishingData**</span></span>](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | <span data-ttu-id="17082-117">Sincroniza todos os dados de publicação para RDMS.</span><span class="sxs-lookup"><span data-stu-id="17082-117">Synchronizes all publishing data for RDMS.</span></span><br/>                  |
| [<span data-ttu-id="17082-118">**SynchronizePublishingData**</span><span class="sxs-lookup"><span data-stu-id="17082-118">**SynchronizePublishingData**</span></span>](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | <span data-ttu-id="17082-119">Sincroniza o conjunto especificado de dados de publicação para RDMS.</span><span class="sxs-lookup"><span data-stu-id="17082-119">Synchronizes the specified set of publishing data for RDMS.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17082-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17082-120">Requirements</span></span>



| <span data-ttu-id="17082-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="17082-121">Requirement</span></span> | <span data-ttu-id="17082-122">Valor</span><span class="sxs-lookup"><span data-stu-id="17082-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="17082-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17082-123">Minimum supported client</span></span><br/> | <span data-ttu-id="17082-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="17082-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="17082-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17082-125">Minimum supported server</span></span><br/> | <span data-ttu-id="17082-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17082-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="17082-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="17082-127">Namespace</span></span><br/>                | <span data-ttu-id="17082-128">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="17082-128">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="17082-129">MOF</span><span class="sxs-lookup"><span data-stu-id="17082-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17082-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17082-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="17082-131">DLL</span><span class="sxs-lookup"><span data-stu-id="17082-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17082-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17082-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="17082-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="17082-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17082-134">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="17082-134">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





