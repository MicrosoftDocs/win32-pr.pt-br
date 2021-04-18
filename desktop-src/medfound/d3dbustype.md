---
description: Especifica o tipo de barramento de e/s usado pelo adaptador gráfico.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Enumeração D3DBUSTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791590"
---
# <a name="d3dbustype-enumeration"></a><span data-ttu-id="7526f-103">Enumeração D3DBUSTYPE</span><span class="sxs-lookup"><span data-stu-id="7526f-103">D3DBUSTYPE enumeration</span></span>

<span data-ttu-id="7526f-104">Especifica o tipo de barramento de e/s usado pelo adaptador gráfico.</span><span class="sxs-lookup"><span data-stu-id="7526f-104">Specifies the type of I/O bus used by the graphics adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7526f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7526f-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a><span data-ttu-id="7526f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7526f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7526f-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ outros**</span><span class="sxs-lookup"><span data-stu-id="7526f-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE\_OTHER**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-108">Indica um tipo de barramento diferente dos tipos listados aqui.</span><span class="sxs-lookup"><span data-stu-id="7526f-108">Indicates a type of bus other than the types listed here.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**\_PCI D3DBUSTYPE**</span><span class="sxs-lookup"><span data-stu-id="7526f-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE\_PCI**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-110">Barramento PCI.</span><span class="sxs-lookup"><span data-stu-id="7526f-110">PCI bus.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIX**</span><span class="sxs-lookup"><span data-stu-id="7526f-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE\_PCIX**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-112">Barramento PCI-X.</span><span class="sxs-lookup"><span data-stu-id="7526f-112">PCI-X bus.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**</span><span class="sxs-lookup"><span data-stu-id="7526f-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE\_PCIEXPRESS**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-114">Barramento PCI Express.</span><span class="sxs-lookup"><span data-stu-id="7526f-114">PCI Express bus.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**</span><span class="sxs-lookup"><span data-stu-id="7526f-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE\_AGP**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-116">Barramento AGP (Accelerated Graphics Port).</span><span class="sxs-lookup"><span data-stu-id="7526f-116">Accelerated Graphics Port (AGP) bus.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_Modificador D3DBUSIMPL \_ dentro \_ do \_ chipset**</span><span class="sxs-lookup"><span data-stu-id="7526f-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL\_MODIFIER\_INSIDE\_OF\_CHIPSET**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-118">A implementação do adaptador gráfico está em uma ponte norte do chipset da motherboard.</span><span class="sxs-lookup"><span data-stu-id="7526f-118">The implementation for the graphics adapter is in a motherboard chipset's north bridge.</span></span> <span data-ttu-id="7526f-119">Esse sinalizador implica que os dados nunca passam por um barramento de expansão (como PCI ou AGP) quando são transferidos da memória principal para o adaptador gráfico.</span><span class="sxs-lookup"><span data-stu-id="7526f-119">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL o \_ modificador \_ \_ de tela na placa- \_ mãe para o \_ \_ \_ chip**</span><span class="sxs-lookup"><span data-stu-id="7526f-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_CHIP**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-121">Indica que o adaptador gráfico está conectado à ponte norte de um chipset da motherboard controlando a placa-mãe e todos os chips do adaptador gráfico estão soldados na placa-mãe.</span><span class="sxs-lookup"><span data-stu-id="7526f-121">Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard and all of the graphics adapter's chips are soldered to the motherboard.</span></span> <span data-ttu-id="7526f-122">Esse sinalizador implica que os dados nunca passam por um barramento de expansão (como PCI ou AGP) quando são transferidos da memória principal para o adaptador gráfico.</span><span class="sxs-lookup"><span data-stu-id="7526f-122">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL o \_ modificador \_ controla \_ na \_ placa-mãe para o \_ \_ \_ soquete**</span><span class="sxs-lookup"><span data-stu-id="7526f-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_SOCKET**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-124">O adaptador gráfico é conectado à ponte norte do chipset da motherboard por meio de faixas na placa-mãe, e todos os chips do adaptador gráfico são conectados por meio de soquetes à placa-mãe.</span><span class="sxs-lookup"><span data-stu-id="7526f-124">The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_Conector da \_ \_ placa filha do modificador D3DBUSIMPL \_**</span><span class="sxs-lookup"><span data-stu-id="7526f-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-126">O adaptador gráfico é conectado à placa-mãe por meio de um conector do daughterboard.</span><span class="sxs-lookup"><span data-stu-id="7526f-126">The graphics adapter is connected to the motherboard through a daughterboard connector.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ \_ Conector da placa filha do modificador D3DBUSIMPL \_ \_ dentro \_ de \_ NUAE**</span><span class="sxs-lookup"><span data-stu-id="7526f-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR\_INSIDE\_OF\_NUAE**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-128">O adaptador gráfico é conectado à placa-mãe por meio de um conector do daughterboard e o adaptador gráfico está dentro de um compartimento que não é acessível pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7526f-128">The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.</span></span>

