---
description: Especifica a hora de parada de uma topologia, em relação ao início da primeira topologia na sequência.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: Atributo MF_TOPOLOGY_PROJECTSTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7e3d50bd89e0fdfc032f9854c1a183276f04a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827620"
---
# <a name="mf_topology_projectstart-attribute"></a><span data-ttu-id="13d8e-103">\_Atributo PROJECTSTART da topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="13d8e-103">MF\_TOPOLOGY\_PROJECTSTART attribute</span></span>

<span data-ttu-id="13d8e-104">Especifica a hora de parada de uma topologia, em relação ao início da primeira topologia na sequência.</span><span class="sxs-lookup"><span data-stu-id="13d8e-104">Specifies the stop time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="13d8e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="13d8e-105">Data type</span></span>

<span data-ttu-id="13d8e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="13d8e-106">**UINT64**</span></span>

<span data-ttu-id="13d8e-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="13d8e-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13d8e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="13d8e-108">Remarks</span></span>

<span data-ttu-id="13d8e-109">O valor é fornecido em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="13d8e-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="13d8e-110">Se a sessão de mídia tiver sido criada com o atributo de [**\_ \_ \_ tempo global de sessão MF**](mf-session-global-time-attribute.md) igual a **true**, todas as topologias deverão conter o atributo **\_ \_ PROJECTSTART da topologia MF** .</span><span class="sxs-lookup"><span data-stu-id="13d8e-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="13d8e-111">Caso contrário, as topologias não devem conter o atributo **\_ \_ PROJECTSTART da topologia MF** .</span><span class="sxs-lookup"><span data-stu-id="13d8e-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="13d8e-112">Para obter mais informações, consulte [tempos de apresentação da sequência](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="13d8e-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="13d8e-113">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="13d8e-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="13d8e-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="13d8e-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d8e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d8e-115">Requirements</span></span>



| <span data-ttu-id="13d8e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d8e-116">Requirement</span></span> | <span data-ttu-id="13d8e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="13d8e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="13d8e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13d8e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13d8e-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13d8e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="13d8e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13d8e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13d8e-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13d8e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="13d8e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13d8e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="13d8e-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="13d8e-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d8e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="13d8e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d8e-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13d8e-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="13d8e-126">Tempos de apresentação da sequência</span><span class="sxs-lookup"><span data-stu-id="13d8e-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="13d8e-127">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="13d8e-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="13d8e-128">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="13d8e-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="13d8e-129">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="13d8e-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="13d8e-130">**\_PROJECTSTOP de topologia MF \_**</span><span class="sxs-lookup"><span data-stu-id="13d8e-130">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




