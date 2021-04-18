---
description: Especifica se a sessão de mídia usa a preversão no coletor de mídia representado por esse nó de topologia.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: Atributo MF_TOPONODE_DISABLE_PREROLL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752157"
---
# <a name="mf_toponode_disable_preroll-attribute"></a><span data-ttu-id="4f713-103">\_TOPONODE de \_ \_ desrollização de DESABILITAção de MF</span><span class="sxs-lookup"><span data-stu-id="4f713-103">MF\_TOPONODE\_DISABLE\_PREROLL attribute</span></span>

<span data-ttu-id="4f713-104">Especifica se a sessão de mídia usa a preversão no coletor de mídia representado por esse nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="4f713-104">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="4f713-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4f713-105">Data type</span></span>

<span data-ttu-id="4f713-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4f713-106">**UINT32**</span></span>

<span data-ttu-id="4f713-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="4f713-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f713-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f713-108">Remarks</span></span>

<span data-ttu-id="4f713-109">Esse atributo se aplica a nós de saída (**\_ nó de \_ saída \_ da topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="4f713-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="4f713-110">Se o valor desse atributo for **true**, a sessão de mídia não preverterá nenhum dado para o coletor de mídia, mesmo que o coletor de mídia exponha a interface [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="4f713-110">If the value of this attribute is **TRUE**, the Media Session does not preroll any data to the media sink, even if the media sink exposes the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span> <span data-ttu-id="4f713-111">Se o valor for **false**, a sessão de mídia preverterá os dados se o coletor de mídia implementar **IMFMediaSinkPreroll**.</span><span class="sxs-lookup"><span data-stu-id="4f713-111">If the value is **FALSE**, the Media Session prerolls data if the media sink implements **IMFMediaSinkPreroll**.</span></span> <span data-ttu-id="4f713-112">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="4f713-112">The default value is **FALSE**.</span></span>

<span data-ttu-id="4f713-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4f713-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f713-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f713-114">Requirements</span></span>



| <span data-ttu-id="4f713-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f713-115">Requirement</span></span> | <span data-ttu-id="4f713-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4f713-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f713-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f713-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4f713-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f713-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4f713-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f713-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4f713-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f713-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4f713-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f713-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f713-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f713-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f713-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f713-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f713-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4f713-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f713-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4f713-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4f713-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="4f713-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4f713-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="4f713-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="4f713-128">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="4f713-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




