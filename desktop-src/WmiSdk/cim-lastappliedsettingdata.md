---
description: Uma associação entre um objeto e outro objeto que foi aplicado a ele.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: Classe CIM_LastAppliedSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793641"
---
# <a name="cim_lastappliedsettingdata-class"></a><span data-ttu-id="fb6a5-103">\_Classe CIM LastAppliedSettingData</span><span class="sxs-lookup"><span data-stu-id="fb6a5-103">CIM\_LastAppliedSettingData class</span></span>

<span data-ttu-id="fb6a5-104">Uma associação entre um objeto e outro objeto que foi aplicado a ele.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-104">An association between an object and another object which has been applied to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb6a5-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fb6a5-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fb6a5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fb6a5-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6a5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb6a5-108">Syntax</span></span>

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a><span data-ttu-id="fb6a5-109">Membros</span><span class="sxs-lookup"><span data-stu-id="fb6a5-109">Members</span></span>

<span data-ttu-id="fb6a5-110">A classe **CIM \_ LastAppliedSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fb6a5-110">The **CIM\_LastAppliedSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fb6a5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fb6a5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb6a5-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fb6a5-112">Properties</span></span>

<span data-ttu-id="fb6a5-113">A classe **CIM \_ LastAppliedSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-113">The **CIM\_LastAppliedSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb6a5-114">**Aplicadoobject**</span><span class="sxs-lookup"><span data-stu-id="fb6a5-114">**AppliedObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb6a5-115">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="fb6a5-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="fb6a5-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fb6a5-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb6a5-117">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="fb6a5-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fb6a5-118">O objeto que foi aplicado ao objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-118">The object that was applied to the target object.</span></span>

</dd> <dt>

<span data-ttu-id="fb6a5-119">**Target (destino)**</span><span class="sxs-lookup"><span data-stu-id="fb6a5-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb6a5-120">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="fb6a5-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="fb6a5-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fb6a5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb6a5-122">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="fb6a5-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fb6a5-123">O objeto que era o destino do aplicativo do objeto.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-123">The object that was the target of the object's application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb6a5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb6a5-124">Requirements</span></span>



| <span data-ttu-id="fb6a5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb6a5-125">Requirement</span></span> | <span data-ttu-id="fb6a5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fb6a5-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="fb6a5-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb6a5-127">Namespace</span></span><br/> | <span data-ttu-id="fb6a5-128">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fb6a5-128">Root\\CIMV2</span></span><br/> |



 

 




