---
description: O valor do campo &\# 0034; c-hostexe&\# 0034; que a fonte de rede usa para o registro em log.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: Propriedade MFNETSOURCE_HOSTEXE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ac786fe08ede556537703d2eb886b30be39207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663013"
---
# <a name="mfnetsource_hostexe-property"></a><span data-ttu-id="84f7c-103">\_Propriedade MFNETSOURCE HOSTEXE</span><span class="sxs-lookup"><span data-stu-id="84f7c-103">MFNETSOURCE\_HOSTEXE property</span></span>

<span data-ttu-id="84f7c-104">O valor do campo "c-hostexe" usado pela fonte de rede para registro em log.</span><span class="sxs-lookup"><span data-stu-id="84f7c-104">The value of the "c-hostexe" field that the network source uses for logging.</span></span> <span data-ttu-id="84f7c-105">Os aplicativos podem definir essa propriedade como o nome do aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="84f7c-105">Applications can set this property to the name of the host application.</span></span> <span data-ttu-id="84f7c-106">Por exemplo, o valor pode ser "iexplore.exe" se o aplicativo estiver hospedado em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="84f7c-106">For example, the value could be "iexplore.exe" if the application is hosted in a webpage.</span></span>



<span data-ttu-id="84f7c-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="84f7c-107">Data type</span></span>

<span data-ttu-id="84f7c-108">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="84f7c-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="84f7c-109">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="84f7c-109">PROPVARIANT member</span></span>

<span data-ttu-id="84f7c-110">Cadeia de caracteres largos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="84f7c-110">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="84f7c-111">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="84f7c-111">VT\_LPWSTR</span></span>

<span data-ttu-id="84f7c-112">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="84f7c-112">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="84f7c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="84f7c-113">Remarks</span></span>

<span data-ttu-id="84f7c-114">A constante **MFNETSOURCE \_ HOSTEXE** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="84f7c-114">The constant **MFNETSOURCE\_HOSTEXE** defines the GUID for this property key.</span></span> <span data-ttu-id="84f7c-115">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="84f7c-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="84f7c-116">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="84f7c-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="84f7c-117">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="84f7c-117">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="84f7c-118">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="84f7c-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84f7c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84f7c-119">Requirements</span></span>



| <span data-ttu-id="84f7c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f7c-120">Requirement</span></span> | <span data-ttu-id="84f7c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="84f7c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84f7c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84f7c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="84f7c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84f7c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="84f7c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84f7c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="84f7c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84f7c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="84f7c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84f7c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f7c-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84f7c-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f7c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="84f7c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f7c-129">Log de cliente</span><span class="sxs-lookup"><span data-stu-id="84f7c-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="84f7c-130">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84f7c-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="84f7c-131">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84f7c-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




