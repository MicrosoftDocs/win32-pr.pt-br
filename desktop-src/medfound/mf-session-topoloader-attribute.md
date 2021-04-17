---
description: Contém o CLSID de um carregador de topologia para a sessão de mídia.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: Atributo MF_SESSION_TOPOLOADER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787663"
---
# <a name="mf_session_topoloader-attribute"></a><span data-ttu-id="b7045-103">\_Atributo TOPOLOADER da sessão MF \_</span><span class="sxs-lookup"><span data-stu-id="b7045-103">MF\_SESSION\_TOPOLOADER attribute</span></span>

<span data-ttu-id="b7045-104">Contém o CLSID de um carregador de topologia para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="b7045-104">Contains the CLSID of a topology loader for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="b7045-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b7045-105">Data type</span></span>

<span data-ttu-id="b7045-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b7045-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b7045-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7045-107">Remarks</span></span>

<span data-ttu-id="b7045-108">Você pode usar esse atributo para fornecer um carregador de topologia personalizado para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="b7045-108">You can use this attribute to provide a custom topology loader for the Media Session.</span></span>

<span data-ttu-id="b7045-109">Defina esse atributo usando o parâmetro *pConfiguration* da função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou a função [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="b7045-109">Set this attribute using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function or the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="b7045-110">Se esse atributo for definido, a sessão de mídia chamará **CoCreateInstance** com o CLSID especificado quando ele criar o carregador de topologia.</span><span class="sxs-lookup"><span data-stu-id="b7045-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID when it creates the topology loader.</span></span> <span data-ttu-id="b7045-111">O objeto criado por esse CLSID deve expor a interface [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="b7045-111">The object created by this CLSID must expose the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="b7045-112">Se esse atributo não for definido, a sessão de mídia criará o carregador de topologia padrão fornecido no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b7045-112">If this attribute is not set, the Media Session creates the default topology loader provided in Media Foundation.</span></span>

<span data-ttu-id="b7045-113">Um carregador de topologia deve dar suporte A Apartments multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="b7045-113">A topology loader must support multithreaded apartments.</span></span> <span data-ttu-id="b7045-114">Você deve registrar o carregador de topologia como ThreadingModel = "both".</span><span class="sxs-lookup"><span data-stu-id="b7045-114">You should register the topology loader as ThreadingModel="Both".</span></span> <span data-ttu-id="b7045-115">Além disso, se você estiver usando o carregador de topologia dentro do caminho de mídia protegido (PMP), o carregador de topologia deverá ser um componente confiável.</span><span class="sxs-lookup"><span data-stu-id="b7045-115">Also, if you are using the topology loader inside the protected media path (PMP), the topology loader must be a trusted component.</span></span> <span data-ttu-id="b7045-116">Para obter mais informações, consulte [proteção de caminho de mídia](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="b7045-116">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

<span data-ttu-id="b7045-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b7045-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7045-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7045-118">Requirements</span></span>



| <span data-ttu-id="b7045-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7045-119">Requirement</span></span> | <span data-ttu-id="b7045-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b7045-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7045-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7045-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7045-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7045-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b7045-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7045-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7045-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7045-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b7045-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7045-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7045-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7045-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7045-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7045-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7045-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7045-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7045-129">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="b7045-129">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="b7045-130">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="b7045-130">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="b7045-131">Atributos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="b7045-131">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7045-132">Carregadores de topologia personalizados</span><span class="sxs-lookup"><span data-stu-id="b7045-132">Custom Topology Loaders</span></span>](custom-topology-loaders.md)
</dt> </dl>

 

 




