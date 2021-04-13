---
description: Especifica o protocolo de controle usado pela fonte de rede.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: Propriedade MFNETSOURCE_PROTOCOL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188eeb1f6669544291f4dca95db8a4a45a50d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501631"
---
# <a name="mfnetsource_protocol-property"></a><span data-ttu-id="75094-103">\_Propriedade de protocolo MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="75094-103">MFNETSOURCE\_PROTOCOL property</span></span>

<span data-ttu-id="75094-104">Especifica o protocolo de controle usado pela fonte de rede.</span><span class="sxs-lookup"><span data-stu-id="75094-104">Specifies the control protocol used by the network source.</span></span> <span data-ttu-id="75094-105">O valor dessa propriedade é um membro da enumeração de [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="75094-105">The value of this property is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>



<span data-ttu-id="75094-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="75094-106">Data type</span></span>

<span data-ttu-id="75094-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="75094-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="75094-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="75094-108">PROPVARIANT member</span></span>

<span data-ttu-id="75094-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="75094-109">**LONG**</span></span>

<span data-ttu-id="75094-110">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="75094-110">VT\_I4</span></span>

<span data-ttu-id="75094-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="75094-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="75094-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="75094-112">Remarks</span></span>

<span data-ttu-id="75094-113">O **\_ protocolo MFNETSOURCE** constante define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="75094-113">The constant **MFNETSOURCE\_PROTOCOL** defines the GUID for this property key.</span></span> <span data-ttu-id="75094-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="75094-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="75094-115">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="75094-115">This property is read-only.</span></span> <span data-ttu-id="75094-116">Para recuperar essa propriedade, consulte a origem da rede para a interface **IPropertyStore** e chame **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="75094-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="75094-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75094-117">Requirements</span></span>



| <span data-ttu-id="75094-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75094-118">Requirement</span></span> | <span data-ttu-id="75094-119">Valor</span><span class="sxs-lookup"><span data-stu-id="75094-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75094-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75094-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75094-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75094-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="75094-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75094-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75094-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75094-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="75094-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75094-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75094-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75094-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75094-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="75094-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75094-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75094-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="75094-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75094-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="75094-129">Protocolos com suporte</span><span class="sxs-lookup"><span data-stu-id="75094-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




