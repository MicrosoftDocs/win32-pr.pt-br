---
description: O valor da primeira parte do &\# 0034; cs (User-Agent) &\# 0034; campo que a fonte de rede usa para registro em log.
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: Propriedade MFNETSOURCE_BROWSERUSERAGENT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cbb4dcd5558c59da20e75209529c16fc0c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502100"
---
# <a name="mfnetsource_browseruseragent-property"></a><span data-ttu-id="bd656-103">\_Propriedade MFNETSOURCE BROWSERUSERAGENT</span><span class="sxs-lookup"><span data-stu-id="bd656-103">MFNETSOURCE\_BROWSERUSERAGENT property</span></span>

<span data-ttu-id="bd656-104">O valor da primeira parte do campo "cs (User-Agent)" que a fonte de rede usa para o registro em log.</span><span class="sxs-lookup"><span data-stu-id="bd656-104">The value of the first portion of the "cs(User-Agent)" field that the network source uses for logging.</span></span> <span data-ttu-id="bd656-105">Os aplicativos podem definir essa propriedade como qualquer valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bd656-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="bd656-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bd656-106">Data type</span></span>

<span data-ttu-id="bd656-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="bd656-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bd656-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="bd656-108">PROPVARIANT member</span></span>

<span data-ttu-id="bd656-109">Cadeia de caracteres largos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="bd656-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="bd656-110">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="bd656-110">VT\_LPWSTR</span></span>

<span data-ttu-id="bd656-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="bd656-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="bd656-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd656-112">Remarks</span></span>

<span data-ttu-id="bd656-113">A constante **MFNETSOURCE \_ BROWSERUSERAGENT** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bd656-113">The constant **MFNETSOURCE\_BROWSERUSERAGENT** defines the GUID for this property key.</span></span> <span data-ttu-id="bd656-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="bd656-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="bd656-115">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="bd656-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="bd656-116">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="bd656-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="bd656-117">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="bd656-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd656-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd656-118">Requirements</span></span>



| <span data-ttu-id="bd656-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd656-119">Requirement</span></span> | <span data-ttu-id="bd656-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bd656-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd656-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd656-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bd656-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd656-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bd656-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd656-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bd656-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd656-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bd656-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd656-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd656-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd656-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd656-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd656-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd656-128">Log de cliente</span><span class="sxs-lookup"><span data-stu-id="bd656-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="bd656-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd656-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="bd656-130">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd656-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="bd656-131">**MFNETSOURCE \_ PLAYERUSERAGENT**</span><span class="sxs-lookup"><span data-stu-id="bd656-131">**MFNETSOURCE\_PLAYERUSERAGENT**</span></span>](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




