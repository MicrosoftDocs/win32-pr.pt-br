---
description: Contém o CLSID de um Gerenciador de qualidade para a sessão de mídia.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: Atributo MF_SESSION_QUALITY_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296980"
---
# <a name="mf_session_quality_manager-attribute"></a><span data-ttu-id="a58b2-103">\_Atributo do \_ Gerenciador de qualidade de sessão MF \_</span><span class="sxs-lookup"><span data-stu-id="a58b2-103">MF\_SESSION\_QUALITY\_MANAGER attribute</span></span>

<span data-ttu-id="a58b2-104">Contém o CLSID de um Gerenciador de qualidade para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="a58b2-104">Contains the CLSID of a quality manager for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="a58b2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a58b2-105">Data type</span></span>

<span data-ttu-id="a58b2-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a58b2-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a58b2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a58b2-107">Remarks</span></span>

<span data-ttu-id="a58b2-108">Você pode usar esse atributo para fornecer um Gerenciador de qualidade personalizado para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="a58b2-108">You can use this attribute to provide a custom quality manager for the Media Session.</span></span>

<span data-ttu-id="a58b2-109">Defina esse atributo usando o parâmetro *pConfiguration* da função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="a58b2-109">Set this attribute by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="a58b2-110">Se esse atributo for definido, a sessão de mídia chamará **CoCreateInstance** com o CLSID especificado para criar o Gerenciador de qualidade.</span><span class="sxs-lookup"><span data-stu-id="a58b2-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID to create the quality manager.</span></span> <span data-ttu-id="a58b2-111">O objeto criado por esse CLSID deve expor a interface [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .</span><span class="sxs-lookup"><span data-stu-id="a58b2-111">The object created by this CLSID must expose the [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) interface.</span></span>

<span data-ttu-id="a58b2-112">Se esse atributo não for definido, a sessão de mídia criará o Gerenciador de qualidade padrão fornecido no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a58b2-112">If this attribute is not set, the Media Session creates the default quality manager provided in Media Foundation.</span></span>

<span data-ttu-id="a58b2-113">Se você quiser executar a sessão de mídia sem nenhum Gerenciador de qualidade, defina este atributo como **GUID \_ NULL**.</span><span class="sxs-lookup"><span data-stu-id="a58b2-113">If you want to run the Media Session with no quality manager at all, set this attribute to **GUID\_NULL**.</span></span>

<span data-ttu-id="a58b2-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a58b2-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a58b2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a58b2-115">Requirements</span></span>



| <span data-ttu-id="a58b2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a58b2-116">Requirement</span></span> | <span data-ttu-id="a58b2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a58b2-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a58b2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a58b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a58b2-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a58b2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a58b2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a58b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a58b2-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a58b2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a58b2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a58b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a58b2-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a58b2-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a58b2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a58b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a58b2-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a58b2-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a58b2-126">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="a58b2-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a58b2-127">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="a58b2-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a58b2-128">Atributos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="a58b2-128">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




