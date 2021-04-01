---
description: A \_ Associação Win32 SessionResource representa a relação entre uma sessão e os recursos aos quais a sessão fornece acesso.
ms.assetid: 39c195cf-e70b-4e93-b46b-61ed4f08f57e
ms.tgt_platform: multiple
title: Classe Win32_SessionResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionResource
- Win32_SessionResource.Antecedent
- Win32_SessionResource.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 3962c8523863bb97710bf21be38906d3897beea3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646471"
---
# <a name="win32_sessionresource-class"></a><span data-ttu-id="595b5-103">\_Classe Win32 SessionResource</span><span class="sxs-lookup"><span data-stu-id="595b5-103">Win32\_SessionResource class</span></span>

<span data-ttu-id="595b5-104">A \_ Associação Win32 SessionResource representa a relação entre uma sessão e os recursos aos quais a sessão fornece acesso.</span><span class="sxs-lookup"><span data-stu-id="595b5-104">The Win32\_SessionResource association represents the relationship between a session and the resources that the session provides access to.</span></span>

<span data-ttu-id="595b5-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="595b5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="595b5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="595b5-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SessionResource : CIM_Dependency
{
  Win32_LogicalElement REF Antecedent;
  Win32_Session        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="595b5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="595b5-107">Members</span></span>

<span data-ttu-id="595b5-108">A classe **Win32 \_ SessionResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="595b5-108">The **Win32\_SessionResource** class has these types of members:</span></span>

-   [<span data-ttu-id="595b5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="595b5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="595b5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="595b5-110">Properties</span></span>

<span data-ttu-id="595b5-111">A classe **Win32 \_ SessionResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="595b5-111">The **Win32\_SessionResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="595b5-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="595b5-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="595b5-113">Tipo de dados: **Win32 \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="595b5-113">Data type: **Win32\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="595b5-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="595b5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="595b5-115">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="595b5-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="595b5-116">A referência Antecedent representa os recursos usados por esta sessão.</span><span class="sxs-lookup"><span data-stu-id="595b5-116">The Antecedent reference represents resources used by this session.</span></span>

</dd> <dt>

<span data-ttu-id="595b5-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="595b5-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="595b5-118">Tipo de dados **: \_ sessão Win32**</span><span class="sxs-lookup"><span data-stu-id="595b5-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="595b5-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="595b5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="595b5-120">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="595b5-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="595b5-121">A referência Dependent representa a sessão usando o recurso.</span><span class="sxs-lookup"><span data-stu-id="595b5-121">The Dependent reference represents the session using the resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="595b5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="595b5-122">Requirements</span></span>



| <span data-ttu-id="595b5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="595b5-123">Requirement</span></span> | <span data-ttu-id="595b5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="595b5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="595b5-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="595b5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="595b5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="595b5-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="595b5-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="595b5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="595b5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="595b5-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="595b5-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="595b5-129">Namespace</span></span><br/>                | <span data-ttu-id="595b5-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="595b5-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="595b5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="595b5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="595b5-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="595b5-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="595b5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="595b5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="595b5-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="595b5-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="595b5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="595b5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="595b5-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="595b5-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
