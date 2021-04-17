---
description: Especifica se o protocolo de multicast de transmissão de fluxo de mídia (MSB) está habilitado na origem da rede.
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: Propriedade MFNETSOURCE_ENABLE_MSB (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b2a49876cf504bfc4e086ab1e064e6835283a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779929"
---
# <a name="mfnetsource_enable_msb-property"></a><span data-ttu-id="fb526-103">MFNETSOURCE \_ habilitar a \_ Propriedade MSB</span><span class="sxs-lookup"><span data-stu-id="fb526-103">MFNETSOURCE\_ENABLE\_MSB property</span></span>

<span data-ttu-id="fb526-104">Especifica se o protocolo de multicast de transmissão de fluxo de mídia (MSB) está habilitado na origem da rede.</span><span class="sxs-lookup"><span data-stu-id="fb526-104">Specifies whether the Media Stream Broadcast (MSB) multicast protocol is enabled in the network source.</span></span>



<span data-ttu-id="fb526-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fb526-105">Data type</span></span>

<span data-ttu-id="fb526-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="fb526-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="fb526-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="fb526-107">PROPVARIANT member</span></span>

<span data-ttu-id="fb526-108">**LONG**</span><span class="sxs-lookup"><span data-stu-id="fb526-108">**LONG**</span></span>

<span data-ttu-id="fb526-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="fb526-109">VT\_I4</span></span>

<span data-ttu-id="fb526-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="fb526-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="fb526-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb526-111">Remarks</span></span>

<span data-ttu-id="fb526-112">A constante **MFNETSOURCE \_ Enable \_ MSB** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="fb526-112">The constant **MFNETSOURCE\_ENABLE\_MSB** defines the GUID for this property key.</span></span> <span data-ttu-id="fb526-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="fb526-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="fb526-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="fb526-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="fb526-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="fb526-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="fb526-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="fb526-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb526-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb526-117">Requirements</span></span>



| <span data-ttu-id="fb526-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb526-118">Requirement</span></span> | <span data-ttu-id="fb526-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fb526-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb526-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb526-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fb526-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fb526-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fb526-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb526-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fb526-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="fb526-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fb526-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb526-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb526-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb526-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb526-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb526-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb526-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb526-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="fb526-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb526-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="fb526-129">Protocolos com suporte</span><span class="sxs-lookup"><span data-stu-id="fb526-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




