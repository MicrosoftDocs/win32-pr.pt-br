---
description: Descreve um perfil que é referenciado por outro perfil registrado.
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Classe Msvm_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbe95658556be8a15bed0e7e5b5b32dda23ff21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787104"
---
# <a name="msvm_referencedprofile-class"></a><span data-ttu-id="a541e-103">\_Classe Msvm ReferencedProfile</span><span class="sxs-lookup"><span data-stu-id="a541e-103">Msvm\_ReferencedProfile class</span></span>

<span data-ttu-id="a541e-104">Descreve um perfil que é referenciado por outro perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="a541e-104">Describes a profile that is referenced by another registered profile.</span></span>

<span data-ttu-id="a541e-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a541e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a541e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a541e-106">Syntax</span></span>

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a541e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a541e-107">Members</span></span>

<span data-ttu-id="a541e-108">A classe **Msvm \_ ReferencedProfile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a541e-108">The **Msvm\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="a541e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a541e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a541e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a541e-110">Properties</span></span>

<span data-ttu-id="a541e-111">A classe **Msvm \_ ReferencedProfile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a541e-111">The **Msvm\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a541e-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="a541e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541e-113">Tipo de dados: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a541e-113">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="a541e-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a541e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a541e-115">O perfil registrado que é referenciado pelo perfil **dependente** .</span><span class="sxs-lookup"><span data-stu-id="a541e-115">The registered profile that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="a541e-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="a541e-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541e-117">Tipo de dados: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a541e-117">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="a541e-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a541e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a541e-119">Um perfil registrado que faz referência a outros perfis.</span><span class="sxs-lookup"><span data-stu-id="a541e-119">A registered profile that references other profiles.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a541e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a541e-120">Requirements</span></span>



| <span data-ttu-id="a541e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a541e-121">Requirement</span></span> | <span data-ttu-id="a541e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a541e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a541e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a541e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a541e-124">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a541e-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a541e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a541e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a541e-126">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="a541e-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a541e-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a541e-127">Namespace</span></span><br/>                | <span data-ttu-id="a541e-128">\\Interoperabilidade raiz</span><span class="sxs-lookup"><span data-stu-id="a541e-128">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="a541e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="a541e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a541e-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a541e-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a541e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a541e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a541e-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a541e-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

