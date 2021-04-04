---
description: Define um tipo de mídia e PHY 802,11.
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: Enumeração de DOT11_PHY_TYPE (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_PHY_TYPE
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 4e8fc4a1154b9f95fad5024607435861b9e98ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828848"
---
# <a name="dot11_phy_type-enumeration"></a><span data-ttu-id="afa96-103">\_Enumeração de \_ tipo DOT11 PHY</span><span class="sxs-lookup"><span data-stu-id="afa96-103">DOT11\_PHY\_TYPE enumeration</span></span>

<span data-ttu-id="afa96-104">A enumeração de **\_ \_ tipo DOT11 PHY** define um tipo de mídia e PHY 802,11.</span><span class="sxs-lookup"><span data-stu-id="afa96-104">The **DOT11\_PHY\_TYPE** enumeration defines an 802.11 PHY and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="afa96-105">Syntax</span></span>


```C++
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = 0,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="afa96-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="afa96-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="afa96-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11 \_ PHY \_ tipo \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="afa96-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11\_phy\_type\_unknown**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-108">Especifica um tipo PHY desconhecido ou não inicializado.</span><span class="sxs-lookup"><span data-stu-id="afa96-108">Specifies an unknown or uninitialized PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11 \_ PHY \_ tipo \_ any**</span><span class="sxs-lookup"><span data-stu-id="afa96-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11\_phy\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-110">Especifica qualquer tipo de PHY.</span><span class="sxs-lookup"><span data-stu-id="afa96-110">Specifies any PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11 \_ PHY \_ Type \_ FHSS**</span><span class="sxs-lookup"><span data-stu-id="afa96-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11\_phy\_type\_fhss**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-112">Especifica um PHY (FHSS) de espectro de dispersão de frequência.</span><span class="sxs-lookup"><span data-stu-id="afa96-112">Specifies a frequency-hopping spread-spectrum (FHSS) PHY.</span></span> <span data-ttu-id="afa96-113">Os dispositivos Bluetooth podem usar FHSS ou uma adaptação de FHSS.</span><span class="sxs-lookup"><span data-stu-id="afa96-113">Bluetooth devices can use FHSS or an adaptation of FHSS.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11 \_ PHY \_ tipo \_ DSSS**</span><span class="sxs-lookup"><span data-stu-id="afa96-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11\_phy\_type\_dsss**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-115">Especifica um tipo PHY de espectro de espalhamento de sequência direta (DSSS).</span><span class="sxs-lookup"><span data-stu-id="afa96-115">Specifies a direct sequence spread spectrum (DSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11 \_ PHY \_ Type \_ irbaseband**</span><span class="sxs-lookup"><span data-stu-id="afa96-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11\_phy\_type\_irbaseband**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-117">Especifica um tipo de PHY de banda de infravermelho (IR).</span><span class="sxs-lookup"><span data-stu-id="afa96-117">Specifies an infrared (IR) baseband PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11 \_ PHY \_ Type \_ OFDM**</span><span class="sxs-lookup"><span data-stu-id="afa96-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11\_phy\_type\_ofdm**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-119">Especifica um tipo PHY de OFDM (multiplexação de divisão de frequência ortogonal).</span><span class="sxs-lookup"><span data-stu-id="afa96-119">Specifies an orthogonal frequency division multiplexing (OFDM) PHY type.</span></span> <span data-ttu-id="afa96-120">dispositivos 802.11 a podem usar o OFDM.</span><span class="sxs-lookup"><span data-stu-id="afa96-120">802.11a devices can use OFDM.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11 \_ PHY \_ Type \_ hrdsss**</span><span class="sxs-lookup"><span data-stu-id="afa96-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11\_phy\_type\_hrdsss**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-122">Especifica um tipo PHY de HRDSSS (DSSS de alta taxa).</span><span class="sxs-lookup"><span data-stu-id="afa96-122">Specifies a high-rate DSSS (HRDSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11 \_ PHY \_ tipo \_ ERP**</span><span class="sxs-lookup"><span data-stu-id="afa96-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11\_phy\_type\_erp**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-124">Especifica um tipo PHY de taxa estendida (ERP).</span><span class="sxs-lookup"><span data-stu-id="afa96-124">Specifies an extended rate PHY type (ERP).</span></span> <span data-ttu-id="afa96-125">dispositivos 802.11 g podem usar ERP.</span><span class="sxs-lookup"><span data-stu-id="afa96-125">802.11g devices can use ERP.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11 \_ PHY \_ tipo \_ HT**</span><span class="sxs-lookup"><span data-stu-id="afa96-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11\_phy\_type\_ht**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-127">Especifica o tipo PHY 802.11 n.</span><span class="sxs-lookup"><span data-stu-id="afa96-127">Specifies the 802.11n PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11 \_ PHY \_ Type \_ vht**</span><span class="sxs-lookup"><span data-stu-id="afa96-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11\_phy\_type\_vht**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-129">Especifica o tipo PHY de AC 802.11.</span><span class="sxs-lookup"><span data-stu-id="afa96-129">Specifies the 802.11ac PHY type.</span></span> <span data-ttu-id="afa96-130">Este é o tipo PHY de taxa de transferência muito alta especificado em IEEE 802.11 AC.</span><span class="sxs-lookup"><span data-stu-id="afa96-130">This is the very high throughput PHY type specified in IEEE 802.11ac.</span></span>

<span data-ttu-id="afa96-131">Esse valor tem suporte em Windows 8.1, Windows Server 2012 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="afa96-131">This value is supported on Windows 8.1, Windows Server 2012 R2, and later.</span></span>

</dd> <dt>

<span data-ttu-id="afa96-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11 \_ PHY \_ tipo \_ de \_ início de IHV**</span><span class="sxs-lookup"><span data-stu-id="afa96-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11\_phy\_type\_IHV\_start**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-133">Especifica o início do intervalo que é usado para definir os tipos de PHY que são desenvolvidos por um fornecedor de hardware independente (IHV).</span><span class="sxs-lookup"><span data-stu-id="afa96-133">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="afa96-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11 \_ PHY \_ tipo \_ de \_ fim de IHV**</span><span class="sxs-lookup"><span data-stu-id="afa96-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11\_phy\_type\_IHV\_end**</span></span>
</dt> <dd>

<span data-ttu-id="afa96-135">Especifica o início do intervalo que é usado para definir os tipos de PHY que são desenvolvidos por um fornecedor de hardware independente (IHV).</span><span class="sxs-lookup"><span data-stu-id="afa96-135">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afa96-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="afa96-136">Remarks</span></span>

<span data-ttu-id="afa96-137">Um IHV pode atribuir um valor para seus tipos de PHY proprietários de **dot11 \_ PHY \_ tipo \_ IHV \_ início** por meio de **dot11 \_ PHY \_ tipo \_ IHV \_ end**.</span><span class="sxs-lookup"><span data-stu-id="afa96-137">An IHV can assign a value for its proprietary PHY types from **dot11\_phy\_type\_IHV\_start** through **dot11\_phy\_type\_IHV\_end**.</span></span> <span data-ttu-id="afa96-138">O IHV deve atribuir um número exclusivo a partir desse intervalo para cada um de seus tipos de PHY proprietários.</span><span class="sxs-lookup"><span data-stu-id="afa96-138">The IHV must assign a unique number from this range for each of its proprietary PHY types.</span></span>

## <a name="requirements"></a><span data-ttu-id="afa96-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afa96-139">Requirements</span></span>



| <span data-ttu-id="afa96-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="afa96-140">Requirement</span></span> | <span data-ttu-id="afa96-141">Valor</span><span class="sxs-lookup"><span data-stu-id="afa96-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afa96-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afa96-142">Minimum supported client</span></span><br/> | <span data-ttu-id="afa96-143">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="afa96-143">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="afa96-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afa96-144">Minimum supported server</span></span><br/> | <span data-ttu-id="afa96-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="afa96-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afa96-146">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="afa96-146">Redistributable</span></span><br/>          | <span data-ttu-id="afa96-147">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="afa96-147">Wireless LAN API for Windows XP with SP2</span></span><br/>                                   |
| <span data-ttu-id="afa96-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="afa96-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="afa96-149"><dt>Windot11. h</dt></span><span class="sxs-lookup"><span data-stu-id="afa96-149"><dt>Windot11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afa96-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="afa96-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa96-151">**\_atributos de associação de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="afa96-151">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="afa96-152">**\_funcionalidade da interface WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="afa96-152">**WLAN\_INTERFACE\_CAPABILITY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




