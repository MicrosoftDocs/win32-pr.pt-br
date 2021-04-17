---
description: Uma associação entre um sistema virtual e os dados de configuração do instantâneo, que é o pai do sistema virtual.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: Classe CIM_PreviousSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782670"
---
# <a name="cim_previoussettingdata-class"></a><span data-ttu-id="d1b12-103">\_Classe CIM PreviousSettingData</span><span class="sxs-lookup"><span data-stu-id="d1b12-103">CIM\_PreviousSettingData class</span></span>

<span data-ttu-id="d1b12-104">Uma associação entre um sistema virtual e os dados de configuração do instantâneo, que é o pai do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="d1b12-104">An association between a virtual system and the setting data of the snapshot which is the parent to the virtual system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1b12-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d1b12-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d1b12-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d1b12-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d1b12-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d1b12-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b12-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1b12-108">Syntax</span></span>

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a><span data-ttu-id="d1b12-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d1b12-109">Members</span></span>

<span data-ttu-id="d1b12-110">A classe **CIM \_ PreviousSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d1b12-110">The **CIM\_PreviousSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d1b12-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1b12-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1b12-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1b12-112">Properties</span></span>

<span data-ttu-id="d1b12-113">A classe **CIM \_ PreviousSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1b12-113">The **CIM\_PreviousSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1b12-114">**Anteriorobject**</span><span class="sxs-lookup"><span data-stu-id="d1b12-114">**PreviousObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b12-115">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="d1b12-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d1b12-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1b12-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1b12-117">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d1b12-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d1b12-118">Os dados de configuração de instantâneo que são o pai deste sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="d1b12-118">The snapshot setting data that is the parent of this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="d1b12-119">**Target (destino)**</span><span class="sxs-lookup"><span data-stu-id="d1b12-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b12-120">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="d1b12-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d1b12-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1b12-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1b12-122">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d1b12-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d1b12-123">O sistema de computador que foi o destino do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d1b12-123">The computer system that was the target of the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1b12-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1b12-124">Requirements</span></span>



| <span data-ttu-id="d1b12-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b12-125">Requirement</span></span> | <span data-ttu-id="d1b12-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b12-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="d1b12-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1b12-127">Namespace</span></span><br/> | <span data-ttu-id="d1b12-128">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d1b12-128">Root\\CIMV2</span></span><br/> |



 

 




