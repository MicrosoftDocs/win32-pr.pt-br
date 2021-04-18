---
description: Especifica a largura de banda do par de pacotes e a largura de banda de tempo de execução detectada pela origem da rede.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: Propriedade MFNETSOURCE_PPBANDWIDTH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772663"
---
# <a name="mfnetsource_ppbandwidth-property"></a><span data-ttu-id="1ea91-103">\_Propriedade MFNETSOURCE PPBANDWIDTH</span><span class="sxs-lookup"><span data-stu-id="1ea91-103">MFNETSOURCE\_PPBANDWIDTH property</span></span>

<span data-ttu-id="1ea91-104">Especifica a largura de banda do par de pacotes e a largura de banda de tempo de execução detectada pela origem da rede.</span><span class="sxs-lookup"><span data-stu-id="1ea91-104">Specifies the packet-pair bandwidth and run-time bandwidth detected by the network source.</span></span> <span data-ttu-id="1ea91-105">O valor da propriedade é uma matriz de dois valores:</span><span class="sxs-lookup"><span data-stu-id="1ea91-105">The property value is a array of two values:</span></span>

-   <span data-ttu-id="1ea91-106">Largura de banda do par de pacotes, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1ea91-106">Packet-pair bandwidth, in bits per second.</span></span>
-   <span data-ttu-id="1ea91-107">A largura de banda em tempo de execução, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1ea91-107">Run-time bandwidth, in bits per second.</span></span>



<span data-ttu-id="1ea91-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1ea91-108">Data type</span></span>

<span data-ttu-id="1ea91-109">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1ea91-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1ea91-110">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1ea91-110">PROPVARIANT member</span></span>

<span data-ttu-id="1ea91-111">Matriz de valores **ULONG** (**Caul**)</span><span class="sxs-lookup"><span data-stu-id="1ea91-111">Array of **ULONG** values (**CAUL**)</span></span>

<span data-ttu-id="1ea91-112">\_UI4 de vetor \| VT \_ VT</span><span class="sxs-lookup"><span data-stu-id="1ea91-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="1ea91-113">**caul**</span><span class="sxs-lookup"><span data-stu-id="1ea91-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="1ea91-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ea91-114">Remarks</span></span>

<span data-ttu-id="1ea91-115">A constante **MFNETSOURCE \_ PPBANDWIDTH** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1ea91-115">The constant **MFNETSOURCE\_PPBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="1ea91-116">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="1ea91-116">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="1ea91-117">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1ea91-117">This property is read-only.</span></span> <span data-ttu-id="1ea91-118">Para recuperar essa propriedade, consulte a origem da rede para a interface **IPropertyStore** e chame **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="1ea91-118">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ea91-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ea91-119">Requirements</span></span>



| <span data-ttu-id="1ea91-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ea91-120">Requirement</span></span> | <span data-ttu-id="1ea91-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1ea91-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea91-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ea91-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1ea91-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ea91-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1ea91-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ea91-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1ea91-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ea91-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1ea91-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ea91-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ea91-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ea91-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ea91-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ea91-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea91-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ea91-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1ea91-130">Recursos de origem da rede</span><span class="sxs-lookup"><span data-stu-id="1ea91-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="1ea91-131">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ea91-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