</dd> <dt>

<span data-ttu-id="7526f-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Modificador de D3DBUSIMPL \_ não \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="7526f-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL\_MODIFIER\_NON\_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="7526f-130">Um dos sinalizadores do modificador do \_ modificador D3DBUSIMPL \_ \_ xxx está definido.</span><span class="sxs-lookup"><span data-stu-id="7526f-130">One of the D3DBUSIMPL\_MODIFIER\_MODIFIER\_Xxx flags is set.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7526f-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="7526f-131">Remarks</span></span>

<span data-ttu-id="7526f-132">Até três sinalizadores podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="7526f-132">As many as three flags can be set.</span></span> <span data-ttu-id="7526f-133">Os sinalizadores no intervalo de 0x00 a 0x04 (**D3DBUSTYPE \_ xxx**) fornecem o tipo de barramento básico.</span><span class="sxs-lookup"><span data-stu-id="7526f-133">Flags in the range 0x00 through 0x04 (**D3DBUSTYPE\_Xxx**) provide the basic bus type.</span></span> <span data-ttu-id="7526f-134">Os sinalizadores no intervalo 0x10000 por meio de 0x50000 (**D3DBUSIMPL \_ modificador \_ xxx**) modificam a descrição básica.</span><span class="sxs-lookup"><span data-stu-id="7526f-134">Flags in the range 0x10000 through 0x50000 (**D3DBUSIMPL\_MODIFIER\_Xxx**) modify the basic description.</span></span> <span data-ttu-id="7526f-135">O driver define um sinalizador de tipo de barramento e pode definir zero ou um sinalizador modificador.</span><span class="sxs-lookup"><span data-stu-id="7526f-135">The driver sets one bus-type flag, and can set zero or one modifier flag.</span></span> <span data-ttu-id="7526f-136">Se o driver definir um sinalizador de modificador, ele também definirá o sinalizador **D3DBUSIMPL de \_ modificador \_ não \_ padrão** .</span><span class="sxs-lookup"><span data-stu-id="7526f-136">If the driver sets a modifier flag, it also sets the **D3DBUSIMPL\_MODIFIER\_NON\_STANDARD** flag.</span></span> <span data-ttu-id="7526f-137">Os sinalizadores são combinados com um **OR bit a** bit.</span><span class="sxs-lookup"><span data-stu-id="7526f-137">Flags are combined with a bitwise **OR**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7526f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7526f-138">Requirements</span></span>



| <span data-ttu-id="7526f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="7526f-139">Requirement</span></span> | <span data-ttu-id="7526f-140">Valor</span><span class="sxs-lookup"><span data-stu-id="7526f-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7526f-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7526f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7526f-142">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7526f-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7526f-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7526f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7526f-144">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="7526f-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7526f-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7526f-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7526f-146"><dt>D3d9types. h (incluir D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7526f-146"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7526f-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="7526f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7526f-148">Enumerações de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="7526f-148">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




