---
description: Especifica se a sessão de mídia tenta modificar a topologia quando o formato de um fluxo é alterado.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: Atributo MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461080"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a><span data-ttu-id="5ac8a-103">\_Atributo de \_ alteração dinâmica de topologia MF \_ \_ não \_ permitido</span><span class="sxs-lookup"><span data-stu-id="5ac8a-103">MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute</span></span>

<span data-ttu-id="5ac8a-104">Especifica se a sessão de mídia tenta modificar a topologia quando o formato de um fluxo é alterado.</span><span class="sxs-lookup"><span data-stu-id="5ac8a-104">Specifies whether the Media Session attempts to modify the topology when the format of a stream changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="5ac8a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5ac8a-105">Data type</span></span>

<span data-ttu-id="5ac8a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5ac8a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5ac8a-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="5ac8a-107">Get/set</span></span>

<span data-ttu-id="5ac8a-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5ac8a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5ac8a-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5ac8a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5ac8a-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="5ac8a-110">Applies to</span></span>

[<span data-ttu-id="5ac8a-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="5ac8a-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="5ac8a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ac8a-112">Remarks</span></span>

<span data-ttu-id="5ac8a-113">Esse atributo controla como a sessão de mídia responde se o formato de um fluxo for alterado durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="5ac8a-113">This attribute controls how the Media Session responds if the format of a stream changes during streaming.</span></span>

<span data-ttu-id="5ac8a-114">Se o formato for alterado e o \_ \_ atributo alteração dinâmica de topologia MF \_ \_ não \_ permitido for **falso**, a sessão de mídia poderá inserir novos nós na topologia para corresponder ao novo formato.</span><span class="sxs-lookup"><span data-stu-id="5ac8a-114">If the format changes and the MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute is **FALSE**, the Media Session might insert new nodes into the topology to match the new format.</span></span> <span data-ttu-id="5ac8a-115">Por exemplo, se o tamanho do vídeo for alterado, a sessão de mídia poderá adicionar uma Media Foundation transformação (MFT) que redimensiona o vídeo.</span><span class="sxs-lookup"><span data-stu-id="5ac8a-115">For example, if the video size changes, the Media Session might add a Media Foundation transform (MFT) that resizes the video.</span></span> <span data-ttu-id="5ac8a-116">Caso contrário, se o atributo for **true**, a sessão de mídia não modificará a topologia.</span><span class="sxs-lookup"><span data-stu-id="5ac8a-116">Otherwise, if the attribute is **TRUE**, the Media Session will not modify the topology.</span></span>

<span data-ttu-id="5ac8a-117">O valor padrão desse atributo é **false**.</span><span class="sxs-lookup"><span data-stu-id="5ac8a-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="5ac8a-118">O valor recomendado é **false**.</span><span class="sxs-lookup"><span data-stu-id="5ac8a-118">The recommended value is **FALSE**.</span></span>

<span data-ttu-id="5ac8a-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5ac8a-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac8a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ac8a-120">Requirements</span></span>



| <span data-ttu-id="5ac8a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac8a-121">Requirement</span></span> | <span data-ttu-id="5ac8a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5ac8a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac8a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ac8a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac8a-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5ac8a-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5ac8a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ac8a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac8a-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5ac8a-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5ac8a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ac8a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac8a-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ac8a-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac8a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ac8a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac8a-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5ac8a-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5ac8a-131">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="5ac8a-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




