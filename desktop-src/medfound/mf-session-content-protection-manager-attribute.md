---
description: Fornece uma interface de retorno de chamada para que o aplicativo receba um objeto de habilitação de conteúdo da sessão do caminho de mídia protegido (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: Atributo MF_SESSION_CONTENT_PROTECTION_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788708"
---
# <a name="mf_session_content_protection_manager-attribute"></a><span data-ttu-id="3f129-103">\_ \_ \_ Atributo Gerenciador de proteção de conteúdo de sessão MF \_</span><span class="sxs-lookup"><span data-stu-id="3f129-103">MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="3f129-104">Fornece uma interface de retorno de chamada para que o aplicativo receba um objeto de habilitação de conteúdo da sessão do caminho de mídia protegido (PMP).</span><span class="sxs-lookup"><span data-stu-id="3f129-104">Provides a callback interface for the application to receive a content enabler object from the protected media path (PMP) session.</span></span>

## <a name="data-type"></a><span data-ttu-id="3f129-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3f129-105">Data type</span></span>

<span data-ttu-id="3f129-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="3f129-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="3f129-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f129-107">Remarks</span></span>

<span data-ttu-id="3f129-108">O valor desse atributo é um ponteiro para a interface [_ *IMFContentProtectionManager* \*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3f129-108">The value of this attribute is a pointer to the application's [_ *IMFContentProtectionManager*\*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="3f129-109">Defina esse atributo na sessão do PMP usando o parâmetro *pConfiguration* da função [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="3f129-109">Set this attribute on the PMP session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="3f129-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3f129-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f129-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f129-111">Requirements</span></span>



| <span data-ttu-id="3f129-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f129-112">Requirement</span></span> | <span data-ttu-id="3f129-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3f129-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f129-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f129-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3f129-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f129-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3f129-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f129-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3f129-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f129-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3f129-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f129-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f129-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f129-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f129-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f129-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f129-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f129-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3f129-122">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="3f129-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="3f129-123">**IMFAttributes:: setunknown**</span><span class="sxs-lookup"><span data-stu-id="3f129-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="3f129-124">Atributos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="3f129-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="3f129-125">Como reproduzir arquivos de mídia protegidos</span><span class="sxs-lookup"><span data-stu-id="3f129-125">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




