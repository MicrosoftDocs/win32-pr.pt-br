---
description: Associa uma cabeça de vídeo com o controlador de vídeo que a inclui.
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Classe Msvm_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11065c7b7a9e23b786697c3d4f0dbd63e67d6b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091556"
---
# <a name="msvm_videoheadoncontroller-class"></a><span data-ttu-id="61b7d-103">\_Classe Msvm VideoHeadOnController</span><span class="sxs-lookup"><span data-stu-id="61b7d-103">Msvm\_VideoHeadOnController class</span></span>

<span data-ttu-id="61b7d-104">Associa uma cabeça de vídeo com o controlador de vídeo que a inclui.</span><span class="sxs-lookup"><span data-stu-id="61b7d-104">Associates a video head with the video controller that includes it.</span></span>

<span data-ttu-id="61b7d-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="61b7d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b7d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61b7d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="61b7d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="61b7d-107">Members</span></span>

<span data-ttu-id="61b7d-108">A classe **Msvm \_ VideoHeadOnController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="61b7d-108">The **Msvm\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="61b7d-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61b7d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61b7d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61b7d-110">Properties</span></span>

<span data-ttu-id="61b7d-111">A classe **Msvm \_ VideoHeadOnController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="61b7d-111">The **Msvm\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61b7d-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="61b7d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61b7d-113">Tipo de dados: **[ **CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="61b7d-113">Data type: **[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="61b7d-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61b7d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61b7d-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="61b7d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="61b7d-116">O controlador de vídeo que inclui o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="61b7d-116">The video controller that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="61b7d-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="61b7d-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61b7d-118">Tipo de dados: **[ **Msvm \_ VideoHead**](msvm-videohead.md)**</span><span class="sxs-lookup"><span data-stu-id="61b7d-118">Data type: **[**Msvm\_VideoHead**](msvm-videohead.md)**</span></span>
</dt> <dt>

<span data-ttu-id="61b7d-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61b7d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61b7d-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="61b7d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="61b7d-121">O cabeçalho no dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="61b7d-121">The head on the video device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61b7d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="61b7d-122">Remarks</span></span>

<span data-ttu-id="61b7d-123">O acesso à classe **Msvm \_ VideoHeadOnController** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="61b7d-123">Access to the **Msvm\_VideoHeadOnController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="61b7d-124">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="61b7d-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="61b7d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b7d-125">Requirements</span></span>



| <span data-ttu-id="61b7d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b7d-126">Requirement</span></span> | <span data-ttu-id="61b7d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="61b7d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b7d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61b7d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="61b7d-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61b7d-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61b7d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61b7d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="61b7d-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61b7d-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61b7d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="61b7d-132">Namespace</span></span><br/>                | <span data-ttu-id="61b7d-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="61b7d-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61b7d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="61b7d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61b7d-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61b7d-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61b7d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="61b7d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61b7d-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61b7d-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61b7d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="61b7d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b7d-139">**\_VIDEOHEADONCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="61b7d-139">**CIM\_VideoHeadOnController**</span></span>](cim-videoheadoncontroller.md)
</dt> <dt>

<span data-ttu-id="61b7d-140">[**\_VIDEOHEADONCONTROLLER CIM**](/previous-versions//cc136950(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61b7d-140">[**CIM\_VideoHeadOnController**](/previous-versions//cc136950(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="61b7d-141">Classes de vídeo</span><span class="sxs-lookup"><span data-stu-id="61b7d-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

