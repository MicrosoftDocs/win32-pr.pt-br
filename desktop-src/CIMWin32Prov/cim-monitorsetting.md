---
description: A \_ classe CIM MonitorSetting associa a resolução do monitor ao monitor de área de trabalho ao qual se aplica.
ms.assetid: 4bf0b2d5-b901-4294-a33b-9c8a87785af0
ms.tgt_platform: multiple
title: Classe CIM_MonitorSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorSetting
- CIM_MonitorSetting.Setting
- CIM_MonitorSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc947f4bb484ec5392204747e583fbf80bbf88cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826492"
---
# <a name="cim_monitorsetting-class"></a><span data-ttu-id="6affa-103">\_Classe CIM MonitorSetting</span><span class="sxs-lookup"><span data-stu-id="6affa-103">CIM\_MonitorSetting class</span></span>

<span data-ttu-id="6affa-104">A classe **CIM \_ MonitorSetting** associa a resolução do monitor ao monitor de área de trabalho ao qual se aplica.</span><span class="sxs-lookup"><span data-stu-id="6affa-104">The **CIM\_MonitorSetting** class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6affa-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6affa-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6affa-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6affa-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6affa-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6affa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6affa-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6affa-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6affa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6affa-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCED-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorSetting : CIM_ElementSetting
{
  CIM_MonitorResolution REF Setting;
  CIM_DesktopMonitor    REF Element;
};
```

## <a name="members"></a><span data-ttu-id="6affa-110">Membros</span><span class="sxs-lookup"><span data-stu-id="6affa-110">Members</span></span>

<span data-ttu-id="6affa-111">A classe **CIM \_ MonitorSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6affa-111">The **CIM\_MonitorSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="6affa-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6affa-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6affa-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6affa-113">Properties</span></span>

<span data-ttu-id="6affa-114">A classe **CIM \_ MonitorSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6affa-114">The **CIM\_MonitorSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6affa-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="6affa-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6affa-116">Tipo de dados: **CIM \_ DesktopMonitor**</span><span class="sxs-lookup"><span data-stu-id="6affa-116">Data type: **CIM\_DesktopMonitor**</span></span>
</dt> <dt>

<span data-ttu-id="6affa-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6affa-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6affa-118">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("elemento")</span><span class="sxs-lookup"><span data-stu-id="6affa-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="6affa-119">Um [**\_ DesktopMonitor CIM**](cim-desktopmonitor.md) que descreve o monitor da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6affa-119">A [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) describing the desktop monitor.</span></span>

</dd> <dt>

<span data-ttu-id="6affa-120">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="6affa-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6affa-121">Tipo de dados: **CIM \_ MonitorResolution**</span><span class="sxs-lookup"><span data-stu-id="6affa-121">Data type: **CIM\_MonitorResolution**</span></span>
</dt> <dt>

<span data-ttu-id="6affa-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6affa-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6affa-123">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuração")</span><span class="sxs-lookup"><span data-stu-id="6affa-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="6affa-124">Um [**\_ MonitorResolution CIM**](cim-monitorresolution.md) que descreve a resolução de monitor associada ao monitor de desktop.</span><span class="sxs-lookup"><span data-stu-id="6affa-124">A [**CIM\_MonitorResolution**](cim-monitorresolution.md) describing the monitor resolution associated with the desktop monitor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6affa-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6affa-125">Remarks</span></span>

<span data-ttu-id="6affa-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="6affa-126">WMI does not implement this class.</span></span>

<span data-ttu-id="6affa-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6affa-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6affa-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6affa-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6affa-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6affa-129">Requirements</span></span>



| <span data-ttu-id="6affa-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6affa-130">Requirement</span></span> | <span data-ttu-id="6affa-131">Valor</span><span class="sxs-lookup"><span data-stu-id="6affa-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6affa-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6affa-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6affa-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6affa-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6affa-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6affa-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6affa-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6affa-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6affa-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="6affa-136">Namespace</span></span><br/>                | <span data-ttu-id="6affa-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6affa-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6affa-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6affa-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6affa-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6affa-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6affa-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6affa-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6affa-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6affa-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6affa-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="6affa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6affa-143">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="6affa-143">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

