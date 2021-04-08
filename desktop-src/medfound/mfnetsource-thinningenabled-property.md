---
description: Especifica se a alternância de fluxo está habilitada na origem da rede.
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: Propriedade MFNETSOURCE_THINNINGENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d5b1b362f8776e80e3d12b591dbf2116217846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920628"
---
# <a name="mfnetsource_thinningenabled-property"></a><span data-ttu-id="b6fde-103">\_Propriedade MFNETSOURCE THINNINGENABLED</span><span class="sxs-lookup"><span data-stu-id="b6fde-103">MFNETSOURCE\_THINNINGENABLED property</span></span>

<span data-ttu-id="b6fde-104">Especifica se a alternância de fluxo está habilitada na origem da rede.</span><span class="sxs-lookup"><span data-stu-id="b6fde-104">Specifies whether stream switching is enabled on the network source.</span></span> <span data-ttu-id="b6fde-105">A alternância de fluxo permite que o servidor de mídia altere os fluxos em um arquivo de taxa de bits múltipla (MBR), com base na largura de banda disponível.</span><span class="sxs-lookup"><span data-stu-id="b6fde-105">Stream switching enables the media server to change streams in a multiple bit-rate (MBR) file, based on available bandwidth.</span></span>



<span data-ttu-id="b6fde-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b6fde-106">Data type</span></span>

<span data-ttu-id="b6fde-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="b6fde-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b6fde-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="b6fde-108">PROPVARIANT member</span></span>

<span data-ttu-id="b6fde-109">Booliano (**longo**)</span><span class="sxs-lookup"><span data-stu-id="b6fde-109">Boolean (**LONG**)</span></span>

<span data-ttu-id="b6fde-110">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="b6fde-110">VT\_I4</span></span>

<span data-ttu-id="b6fde-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="b6fde-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="b6fde-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6fde-112">Remarks</span></span>

<span data-ttu-id="b6fde-113">A constante **MFNETSOURCE \_ THINNINGENABLED** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b6fde-113">The constant **MFNETSOURCE\_THINNINGENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="b6fde-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="b6fde-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="b6fde-115">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="b6fde-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="b6fde-116">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="b6fde-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="b6fde-117">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="b6fde-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="b6fde-118">O valor padrão dessa propriedade é **true**.</span><span class="sxs-lookup"><span data-stu-id="b6fde-118">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6fde-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6fde-119">Requirements</span></span>



| <span data-ttu-id="b6fde-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6fde-120">Requirement</span></span> | <span data-ttu-id="b6fde-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b6fde-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6fde-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6fde-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b6fde-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6fde-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b6fde-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6fde-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b6fde-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6fde-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b6fde-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6fde-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6fde-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6fde-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6fde-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6fde-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6fde-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6fde-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b6fde-130">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6fde-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




