---
description: Especifica se a origem da rede armazena em cache o conteúdo.
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: Propriedade MFNETSOURCE_CACHEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6f38398e44eaa25da7a5b1f88a76edb8e40924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827411"
---
# <a name="mfnetsource_cacheenabled-property"></a><span data-ttu-id="1b1f1-103">\_Propriedade MFNETSOURCE CACHEENABLED</span><span class="sxs-lookup"><span data-stu-id="1b1f1-103">MFNETSOURCE\_CACHEENABLED property</span></span>

<span data-ttu-id="1b1f1-104">Especifica se a origem da rede armazena em cache o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1b1f1-104">Specifies whether the network source caches content.</span></span>



<span data-ttu-id="1b1f1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1b1f1-105">Data type</span></span>

<span data-ttu-id="1b1f1-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1b1f1-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1b1f1-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1b1f1-107">PROPVARIANT member</span></span>

<span data-ttu-id="1b1f1-108">Booliano (**longo**)</span><span class="sxs-lookup"><span data-stu-id="1b1f1-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="1b1f1-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="1b1f1-109">VT\_I4</span></span>

<span data-ttu-id="1b1f1-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="1b1f1-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1b1f1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b1f1-111">Remarks</span></span>

<span data-ttu-id="1b1f1-112">A constante **MFNETSOURCE \_ CACHEENABLED** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1b1f1-112">The constant **MFNETSOURCE\_CACHEENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="1b1f1-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="1b1f1-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="1b1f1-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="1b1f1-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="1b1f1-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="1b1f1-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="1b1f1-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="1b1f1-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="1b1f1-117">O valor padrão dessa propriedade é **true**.</span><span class="sxs-lookup"><span data-stu-id="1b1f1-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b1f1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b1f1-118">Requirements</span></span>



| <span data-ttu-id="1b1f1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b1f1-119">Requirement</span></span> | <span data-ttu-id="1b1f1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1b1f1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1f1-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b1f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1f1-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b1f1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1b1f1-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b1f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1f1-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b1f1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1b1f1-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b1f1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b1f1-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b1f1-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b1f1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b1f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b1f1-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b1f1-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1b1f1-129">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b1f1-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




