---
description: Número de segundos de dados que a fonte de rede armazena em buffer na inicialização.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: Propriedade MFNETSOURCE_BUFFERINGTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21c165e58ebd5f2aec0f1ca7ce38281f8c94896d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090856"
---
# <a name="mfnetsource_bufferingtime-property"></a><span data-ttu-id="d994c-103">\_Propriedade MFNETSOURCE BUFFERINGTIME</span><span class="sxs-lookup"><span data-stu-id="d994c-103">MFNETSOURCE\_BUFFERINGTIME property</span></span>

<span data-ttu-id="d994c-104">Número de segundos de dados que a fonte de rede armazena em buffer na inicialização.</span><span class="sxs-lookup"><span data-stu-id="d994c-104">Number of seconds of data that the network source buffers at startup.</span></span>



<span data-ttu-id="d994c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d994c-105">Data type</span></span>

<span data-ttu-id="d994c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d994c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d994c-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d994c-107">PROPVARIANT member</span></span>

<span data-ttu-id="d994c-108">**DWORD** (armazenado como **longo**)</span><span class="sxs-lookup"><span data-stu-id="d994c-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="d994c-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="d994c-109">VT\_I4</span></span>

<span data-ttu-id="d994c-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="d994c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d994c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d994c-111">Remarks</span></span>

<span data-ttu-id="d994c-112">A constante **MFNETSOURCE \_ BUFFERINGTIME** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d994c-112">The constant **MFNETSOURCE\_BUFFERINGTIME** defines the GUID for this property key.</span></span> <span data-ttu-id="d994c-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="d994c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d994c-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="d994c-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="d994c-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="d994c-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="d994c-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d994c-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="d994c-117">O valor padrão dessa propriedade é 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="d994c-117">The default value of this property is 5 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="d994c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d994c-118">Requirements</span></span>



| <span data-ttu-id="d994c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d994c-119">Requirement</span></span> | <span data-ttu-id="d994c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d994c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d994c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d994c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d994c-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d994c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d994c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d994c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d994c-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d994c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d994c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d994c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d994c-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d994c-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d994c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d994c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d994c-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d994c-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d994c-129">Recursos de origem da rede</span><span class="sxs-lookup"><span data-stu-id="d994c-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="d994c-130">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d994c-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




