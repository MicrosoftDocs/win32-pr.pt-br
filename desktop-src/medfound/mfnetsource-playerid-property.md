---
description: O valor do campo &\# 0034; c-playerid&\# 0034; que a fonte de rede usa para o registro em log.
ms.assetid: de52cc34-9b88-41ae-b8b8-ef5dff85892c
title: Propriedade MFNETSOURCE_PLAYERID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d20754c93057ef3f000fc9c7201cda7ec287eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011400"
---
# <a name="mfnetsource_playerid-property"></a><span data-ttu-id="15cd5-103">\_Propriedade MFNETSOURCE playerid</span><span class="sxs-lookup"><span data-stu-id="15cd5-103">MFNETSOURCE\_PLAYERID property</span></span>

<span data-ttu-id="15cd5-104">O valor do campo "c-playerid" que a fonte de rede usa para registro em log.</span><span class="sxs-lookup"><span data-stu-id="15cd5-104">The value of the "c-playerid" field that the network source uses for logging.</span></span> <span data-ttu-id="15cd5-105">Os aplicativos podem definir essa propriedade como qualquer valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="15cd5-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="15cd5-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="15cd5-106">Data type</span></span>

<span data-ttu-id="15cd5-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="15cd5-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="15cd5-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="15cd5-108">PROPVARIANT member</span></span>

<span data-ttu-id="15cd5-109">Cadeia de caracteres largos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="15cd5-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="15cd5-110">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="15cd5-110">VT\_LPWSTR</span></span>

<span data-ttu-id="15cd5-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="15cd5-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="15cd5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="15cd5-112">Remarks</span></span>

<span data-ttu-id="15cd5-113">A constante **MFNETSOURCE \_ playerid** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="15cd5-113">The constant **MFNETSOURCE\_PLAYERID** defines the GUID for this property key.</span></span> <span data-ttu-id="15cd5-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="15cd5-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="15cd5-115">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="15cd5-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="15cd5-116">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="15cd5-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="15cd5-117">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="15cd5-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15cd5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15cd5-118">Requirements</span></span>



| <span data-ttu-id="15cd5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="15cd5-119">Requirement</span></span> | <span data-ttu-id="15cd5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="15cd5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15cd5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15cd5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15cd5-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15cd5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="15cd5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15cd5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15cd5-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15cd5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="15cd5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15cd5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15cd5-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15cd5-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15cd5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="15cd5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15cd5-128">Log de cliente</span><span class="sxs-lookup"><span data-stu-id="15cd5-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="15cd5-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15cd5-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="15cd5-130">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15cd5-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




