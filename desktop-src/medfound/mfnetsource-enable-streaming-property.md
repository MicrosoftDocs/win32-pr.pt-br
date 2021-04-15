---
description: Especifica se todos os protocolos de streaming estão habilitados.
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: Propriedade MFNETSOURCE_ENABLE_STREAMING (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc8ae10dedd5cb904e43ee79ff64e8f451e37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502097"
---
# <a name="mfnetsource_enable_streaming-property"></a><span data-ttu-id="5df2c-103">MFNETSOURCE \_ habilitar a \_ Propriedade streaming</span><span class="sxs-lookup"><span data-stu-id="5df2c-103">MFNETSOURCE\_ENABLE\_STREAMING property</span></span>

<span data-ttu-id="5df2c-104">Especifica se todos os protocolos de streaming estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="5df2c-104">Specifies whether all streaming protocols are enabled.</span></span>



<span data-ttu-id="5df2c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5df2c-105">Data type</span></span>

<span data-ttu-id="5df2c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="5df2c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5df2c-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="5df2c-107">PROPVARIANT member</span></span>

<span data-ttu-id="5df2c-108">Booliano (**longo**)</span><span class="sxs-lookup"><span data-stu-id="5df2c-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="5df2c-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="5df2c-109">VT\_I4</span></span>

<span data-ttu-id="5df2c-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="5df2c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5df2c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5df2c-111">Remarks</span></span>

<span data-ttu-id="5df2c-112">A constante **MFNETSOURCE \_ habilitar \_ streaming** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5df2c-112">The constant **MFNETSOURCE\_ENABLE\_STREAMING** defines the GUID for this property key.</span></span> <span data-ttu-id="5df2c-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="5df2c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="5df2c-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="5df2c-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="5df2c-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** para a [configuração de uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5df2c-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5df2c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5df2c-116">Requirements</span></span>



| <span data-ttu-id="5df2c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5df2c-117">Requirement</span></span> | <span data-ttu-id="5df2c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5df2c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5df2c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5df2c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5df2c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5df2c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5df2c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5df2c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5df2c-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5df2c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5df2c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5df2c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5df2c-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df2c-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5df2c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5df2c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df2c-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5df2c-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5df2c-127">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5df2c-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="5df2c-128">Protocolos com suporte</span><span class="sxs-lookup"><span data-stu-id="5df2c-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




