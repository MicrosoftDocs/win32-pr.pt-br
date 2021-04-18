---
description: Representa os recursos de exibição básicos de um monitor de computador.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: Classe WmiMonitorBasicDisplayParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760664"
---
# <a name="wmimonitorbasicdisplayparams-class"></a><span data-ttu-id="7e287-103">Classe WmiMonitorBasicDisplayParams</span><span class="sxs-lookup"><span data-stu-id="7e287-103">WmiMonitorBasicDisplayParams class</span></span>

<span data-ttu-id="7e287-104">A classe WMI **WmiMonitorBasicDisplayParams** representa os recursos de exibição básicos de um monitor de computador.</span><span class="sxs-lookup"><span data-stu-id="7e287-104">The **WmiMonitorBasicDisplayParams** WMI class represents the basic display features of a computer monitor.</span></span> <span data-ttu-id="7e287-105">O valor da propriedade **VideoInputType** indica se o monitor é analógico ou digital.</span><span class="sxs-lookup"><span data-stu-id="7e287-105">The value of the **VideoInputType** property indicates whether the monitor is analog or digital.</span></span> <span data-ttu-id="7e287-106">Os dados nessa classe correspondem aos dados no bloco de parâmetros/recursos de exibição básico de VESA (vídeo de associação padrão de tela de eletrônicos) avançado (E-EDID) padrão de dados de identificação de exibição estendida.</span><span class="sxs-lookup"><span data-stu-id="7e287-106">Data in this class corresponds to data in the Basic Display Parameters/Features block of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e287-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e287-107">Syntax</span></span>

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a><span data-ttu-id="7e287-108">Membros</span><span class="sxs-lookup"><span data-stu-id="7e287-108">Members</span></span>

<span data-ttu-id="7e287-109">A classe **WmiMonitorBasicDisplayParams** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7e287-109">The **WmiMonitorBasicDisplayParams** class has these types of members:</span></span>

-   [<span data-ttu-id="7e287-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7e287-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e287-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7e287-111">Properties</span></span>

<span data-ttu-id="7e287-112">A classe **WmiMonitorBasicDisplayParams** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7e287-112">The **WmiMonitorBasicDisplayParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e287-113">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="7e287-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e287-114">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7e287-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7e287-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e287-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e287-116">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="7e287-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7e287-117">**DisplayTransferCharacteristic**</span><span class="sxs-lookup"><span data-stu-id="7e287-117">**DisplayTransferCharacteristic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e287-118">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="7e287-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7e287-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e287-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e287-120">Característica de transferência de exibição (100 \* gama-100).</span><span class="sxs-lookup"><span data-stu-id="7e287-120">Display transfer characteristic (100\*Gamma-100).</span></span>

</dd> <dt>

<span data-ttu-id="7e287-121">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="7e287-121">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e287-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e287-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e287-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e287-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e287-124">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="7e287-124">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7e287-125">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="7e287-125">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="7e287-126">**MaxHorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="7e287-126">**MaxHorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e287-127">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="7e287-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7e287-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e287-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e287-129">Tamanho máximo da imagem horizontal em centímetros.</span><span class="sxs-lookup"><span data-stu-id="7e287-129">Maximum horizontal image size in centimeters.</span></span> <span data-ttu-id="7e287-130">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="7e287-130">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7e287-131">**MaxVerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="7e287-131">**MaxVerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e287-132">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="7e287-132">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7e287-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e287-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e287-134">Tamanho máximo da imagem vertical em centímetros.</span><span class="sxs-lookup"><span data-stu-id="7e287-134">Maximum vertical image size in centimeters.</span></span> <span data-ttu-id="7e287-135">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="7e287-135">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7e287-136">**SupportedDisplayFeatures**</span><span class="sxs-lookup"><span data-stu-id="7e287-136">**SupportedDisplayFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e287-137">Tipo de dados: **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span><span class="sxs-lookup"><span data-stu-id="7e287-137">Data type: **[**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7e287-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e287-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e287-139">Exibir recursos com suporte no monitor.</span><span class="sxs-lookup"><span data-stu-id="7e287-139">Display features supported by the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7e287-140">**VideoInputType**</span><span class="sxs-lookup"><span data-stu-id="7e287-140">**VideoInputType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e287-141">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="7e287-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7e287-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e287-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e287-143">Tipo de entrada de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7e287-143">Video input type.</span></span>



| <span data-ttu-id="7e287-144">Valor</span><span class="sxs-lookup"><span data-stu-id="7e287-144">Value</span></span>                                                                              | <span data-ttu-id="7e287-145">Significado</span><span class="sxs-lookup"><span data-stu-id="7e287-145">Meaning</span></span>            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="7e287-146"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7e287-146"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="7e287-147">Analog</span><span class="sxs-lookup"><span data-stu-id="7e287-147">Analog</span></span><br/>  |
| <dl> <span data-ttu-id="7e287-148"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="7e287-148"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="7e287-149">Digital</span><span class="sxs-lookup"><span data-stu-id="7e287-149">Digital</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e287-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e287-150">Remarks</span></span>

<span data-ttu-id="7e287-151">**MaxHorizontalImageSize** e **MaxVerticalImageSize** representam as dimensões de imagem máxima que o monitor pode exibir corretamente para todo o conjunto de combinações de tempo e formato com suporte.</span><span class="sxs-lookup"><span data-stu-id="7e287-151">**MaxHorizontalImageSize** and **MaxVerticalImageSize** represent the maximum image dimensions that the monitor can correctly display for the entire set of supported timing and format combinations.</span></span> <span data-ttu-id="7e287-152">A dimensão de imagem máxima é definida pelo padrão da VIAD (linguagem de imagem de vídeo) VESA e é arredondada para o centímetro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="7e287-152">The maximum image dimension is defined by VESA Video Image Area Definition (VIAD) Standard and is rounded to the nearest centimeter.</span></span> <span data-ttu-id="7e287-153">O sistema de computador host pode usar esses dados para selecionar o tamanho da imagem e a taxa de proporção que permitirá o texto corretamente dimensionado.</span><span class="sxs-lookup"><span data-stu-id="7e287-153">The host computer system can use this data to select the image size and aspect ratio that will allow properly scaled text.</span></span> <span data-ttu-id="7e287-154">Lembre-se de que, se um ou ambos os campos forem zero, o sistema não fará suposições sobre o tamanho de exibição.</span><span class="sxs-lookup"><span data-stu-id="7e287-154">Be aware that, if either or both of these fields are zero, then the system makes no assumptions about the display size.</span></span> <span data-ttu-id="7e287-155">Por exemplo, o tamanho de uma exibição de projeção pode não ser determinado.</span><span class="sxs-lookup"><span data-stu-id="7e287-155">For example, the size of a projection display may be undetermined.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e287-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e287-156">Requirements</span></span>



| <span data-ttu-id="7e287-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e287-157">Requirement</span></span> | <span data-ttu-id="7e287-158">Valor</span><span class="sxs-lookup"><span data-stu-id="7e287-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e287-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e287-159">Minimum supported client</span></span><br/> | <span data-ttu-id="7e287-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e287-160">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7e287-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e287-161">Minimum supported server</span></span><br/> | <span data-ttu-id="7e287-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e287-162">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7e287-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e287-163">Namespace</span></span><br/>                | <span data-ttu-id="7e287-164">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="7e287-164">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7e287-165">MOF</span><span class="sxs-lookup"><span data-stu-id="7e287-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e287-166"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e287-166"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e287-167">DLL</span><span class="sxs-lookup"><span data-stu-id="7e287-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e287-168"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e287-168"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e287-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e287-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e287-170">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="7e287-170">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




