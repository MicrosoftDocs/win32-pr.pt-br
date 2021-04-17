---
description: Especifica se o transporte RTSP (Real-Time Streaming Protocol) está habilitado na origem da rede.
ms.assetid: 299393d2-7949-48ef-a36d-19bb8760fc4e
title: Propriedade MFNETSOURCE_ENABLE_RTSP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac191e6e244a8e341fef0dccd274293f09846aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812085"
---
# <a name="mfnetsource_enable_rtsp-property"></a><span data-ttu-id="fe9b7-103">MFNETSOURCE \_ habilitar a \_ Propriedade RTSP</span><span class="sxs-lookup"><span data-stu-id="fe9b7-103">MFNETSOURCE\_ENABLE\_RTSP property</span></span>

<span data-ttu-id="fe9b7-104">Especifica se o transporte RTSP (Real-Time Streaming Protocol) está habilitado na origem da rede.</span><span class="sxs-lookup"><span data-stu-id="fe9b7-104">Specifies whether Real-Time Streaming Protocol (RTSP) transport is enabled in the network source.</span></span>



<span data-ttu-id="fe9b7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fe9b7-105">Data type</span></span>

<span data-ttu-id="fe9b7-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="fe9b7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="fe9b7-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="fe9b7-107">PROPVARIANT member</span></span>

<span data-ttu-id="fe9b7-108">Booliano (**longo**)</span><span class="sxs-lookup"><span data-stu-id="fe9b7-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="fe9b7-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="fe9b7-109">VT\_I4</span></span>

<span data-ttu-id="fe9b7-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="fe9b7-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="fe9b7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe9b7-111">Remarks</span></span>

<span data-ttu-id="fe9b7-112">A constante **MFNETSOURCE \_ habilitar \_ RTSP** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="fe9b7-112">The constant **MFNETSOURCE\_ENABLE\_RTSP** defines the GUID for this property key.</span></span> <span data-ttu-id="fe9b7-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="fe9b7-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="fe9b7-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="fe9b7-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="fe9b7-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="fe9b7-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="fe9b7-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="fe9b7-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe9b7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe9b7-117">Requirements</span></span>



| <span data-ttu-id="fe9b7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe9b7-118">Requirement</span></span> | <span data-ttu-id="fe9b7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fe9b7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9b7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe9b7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe9b7-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe9b7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fe9b7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe9b7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe9b7-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe9b7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fe9b7-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe9b7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe9b7-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe9b7-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe9b7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe9b7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe9b7-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fe9b7-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="fe9b7-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fe9b7-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="fe9b7-129">Protocolos com suporte</span><span class="sxs-lookup"><span data-stu-id="fe9b7-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




