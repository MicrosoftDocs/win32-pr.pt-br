---
description: Associa um cabeçalho de vídeo ao adaptador de vídeo que o contém.
ms.assetid: d15f4350-1529-4246-9ea2-8453e52516c6
title: Classe CIM_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHeadOnController
- CIM_VideoHeadOnController.Antecedent
- CIM_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18178e6d9d7f1e684af1d4fe74336e1f2a02eedc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787524"
---
# <a name="cim_videoheadoncontroller-class"></a><span data-ttu-id="bf636-103">\_Classe CIM VideoHeadOnController</span><span class="sxs-lookup"><span data-stu-id="bf636-103">CIM\_VideoHeadOnController class</span></span>

<span data-ttu-id="bf636-104">Associa um cabeçalho de vídeo ao adaptador de vídeo que o contém.</span><span class="sxs-lookup"><span data-stu-id="bf636-104">Associates a video head with the video adapter that contains it.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf636-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf636-105">Syntax</span></span>

``` syntax
[Association, Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHeadOnController : CIM_HostedDependency
{
  CIM_DisplayController REF Antecedent;
  CIM_VideoHead         REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bf636-106">Membros</span><span class="sxs-lookup"><span data-stu-id="bf636-106">Members</span></span>

<span data-ttu-id="bf636-107">A classe **CIM \_ VideoHeadOnController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bf636-107">The **CIM\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="bf636-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf636-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf636-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf636-109">Properties</span></span>

<span data-ttu-id="bf636-110">A classe **CIM \_ VideoHeadOnController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bf636-110">The **CIM\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf636-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="bf636-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf636-112">Tipo de dados: **CIM \_ DisplayController**</span><span class="sxs-lookup"><span data-stu-id="bf636-112">Data type: **CIM\_DisplayController**</span></span>
</dt> <dt>

<span data-ttu-id="bf636-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf636-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf636-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="bf636-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="bf636-115">O adaptador de vídeo que inclui o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="bf636-115">The video adapter that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="bf636-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="bf636-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf636-117">Tipo de dados: **CIM \_ VideoHead**</span><span class="sxs-lookup"><span data-stu-id="bf636-117">Data type: **CIM\_VideoHead**</span></span>
</dt> <dt>

<span data-ttu-id="bf636-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf636-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf636-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="bf636-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="bf636-120">O cabeçalho no adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf636-120">The head on the video adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf636-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf636-121">Requirements</span></span>



| <span data-ttu-id="bf636-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf636-122">Requirement</span></span> | <span data-ttu-id="bf636-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bf636-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf636-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf636-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bf636-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bf636-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bf636-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf636-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bf636-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf636-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bf636-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf636-128">Namespace</span></span><br/>                | <span data-ttu-id="bf636-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bf636-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bf636-130">MOF</span><span class="sxs-lookup"><span data-stu-id="bf636-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf636-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf636-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf636-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bf636-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf636-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf636-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf636-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf636-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf636-135">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="bf636-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

