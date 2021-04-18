---
description: Representa um monitor de área de trabalho CRT.
ms.assetid: 26a06320-9fd9-434e-87c8-486e9ca4945c
title: Classe CIM_DesktopMonitor (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab152fc10f3fd404744c293d2368039ffcfdb291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756935"
---
# <a name="cim_desktopmonitor-class-hyper-v-management"></a><span data-ttu-id="5b4db-103">Classe CIM_DesktopMonitor (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="5b4db-103">CIM_DesktopMonitor class (Hyper-V management)</span></span>

<span data-ttu-id="5b4db-104">Representa um monitor de área de trabalho CRT.</span><span class="sxs-lookup"><span data-stu-id="5b4db-104">Represents a CRT desktop monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b4db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b4db-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices")]
class CIM_DesktopMonitor : CIM_Display
{
  uint16 DisplayType;
  uint32 Bandwidth;
  uint32 ScreenHeight;
  uint32 ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="5b4db-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5b4db-106">Members</span></span>

<span data-ttu-id="5b4db-107">A classe **CIM \_ DesktopMonitor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5b4db-107">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="5b4db-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b4db-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b4db-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b4db-109">Properties</span></span>

<span data-ttu-id="5b4db-110">A classe **CIM \_ DesktopMonitor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b4db-110">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b4db-111">**Largura de banda**</span><span class="sxs-lookup"><span data-stu-id="5b4db-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4db-112">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b4db-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b4db-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b4db-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b4db-114">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz"), **PUnit** ("Hertz \* 10 ^ 6")</span><span class="sxs-lookup"><span data-stu-id="5b4db-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="5b4db-115">A largura de banda da exibição, em MHertz.</span><span class="sxs-lookup"><span data-stu-id="5b4db-115">The bandwidth of the display, in MHertz.</span></span> <span data-ttu-id="5b4db-116">"0" indica desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5b4db-116">"0" indicates unknown.</span></span>

</dd> <dt>

<span data-ttu-id="5b4db-117">**TipoDeExibição**</span><span class="sxs-lookup"><span data-stu-id="5b4db-117">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4db-118">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b4db-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b4db-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b4db-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b4db-120">O tipo de tipo de exibição do monitor CRT.</span><span class="sxs-lookup"><span data-stu-id="5b4db-120">The type of display type of the CRT monitor.</span></span> <span data-ttu-id="5b4db-121">Por exemplo, cor de multiexame ou monocromático.</span><span class="sxs-lookup"><span data-stu-id="5b4db-121">For example, multiscan color, or monochrome.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5b4db-122">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5b4db-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5b4db-123">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5b4db-123">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="5b4db-124">**Cor de MultiScan** (2)</span><span class="sxs-lookup"><span data-stu-id="5b4db-124">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="5b4db-125">**Multiexame monocromático** (3)</span><span class="sxs-lookup"><span data-stu-id="5b4db-125">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="5b4db-126">**Cor de frequência fixa** (4)</span><span class="sxs-lookup"><span data-stu-id="5b4db-126">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="5b4db-127">**Frequência fixa monocromático** (5)</span><span class="sxs-lookup"><span data-stu-id="5b4db-127">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b4db-128">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="5b4db-128">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4db-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b4db-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b4db-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b4db-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b4db-131">A altura lógica da exibição, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="5b4db-131">The logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="5b4db-132">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="5b4db-132">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4db-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b4db-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b4db-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b4db-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b4db-135">A largura lógica da exibição, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="5b4db-135">The logical width of the display, in screen coordinates.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b4db-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b4db-136">Requirements</span></span>



| <span data-ttu-id="5b4db-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b4db-137">Requirement</span></span> | <span data-ttu-id="5b4db-138">Valor</span><span class="sxs-lookup"><span data-stu-id="5b4db-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4db-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b4db-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5b4db-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5b4db-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5b4db-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b4db-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5b4db-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5b4db-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5b4db-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b4db-143">Namespace</span></span><br/>                | <span data-ttu-id="5b4db-144">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5b4db-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5b4db-145">MOF</span><span class="sxs-lookup"><span data-stu-id="5b4db-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b4db-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b4db-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b4db-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5b4db-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b4db-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b4db-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b4db-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b4db-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b4db-150">**Exibição de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5b4db-150">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

