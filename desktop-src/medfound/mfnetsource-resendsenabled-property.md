---
description: Especifica se a origem da rede envia solicitações UDP de reenvio em resposta a pacotes perdidos.
ms.assetid: 7956536d-9f3d-4875-8006-17e2cd577b61
title: Propriedade MFNETSOURCE_RESENDSENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2646a9ef3e23fbcc9b3dff205f87d268115177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756502"
---
# <a name="mfnetsource_resendsenabled-property"></a><span data-ttu-id="fac7b-103">\_Propriedade MFNETSOURCE RESENDSENABLED</span><span class="sxs-lookup"><span data-stu-id="fac7b-103">MFNETSOURCE\_RESENDSENABLED property</span></span>

<span data-ttu-id="fac7b-104">Especifica se a origem da rede envia solicitações UDP de reenvio em resposta a pacotes perdidos.</span><span class="sxs-lookup"><span data-stu-id="fac7b-104">Specifies whether the network source sends UDP resend requests in response to lost packets.</span></span>



<span data-ttu-id="fac7b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fac7b-105">Data type</span></span>

<span data-ttu-id="fac7b-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="fac7b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="fac7b-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="fac7b-107">PROPVARIANT member</span></span>

<span data-ttu-id="fac7b-108">Booliano (**longo**)</span><span class="sxs-lookup"><span data-stu-id="fac7b-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="fac7b-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="fac7b-109">VT\_I4</span></span>

<span data-ttu-id="fac7b-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="fac7b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="fac7b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fac7b-111">Remarks</span></span>

<span data-ttu-id="fac7b-112">A constante **MFNETSOURCE \_ RESENDSENABLED** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="fac7b-112">The constant **MFNETSOURCE\_RESENDSENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="fac7b-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="fac7b-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="fac7b-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="fac7b-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="fac7b-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="fac7b-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="fac7b-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="fac7b-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="fac7b-117">O valor padrão dessa propriedade é **true**.</span><span class="sxs-lookup"><span data-stu-id="fac7b-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac7b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fac7b-118">Requirements</span></span>



| <span data-ttu-id="fac7b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fac7b-119">Requirement</span></span> | <span data-ttu-id="fac7b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fac7b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fac7b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fac7b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fac7b-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fac7b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fac7b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fac7b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fac7b-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fac7b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fac7b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fac7b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fac7b-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fac7b-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac7b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fac7b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac7b-128">Log de cliente</span><span class="sxs-lookup"><span data-stu-id="fac7b-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="fac7b-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fac7b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="fac7b-130">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fac7b-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




