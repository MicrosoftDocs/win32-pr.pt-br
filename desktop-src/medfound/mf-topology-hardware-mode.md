---
description: Especifica se é para carregar transformações de Microsoft Media Foundation baseadas em hardware (MFTs) na topologia.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: Atributo MF_TOPOLOGY_HARDWARE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760624"
---
# <a name="mf_topology_hardware_mode-attribute"></a><span data-ttu-id="76c0b-103">\_Atributo de \_ modo de hardware de topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="76c0b-103">MF\_TOPOLOGY\_HARDWARE\_MODE attribute</span></span>

<span data-ttu-id="76c0b-104">Especifica se é para carregar transformações de Microsoft Media Foundation baseadas em hardware (MFTs) na topologia.</span><span class="sxs-lookup"><span data-stu-id="76c0b-104">Specifies whether to load hardware-based Microsoft Media Foundation transforms (MFTs) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="76c0b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="76c0b-105">Data type</span></span>

<span data-ttu-id="76c0b-106">**[**MFTOPOLOGY \_ \_Modo de hardware**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="76c0b-106">**[**MFTOPOLOGY\_HARDWARE\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="76c0b-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="76c0b-107">Get/set</span></span>

<span data-ttu-id="76c0b-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="76c0b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="76c0b-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="76c0b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="76c0b-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="76c0b-110">Applies to</span></span>

[<span data-ttu-id="76c0b-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="76c0b-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="76c0b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="76c0b-112">Remarks</span></span>

<span data-ttu-id="76c0b-113">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="76c0b-113">This attribute is optional.</span></span> <span data-ttu-id="76c0b-114">Defina o atributo antes de resolver a topologia.</span><span class="sxs-lookup"><span data-stu-id="76c0b-114">Set the attribute before resolving the topology.</span></span>



| <span data-ttu-id="76c0b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="76c0b-115">Value</span></span>                                  | <span data-ttu-id="76c0b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="76c0b-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76c0b-117">**MFTOPOLOGY \_ HWMODE \_ usar \_ hardware**</span><span class="sxs-lookup"><span data-stu-id="76c0b-117">**MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**</span></span>  | <span data-ttu-id="76c0b-118">O carregador de topologia carregará MFTs baseadas em hardware, como decodificadores de hardware, quando disponível.</span><span class="sxs-lookup"><span data-stu-id="76c0b-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="76c0b-119">O carregador de topologia voltará automaticamente para a decodificação de software se nenhum decodificador de hardware for encontrado ou se um decodificador de hardware não conseguir se conectar por algum motivo.</span><span class="sxs-lookup"><span data-stu-id="76c0b-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="76c0b-120">**\_somente MFTOPOLOGY HWMODE \_ software \_**</span><span class="sxs-lookup"><span data-stu-id="76c0b-120">**MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**</span></span> | <span data-ttu-id="76c0b-121">O carregador de topologia carregará apenas MFTs de software, incluindo os decodificadores de software.</span><span class="sxs-lookup"><span data-stu-id="76c0b-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="76c0b-122">O valor padrão é **MFTOPOLOGY \_ HWMODE \_ software \_ apenas**, para compatibilidade com os aplicativos existentes.</span><span class="sxs-lookup"><span data-stu-id="76c0b-122">The default value is **MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**, for compatibility with existing applications.</span></span> <span data-ttu-id="76c0b-123">O valor recomendado é **MFTOPOLOGY \_ HWMODE \_ use \_ hardware**.</span><span class="sxs-lookup"><span data-stu-id="76c0b-123">The recommended value is **MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**.</span></span>

<span data-ttu-id="76c0b-124">Se o carregador de topologia inserir uma MFT de hardware na topologia, ele definirá o atributo de atributo de URL de hardware de enumeração de MFT no nó de topologia. [ \_ \_ \_ \_ ](mft-enum-hardware-url-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="76c0b-124">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="76c0b-125">Para verificar se um MFT de hardware está presente, enumere os nós na topologia resolvida e verifique se esse atributo está presente.</span><span class="sxs-lookup"><span data-stu-id="76c0b-125">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="76c0b-126">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="76c0b-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="76c0b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76c0b-127">Requirements</span></span>



| <span data-ttu-id="76c0b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="76c0b-128">Requirement</span></span> | <span data-ttu-id="76c0b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="76c0b-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76c0b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76c0b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="76c0b-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="76c0b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="76c0b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76c0b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="76c0b-133">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="76c0b-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="76c0b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76c0b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="76c0b-135"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76c0b-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76c0b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="76c0b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76c0b-137">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76c0b-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="76c0b-138">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="76c0b-138">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




