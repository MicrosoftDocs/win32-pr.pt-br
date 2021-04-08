---
description: O valor do &\# 0034; cs (referente) &\# 0034; campo que a fonte de rede usa para registro em log.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: Propriedade MFNETSOURCE_BROWSERWEBPAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e8222761299cad229b692ef400f69d0968ebd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921121"
---
# <a name="mfnetsource_browserwebpage-property"></a><span data-ttu-id="67665-103">\_Propriedade MFNETSOURCE BROWSERWEBPAGE</span><span class="sxs-lookup"><span data-stu-id="67665-103">MFNETSOURCE\_BROWSERWEBPAGE property</span></span>

<span data-ttu-id="67665-104">O valor do campo "cs (referenciador)" que a fonte de rede usa para registro em log.</span><span class="sxs-lookup"><span data-stu-id="67665-104">The value of the "cs(Referer)" field that the network source uses for logging.</span></span> <span data-ttu-id="67665-105">Os aplicativos podem definir essa propriedade como a URL da página da Web na qual o aplicativo foi incorporado.</span><span class="sxs-lookup"><span data-stu-id="67665-105">Applications can set this property to the URL of the webpage in which the application was embedded.</span></span>



<span data-ttu-id="67665-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="67665-106">Data type</span></span>

<span data-ttu-id="67665-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="67665-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="67665-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="67665-108">PROPVARIANT member</span></span>

<span data-ttu-id="67665-109">Cadeia de caracteres largos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="67665-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="67665-110">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="67665-110">VT\_LPWSTR</span></span>

<span data-ttu-id="67665-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="67665-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="67665-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="67665-112">Remarks</span></span>

<span data-ttu-id="67665-113">A constante **MFNETSOURCE \_ BROWSERWEBPAGE** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="67665-113">The constant **MFNETSOURCE\_BROWSERWEBPAGE** defines the GUID for this property key.</span></span> <span data-ttu-id="67665-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="67665-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="67665-115">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="67665-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="67665-116">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="67665-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="67665-117">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="67665-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67665-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67665-118">Requirements</span></span>



| <span data-ttu-id="67665-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="67665-119">Requirement</span></span> | <span data-ttu-id="67665-120">Valor</span><span class="sxs-lookup"><span data-stu-id="67665-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67665-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67665-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67665-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67665-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67665-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67665-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67665-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67665-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="67665-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67665-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="67665-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="67665-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67665-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="67665-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67665-128">Log de cliente</span><span class="sxs-lookup"><span data-stu-id="67665-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="67665-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67665-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="67665-130">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67665-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




