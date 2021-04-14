---
description: Armazena a cadeia de caracteres enviada no cabeçalho de Accept-Language.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: Propriedade MFNETSOURCE_STREAM_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200c49d4a14146277c66fbb3389cf1ba6ab13fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370518"
---
# <a name="mfnetsource_stream_language-property"></a><span data-ttu-id="8d051-103">Propriedade de linguagem de \_ fluxo MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="8d051-103">MFNETSOURCE\_STREAM\_LANGUAGE property</span></span>

<span data-ttu-id="8d051-104">Armazena a cadeia de caracteres enviada no cabeçalho de Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="8d051-104">Stores the string sent in the Accept-Language header.</span></span>



<span data-ttu-id="8d051-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8d051-105">Data type</span></span>

<span data-ttu-id="8d051-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8d051-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8d051-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8d051-107">PROPVARIANT member</span></span>

<span data-ttu-id="8d051-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="8d051-108">\**WCHAR\** _</span></span>

<span data-ttu-id="8d051-109">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="8d051-109">VT\_LPWSTR</span></span>

<span data-ttu-id="8d051-110">_ *pwszVal*\*</span><span class="sxs-lookup"><span data-stu-id="8d051-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="8d051-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d051-111">Remarks</span></span>

<span data-ttu-id="8d051-112">A \_ constante de linguagem de fluxo MFNETSOURCE \_ define o GUID da chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="8d051-112">The MFNETSOURCE\_STREAM\_LANGUAGE constant defines the GUID for the property key.</span></span> <span data-ttu-id="8d051-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="8d051-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="8d051-114">Para definir essa propriedade na fonte de rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="8d051-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="8d051-115">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="8d051-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d051-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d051-116">Requirements</span></span>



| <span data-ttu-id="8d051-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d051-117">Requirement</span></span> | <span data-ttu-id="8d051-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8d051-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d051-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d051-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d051-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8d051-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8d051-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d051-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d051-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8d051-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8d051-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d051-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d051-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d051-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d051-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d051-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d051-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8d051-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8d051-127">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8d051-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




