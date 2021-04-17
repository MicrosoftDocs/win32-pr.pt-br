---
description: O intervalo de portas UDP válidas que a fonte de rede pode usar para receber conteúdo de streaming.
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: Propriedade MFNETSOURCE_UDP_PORT_RANGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04db8c450bd20adc8c03ec3b964b543f1500aa51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812217"
---
# <a name="mfnetsource_udp_port_range-property"></a><span data-ttu-id="b924f-103">\_Propriedade de \_ intervalo de portas UDP MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="b924f-103">MFNETSOURCE\_UDP\_PORT\_RANGE property</span></span>

<span data-ttu-id="b924f-104">O intervalo de portas UDP válidas que a fonte de rede pode usar para receber conteúdo de streaming.</span><span class="sxs-lookup"><span data-stu-id="b924f-104">The range of valid UDP ports that the network source can use to receive streaming content.</span></span> <span data-ttu-id="b924f-105">O valor dessa propriedade é uma cadeia de caracteres com o formato " *m*–*n* ", em que *m* e *n* são números de porta.</span><span class="sxs-lookup"><span data-stu-id="b924f-105">The value of this property is a string with the form " *m*–*n* " where *m* and *n* are port numbers.</span></span>



<span data-ttu-id="b924f-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b924f-106">Data type</span></span>

<span data-ttu-id="b924f-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="b924f-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b924f-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="b924f-108">PROPVARIANT member</span></span>

<span data-ttu-id="b924f-109">Cadeia de caracteres largos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="b924f-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="b924f-110">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="b924f-110">VT\_LPWSTR</span></span>

<span data-ttu-id="b924f-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="b924f-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="b924f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b924f-112">Remarks</span></span>

<span data-ttu-id="b924f-113">O **intervalo de \_ \_ portas UDP \_ MFNETSOURCE** constante define o GUID dessa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b924f-113">The constant **MFNETSOURCE\_UDP\_PORT\_RANGE** defines the GUID for this property key.</span></span> <span data-ttu-id="b924f-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="b924f-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="b924f-115">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="b924f-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="b924f-116">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="b924f-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="b924f-117">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="b924f-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b924f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b924f-118">Requirements</span></span>



| <span data-ttu-id="b924f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b924f-119">Requirement</span></span> | <span data-ttu-id="b924f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b924f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b924f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b924f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b924f-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b924f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b924f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b924f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b924f-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b924f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b924f-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b924f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b924f-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b924f-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b924f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b924f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b924f-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b924f-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b924f-129">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b924f-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




