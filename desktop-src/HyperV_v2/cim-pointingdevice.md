---
description: Representa um dispositivo usado para apontar para regiões de uma exibição.
ms.assetid: ffc675c3-29bd-4c54-8e54-8b6212daf66d
title: Classe CIM_PointingDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.Resolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57cca8c81a2d363e9e31bfc958a75b71e1b910d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091847"
---
# <a name="cim_pointingdevice-class-hyper-v-management"></a><span data-ttu-id="10646-103">Classe CIM_PointingDevice (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="10646-103">CIM_PointingDevice class (Hyper-V management)</span></span>

<span data-ttu-id="10646-104">Representa um dispositivo usado para apontar para regiões de uma exibição.</span><span class="sxs-lookup"><span data-stu-id="10646-104">Represents a device used to point to regions of a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="10646-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10646-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16 PointingType;
  uint8  NumberOfButtons;
  uint16 Handedness;
  uint32 Resolution;
};
```

## <a name="members"></a><span data-ttu-id="10646-106">Membros</span><span class="sxs-lookup"><span data-stu-id="10646-106">Members</span></span>

<span data-ttu-id="10646-107">A classe **CIM \_ PointingDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="10646-107">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="10646-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10646-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10646-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10646-109">Properties</span></span>

<span data-ttu-id="10646-110">A classe **CIM \_ PointingDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="10646-110">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10646-111">**Direção**</span><span class="sxs-lookup"><span data-stu-id="10646-111">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10646-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10646-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10646-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10646-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10646-114">Indica se o dispositivo apontador está configurado para a operação de mão direita ou esquerda.</span><span class="sxs-lookup"><span data-stu-id="10646-114">Indicates whether the pointing device is configured for right or left handed operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10646-115">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="10646-115">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="10646-116">**Não aplicável** (1)</span><span class="sxs-lookup"><span data-stu-id="10646-116">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="10646-117">**Operação da mão direita** (2)</span><span class="sxs-lookup"><span data-stu-id="10646-117">**Right Handed Operation** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="10646-118">**Operação da mão esquerda** (3)</span><span class="sxs-lookup"><span data-stu-id="10646-118">**Left Handed Operation** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10646-119">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="10646-119">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10646-120">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="10646-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="10646-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10646-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10646-122">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo apontador DMTF \| 3,4 ")</span><span class="sxs-lookup"><span data-stu-id="10646-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.4")</span></span>
</dt> </dl>

<span data-ttu-id="10646-123">O número de botões no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10646-123">The number of buttons on the device.</span></span> <span data-ttu-id="10646-124">Se o dispositivo apontador não tiver botões, esse valor deverá ser definido como "0".</span><span class="sxs-lookup"><span data-stu-id="10646-124">If the pointing device has no buttons, this value should be set to "0".</span></span>

</dd> <dt>

<span data-ttu-id="10646-125">**Ponto de apontar**</span><span class="sxs-lookup"><span data-stu-id="10646-125">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10646-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10646-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10646-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10646-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10646-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo apontador DMTF \| 3,1 ")</span><span class="sxs-lookup"><span data-stu-id="10646-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.1")</span></span>
</dt> </dl>

<span data-ttu-id="10646-129">O tipo do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="10646-129">The type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10646-130">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10646-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10646-131">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10646-131">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="10646-132">**Mouse** (3)</span><span class="sxs-lookup"><span data-stu-id="10646-132">**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="10646-133">**Rastrear bola** (4)</span><span class="sxs-lookup"><span data-stu-id="10646-133">**Track Ball** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="10646-134">**Ponto de controle** (5)</span><span class="sxs-lookup"><span data-stu-id="10646-134">**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="10646-135">**Ponto de deslizamento** (6)</span><span class="sxs-lookup"><span data-stu-id="10646-135">**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="10646-136">**Touch pad** (7)</span><span class="sxs-lookup"><span data-stu-id="10646-136">**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="10646-137">**Tela sensível ao toque** (8)</span><span class="sxs-lookup"><span data-stu-id="10646-137">**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="10646-138">**Sensor de mouse-óptico** (9)</span><span class="sxs-lookup"><span data-stu-id="10646-138">**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10646-139">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="10646-139">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10646-140">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10646-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10646-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10646-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10646-142">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagens por polegada"), **PUnit** ("contagem/polegada")</span><span class="sxs-lookup"><span data-stu-id="10646-142">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Counts per Inch"), **PUnit** ("count / inch")</span></span>
</dt> </dl>

<span data-ttu-id="10646-143">A resolução de rastreamento do dispositivo apontador, em contagens por polegada.</span><span class="sxs-lookup"><span data-stu-id="10646-143">The tracking resolution of the pointing device, in counts per inch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10646-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10646-144">Requirements</span></span>



| <span data-ttu-id="10646-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="10646-145">Requirement</span></span> | <span data-ttu-id="10646-146">Valor</span><span class="sxs-lookup"><span data-stu-id="10646-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10646-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10646-147">Minimum supported client</span></span><br/> | <span data-ttu-id="10646-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="10646-148">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="10646-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10646-149">Minimum supported server</span></span><br/> | <span data-ttu-id="10646-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10646-150">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="10646-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="10646-151">Namespace</span></span><br/>                | <span data-ttu-id="10646-152">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="10646-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="10646-153">MOF</span><span class="sxs-lookup"><span data-stu-id="10646-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10646-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10646-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10646-155">DLL</span><span class="sxs-lookup"><span data-stu-id="10646-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10646-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10646-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="10646-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="10646-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10646-158">**Userdevice do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="10646-158">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

