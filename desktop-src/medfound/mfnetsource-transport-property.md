---
description: Especifica o protocolo de transporte usado pela fonte de rede.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: Propriedade MFNETSOURCE_TRANSPORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd41653f2b5ea0686527af4d6ee8c8b9962005aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827408"
---
# <a name="mfnetsource_transport-property"></a><span data-ttu-id="3a4a9-103">\_Propriedade de transporte MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="3a4a9-103">MFNETSOURCE\_TRANSPORT property</span></span>

<span data-ttu-id="3a4a9-104">Especifica o protocolo de transporte usado pela fonte de rede.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-104">Specifies the transport protocol used by the network source.</span></span> <span data-ttu-id="3a4a9-105">O valor dessa propriedade é um membro da enumeração de [**\_ \_ tipo de transporte MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="3a4a9-105">The value of this property is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>



<span data-ttu-id="3a4a9-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3a4a9-106">Data type</span></span>

<span data-ttu-id="3a4a9-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="3a4a9-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3a4a9-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="3a4a9-108">PROPVARIANT member</span></span>

<span data-ttu-id="3a4a9-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="3a4a9-109">**LONG**</span></span>

<span data-ttu-id="3a4a9-110">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="3a4a9-110">VT\_I4</span></span>

<span data-ttu-id="3a4a9-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="3a4a9-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="3a4a9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a4a9-112">Remarks</span></span>

<span data-ttu-id="3a4a9-113">O **\_ transporte constante MFNETSOURCE** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-113">The constant **MFNETSOURCE\_TRANSPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="3a4a9-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="3a4a9-115">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-115">This property is read-only.</span></span> <span data-ttu-id="3a4a9-116">Para recuperar essa propriedade, consulte a origem da rede para a interface **IPropertyStore** e chame **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="3a4a9-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4a9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a4a9-117">Requirements</span></span>



| <span data-ttu-id="3a4a9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a4a9-118">Requirement</span></span> | <span data-ttu-id="3a4a9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3a4a9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4a9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a4a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4a9-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a4a9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a4a9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a4a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4a9-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a4a9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a4a9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a4a9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a4a9-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a4a9-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a4a9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a4a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4a9-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a4a9-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3a4a9-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a4a9-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="3a4a9-129">Protocolos com suporte</span><span class="sxs-lookup"><span data-stu-id="3a4a9-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




