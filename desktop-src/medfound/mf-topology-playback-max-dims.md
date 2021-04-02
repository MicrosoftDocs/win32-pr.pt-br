---
description: Especifica o tamanho da janela de destino para reprodução de vídeo.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: Atributo MF_TOPOLOGY_PLAYBACK_MAX_DIMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165013"
---
# <a name="mf_topology_playback_max_dims-attribute"></a><span data-ttu-id="d9287-103">\_Atributo de \_ \_ esmaecimento máximo da reprodução de topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="d9287-103">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS attribute</span></span>

<span data-ttu-id="d9287-104">Especifica o tamanho da janela de destino para reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d9287-104">Specifies the size of the destination window for video playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="d9287-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d9287-105">Data type</span></span>

<span data-ttu-id="d9287-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d9287-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="d9287-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="d9287-107">Get/set</span></span>

<span data-ttu-id="d9287-108">Para obter esse atributo, chame [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span><span class="sxs-lookup"><span data-stu-id="d9287-108">To get this attribute, call [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span></span>

<span data-ttu-id="d9287-109">Para definir esse atributo, chame [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span><span class="sxs-lookup"><span data-stu-id="d9287-109">To set this attribute, call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d9287-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="d9287-110">Applies to</span></span>

[<span data-ttu-id="d9287-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="d9287-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="d9287-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9287-112">Remarks</span></span>

<span data-ttu-id="d9287-113">O carregador de topologia usa esse atributo para otimizar o pipeline antes do início da reprodução.</span><span class="sxs-lookup"><span data-stu-id="d9287-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="d9287-114">Se você definir esse atributo, defina também o atributo de [ \_ \_ \_ \_ otimizações de reprodução estática da topologia MF](mf-topology-static-playback-optimizations.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="d9287-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="d9287-115">Os bits superiores de 32 do valor do atributo contêm a largura e os bits inferiores de 32 contêm a altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d9287-115">The upper 32 bits of the attribute value contain the width and the lower 32 bits contain the height, both in pixels.</span></span>

<span data-ttu-id="d9287-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d9287-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9287-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9287-117">Requirements</span></span>



| <span data-ttu-id="d9287-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9287-118">Requirement</span></span> | <span data-ttu-id="d9287-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d9287-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9287-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9287-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9287-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d9287-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d9287-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9287-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9287-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d9287-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d9287-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9287-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9287-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9287-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9287-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9287-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9287-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9287-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9287-128">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="d9287-128">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9287-129">Gerenciamento de qualidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="d9287-129">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




