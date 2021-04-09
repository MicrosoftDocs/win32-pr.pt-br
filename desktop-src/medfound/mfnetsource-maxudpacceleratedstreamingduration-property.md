---
description: Duração máxima de streaming acelerado, em milissegundos, quando a origem da rede usa o transporte UDP.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: Propriedade MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011697"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a><span data-ttu-id="35035-103">\_Propriedade MFNETSOURCE MAXUDPACCELERATEDSTREAMINGDURATION</span><span class="sxs-lookup"><span data-stu-id="35035-103">MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="35035-104">Duração máxima de streaming acelerado, em milissegundos, quando a origem da rede usa o transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="35035-104">Maximum duration of accelerated streaming, in milliseconds, when the network source uses UDP transport.</span></span>



<span data-ttu-id="35035-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="35035-105">Data type</span></span>

<span data-ttu-id="35035-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="35035-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="35035-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="35035-107">PROPVARIANT member</span></span>

<span data-ttu-id="35035-108">**DWORD** (armazenado como **longo**)</span><span class="sxs-lookup"><span data-stu-id="35035-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="35035-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="35035-109">VT\_I4</span></span>

<span data-ttu-id="35035-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="35035-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="35035-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="35035-111">Remarks</span></span>

<span data-ttu-id="35035-112">A constante **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="35035-112">The constant **MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="35035-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="35035-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="35035-114">Para o transporte UDP, essa propriedade substitui a propriedade [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) se o valor dessa propriedade for menor.</span><span class="sxs-lookup"><span data-stu-id="35035-114">For UDP transport, this property overrides the [**MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) property if the value of this property is lower.</span></span>

<span data-ttu-id="35035-115">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="35035-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="35035-116">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="35035-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="35035-117">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="35035-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="35035-118">O valor padrão dessa propriedade é 8.000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="35035-118">The default value of this property is 8,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="35035-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35035-119">Requirements</span></span>



| <span data-ttu-id="35035-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="35035-120">Requirement</span></span> | <span data-ttu-id="35035-121">Valor</span><span class="sxs-lookup"><span data-stu-id="35035-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35035-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35035-122">Minimum supported client</span></span><br/> | <span data-ttu-id="35035-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35035-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="35035-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35035-124">Minimum supported server</span></span><br/> | <span data-ttu-id="35035-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35035-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="35035-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35035-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="35035-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="35035-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35035-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="35035-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35035-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35035-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="35035-130">Recursos de origem da rede</span><span class="sxs-lookup"><span data-stu-id="35035-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="35035-131">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35035-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




