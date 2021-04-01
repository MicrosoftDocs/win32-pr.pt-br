---
description: Especifica a taxa de atualização do monitor.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: Atributo MF_TOPOLOGY_PLAYBACK_FRAMERATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165014"
---
# <a name="mf_topology_playback_framerate-attribute"></a><span data-ttu-id="91920-103">\_Atributo de \_ taxa de reprodução da topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="91920-103">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE attribute</span></span>

<span data-ttu-id="91920-104">Especifica a taxa de atualização do monitor.</span><span class="sxs-lookup"><span data-stu-id="91920-104">Specifies the monitor refresh rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="91920-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="91920-105">Data type</span></span>

<span data-ttu-id="91920-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="91920-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="91920-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="91920-107">Get/set</span></span>

<span data-ttu-id="91920-108">Para obter esse atributo, chame [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="91920-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="91920-109">Para definir esse atributo, chame [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="91920-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="applies-to"></a><span data-ttu-id="91920-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="91920-110">Applies to</span></span>

[<span data-ttu-id="91920-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="91920-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="91920-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="91920-112">Remarks</span></span>

<span data-ttu-id="91920-113">O carregador de topologia usa esse atributo para otimizar o pipeline antes do início da reprodução.</span><span class="sxs-lookup"><span data-stu-id="91920-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="91920-114">Se você definir esse atributo, defina também o atributo de [ \_ \_ \_ \_ otimizações de reprodução estática da topologia MF](mf-topology-static-playback-optimizations.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="91920-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="91920-115">A taxa de quadros é expressa como uma taxa.</span><span class="sxs-lookup"><span data-stu-id="91920-115">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="91920-116">Os bits superiores de 32 do valor do atributo contêm o numerador e os bits 32 inferiores contêm o denominador.</span><span class="sxs-lookup"><span data-stu-id="91920-116">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span>

<span data-ttu-id="91920-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="91920-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="91920-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91920-118">Requirements</span></span>



| <span data-ttu-id="91920-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="91920-119">Requirement</span></span> | <span data-ttu-id="91920-120">Valor</span><span class="sxs-lookup"><span data-stu-id="91920-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91920-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91920-121">Minimum supported client</span></span><br/> | <span data-ttu-id="91920-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="91920-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="91920-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91920-123">Minimum supported server</span></span><br/> | <span data-ttu-id="91920-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="91920-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="91920-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91920-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="91920-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91920-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91920-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="91920-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91920-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91920-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="91920-129">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="91920-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="91920-130">Gerenciamento de qualidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="91920-130">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




