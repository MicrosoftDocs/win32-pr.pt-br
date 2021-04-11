---
title: Classe Win32_RDMSDesktopAssignment
description: Descreve a atribuição da área de trabalho do usuário da coleção RD.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSDesktopAssignment Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSDesktopAssignment classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295779"
---
# <a name="win32_rdmsdesktopassignment-class"></a><span data-ttu-id="a078d-105">\_Classe Win32 RDMSDesktopAssignment</span><span class="sxs-lookup"><span data-stu-id="a078d-105">Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="a078d-106">Descreve a atribuição da área de trabalho do usuário da coleção RD.</span><span class="sxs-lookup"><span data-stu-id="a078d-106">Describes the RD collection User Desktop assignment.</span></span>

<span data-ttu-id="a078d-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a078d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a078d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a078d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a><span data-ttu-id="a078d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a078d-109">Members</span></span>

<span data-ttu-id="a078d-110">A classe **Win32 \_ RDMSDesktopAssignment** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a078d-110">The **Win32\_RDMSDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="a078d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a078d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a078d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a078d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a078d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a078d-113">Methods</span></span>

<span data-ttu-id="a078d-114">A classe **Win32 \_ RDMSDesktopAssignment** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a078d-114">The **Win32\_RDMSDesktopAssignment** class has these methods.</span></span>



| <span data-ttu-id="a078d-115">Método</span><span class="sxs-lookup"><span data-stu-id="a078d-115">Method</span></span>                                                                                 | <span data-ttu-id="a078d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a078d-116">Description</span></span>                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="a078d-117">**AddDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="a078d-117">**AddDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-adddesktopassignment.md)       | <span data-ttu-id="a078d-118">Adiciona uma atribuição de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a078d-118">Adds a desktop assignment.</span></span><br/>    |
| [<span data-ttu-id="a078d-119">**RemoveDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="a078d-119">**RemoveDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-removedesktopassignment.md) | <span data-ttu-id="a078d-120">Remove uma atribuição de desktop.</span><span class="sxs-lookup"><span data-stu-id="a078d-120">Removes a desktop assignment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a078d-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a078d-121">Properties</span></span>

<span data-ttu-id="a078d-122">A classe **Win32 \_ RDMSDesktopAssignment** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a078d-122">The **Win32\_RDMSDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a078d-123">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="a078d-123">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a078d-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a078d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a078d-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a078d-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a078d-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a078d-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a078d-127">Alias da coleção.</span><span class="sxs-lookup"><span data-stu-id="a078d-127">Alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="a078d-128">**Área de trabalho**</span><span class="sxs-lookup"><span data-stu-id="a078d-128">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a078d-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a078d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a078d-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a078d-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a078d-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a078d-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a078d-132">O nome da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a078d-132">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="a078d-133">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="a078d-133">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a078d-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a078d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a078d-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a078d-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a078d-136">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a078d-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a078d-137">O nome de domínio da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="a078d-137">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="a078d-138">**UserName**</span><span class="sxs-lookup"><span data-stu-id="a078d-138">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a078d-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a078d-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a078d-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a078d-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a078d-141">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a078d-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a078d-142">O nome da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="a078d-142">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a078d-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a078d-143">Requirements</span></span>



| <span data-ttu-id="a078d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a078d-144">Requirement</span></span> | <span data-ttu-id="a078d-145">Valor</span><span class="sxs-lookup"><span data-stu-id="a078d-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a078d-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a078d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a078d-147">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a078d-147">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a078d-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a078d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a078d-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a078d-149">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="a078d-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="a078d-150">Namespace</span></span><br/>                | <span data-ttu-id="a078d-151">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="a078d-151">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a078d-152">MOF</span><span class="sxs-lookup"><span data-stu-id="a078d-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a078d-153"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a078d-153"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a078d-154">DLL</span><span class="sxs-lookup"><span data-stu-id="a078d-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a078d-155"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a078d-155"><dt>RDMS.dll</dt></span></span> </dl>         |



 

