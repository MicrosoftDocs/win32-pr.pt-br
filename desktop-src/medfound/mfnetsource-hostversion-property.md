---
description: O valor do campo &\# 0034; c-hostexever&\# 0034; que a fonte de rede usa para o registro em log.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: Propriedade MFNETSOURCE_HOSTVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461180"
---
# <a name="mfnetsource_hostversion-property"></a><span data-ttu-id="5e4fd-103">\_Propriedade MFNETSOURCE HOSTVERSION</span><span class="sxs-lookup"><span data-stu-id="5e4fd-103">MFNETSOURCE\_HOSTVERSION property</span></span>

<span data-ttu-id="5e4fd-104">O valor do campo "c-hostexever" usado pela fonte de rede para registro em log.</span><span class="sxs-lookup"><span data-stu-id="5e4fd-104">The value of the "c-hostexever" field that the network source uses for logging.</span></span> <span data-ttu-id="5e4fd-105">Os aplicativos podem definir essa propriedade como o número de versão do aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="5e4fd-105">Applications can set this property to the version number of the host application.</span></span> <span data-ttu-id="5e4fd-106">O aplicativo host é o arquivo. exe identificado pelo campo c-hostexe.</span><span class="sxs-lookup"><span data-stu-id="5e4fd-106">The host application is the .exe file identified by the c-hostexe field.</span></span>



<span data-ttu-id="5e4fd-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5e4fd-107">Data type</span></span>

<span data-ttu-id="5e4fd-108">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="5e4fd-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5e4fd-109">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="5e4fd-109">PROPVARIANT member</span></span>

<span data-ttu-id="5e4fd-110">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="5e4fd-110">**LONGLONG**</span></span>

<span data-ttu-id="5e4fd-111">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="5e4fd-111">VT\_I8</span></span>

<span data-ttu-id="5e4fd-112">**hVal**</span><span class="sxs-lookup"><span data-stu-id="5e4fd-112">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5e4fd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e4fd-113">Remarks</span></span>

<span data-ttu-id="5e4fd-114">A constante **MFNETSOURCE \_ HOSTVERSION** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5e4fd-114">The constant **MFNETSOURCE\_HOSTVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="5e4fd-115">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="5e4fd-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="5e4fd-116">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="5e4fd-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="5e4fd-117">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="5e4fd-117">To set the property, pass an **IPropertyStore** pointer to the Source resolver.</span></span> <span data-ttu-id="5e4fd-118">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5e4fd-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4fd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e4fd-119">Requirements</span></span>



| <span data-ttu-id="5e4fd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e4fd-120">Requirement</span></span> | <span data-ttu-id="5e4fd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5e4fd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e4fd-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e4fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5e4fd-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e4fd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e4fd-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e4fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5e4fd-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e4fd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e4fd-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e4fd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e4fd-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e4fd-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e4fd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e4fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4fd-129">Log de cliente</span><span class="sxs-lookup"><span data-stu-id="5e4fd-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="5e4fd-130">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e4fd-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5e4fd-131">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e4fd-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




