---
description: Especifica se o carregador de topologia permite o DXVA (Microsoft DirectX Video Acceleration) na topologia.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: Atributo MF_TOPOLOGY_DXVA_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762440"
---
# <a name="mf_topology_dxva_mode-attribute"></a><span data-ttu-id="a5f7a-103">\_Atributo do \_ modo DXVA da topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="a5f7a-103">MF\_TOPOLOGY\_DXVA\_MODE attribute</span></span>

<span data-ttu-id="a5f7a-104">Especifica se o carregador de topologia permite o DXVA (Microsoft DirectX Video Acceleration) na topologia.</span><span class="sxs-lookup"><span data-stu-id="a5f7a-104">Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5f7a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a5f7a-105">Data type</span></span>

<span data-ttu-id="a5f7a-106">**[**MFTOPOLOGY \_ \_Modo DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5f7a-106">**[**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a5f7a-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="a5f7a-107">Get/set</span></span>

<span data-ttu-id="a5f7a-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a5f7a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a5f7a-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a5f7a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a5f7a-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="a5f7a-110">Applies to</span></span>

[<span data-ttu-id="a5f7a-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="a5f7a-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="a5f7a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5f7a-112">Remarks</span></span>

<span data-ttu-id="a5f7a-113">O valor desse atributo é uma constante de enumeração do [**\_ \_ modo MFTOPOLOGY DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) .</span><span class="sxs-lookup"><span data-stu-id="a5f7a-113">The value of this attribute is an [**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) enumeration constant.</span></span> <span data-ttu-id="a5f7a-114">O valor padrão é **MFTOPOLOGY \_ DXVA \_ Default**.</span><span class="sxs-lookup"><span data-stu-id="a5f7a-114">The default value is **MFTOPOLOGY\_DXVA\_DEFAULT**.</span></span>

<span data-ttu-id="a5f7a-115">Esse atributo controla qual MFTs recebe um ponteiro para o Gerenciador de dispositivos do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a5f7a-115">This attribute controls which MFTs receive a pointer to the Direct3D device manager.</span></span> <span data-ttu-id="a5f7a-116">Para habilitar a aceleração de vídeo completa, defina o valor como **MFTOPOLOGY \_ DXVA \_ Full**.</span><span class="sxs-lookup"><span data-stu-id="a5f7a-116">To enable full video acceleration, set the value to **MFTOPOLOGY\_DXVA\_FULL**.</span></span> <span data-ttu-id="a5f7a-117">O valor **\_ \_ padrão de DXVA MFTOPOLOGY** é definido para compatibilidade com versões anteriores; ele corresponde ao comportamento de todas as versões mais antigas do Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a5f7a-117">The value **MFTOPOLOGY\_DXVA\_DEFAULT** is defined for backward compatibility; it matches the behavior of all earlier versions of Microsoft Media Foundation.</span></span>

<span data-ttu-id="a5f7a-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a5f7a-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f7a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5f7a-119">Requirements</span></span>



| <span data-ttu-id="a5f7a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5f7a-120">Requirement</span></span> | <span data-ttu-id="a5f7a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a5f7a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f7a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5f7a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a5f7a-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a5f7a-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a5f7a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5f7a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a5f7a-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="a5f7a-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a5f7a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5f7a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5f7a-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5f7a-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5f7a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5f7a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f7a-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5f7a-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5f7a-130">Gerenciador de Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="a5f7a-130">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="a5f7a-131">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="a5f7a-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




