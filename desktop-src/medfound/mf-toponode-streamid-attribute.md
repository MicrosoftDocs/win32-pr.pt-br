---
description: O identificador de fluxo do coletor de fluxo associado a este nó de topologia.
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: Atributo MF_TOPONODE_STREAMID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2377183927cf75c6e0a7436384426dcab94680c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815410"
---
# <a name="mf_toponode_streamid-attribute"></a><span data-ttu-id="bd96a-103">\_Atributo TOPONODE de \_ STREAMid MF</span><span class="sxs-lookup"><span data-stu-id="bd96a-103">MF\_TOPONODE\_STREAMID attribute</span></span>

<span data-ttu-id="bd96a-104">O identificador de fluxo do coletor de fluxo associado a este nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="bd96a-104">The stream identifier of the stream sink associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="bd96a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bd96a-105">Data type</span></span>

<span data-ttu-id="bd96a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bd96a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bd96a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd96a-107">Remarks</span></span>

<span data-ttu-id="bd96a-108">Esse atributo se aplica a nós de saída (**\_ nó de \_ saída \_ da topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="bd96a-108">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="bd96a-109">Quando a sessão de mídia carrega a topologia, ela consulta o coletor de mídia para um coletor de fluxo com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="bd96a-109">When the Media Session loads the topology, it queries the media sink for a stream sink with the specified identifier.</span></span> <span data-ttu-id="bd96a-110">Se isso falhar, ele tentará adicionar um novo coletor de fluxo ao coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="bd96a-110">If that fails, it attempts to add a new stream sink to the media sink.</span></span>

<span data-ttu-id="bd96a-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="bd96a-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd96a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd96a-112">Requirements</span></span>



| <span data-ttu-id="bd96a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd96a-113">Requirement</span></span> | <span data-ttu-id="bd96a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bd96a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd96a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd96a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bd96a-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd96a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bd96a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd96a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bd96a-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd96a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bd96a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd96a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd96a-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd96a-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd96a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd96a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd96a-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd96a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bd96a-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bd96a-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="bd96a-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="bd96a-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="bd96a-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="bd96a-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="bd96a-126">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="bd96a-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




