---
description: Especifica o nome de exibição de um dispositivo.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: Atributo MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab0d2bb3c0e75d547e1249a83261b7c804743ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763849"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a><span data-ttu-id="b877f-103">\_Atributo de \_ \_ nome amigável do atributo MF DEVSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="b877f-103">MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME attribute</span></span>

<span data-ttu-id="b877f-104">Especifica o nome de exibição de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b877f-104">Specifies the display name for a device.</span></span> <span data-ttu-id="b877f-105">O *nome de exibição* é uma cadeia de caracteres legível, adequada para exibição em uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b877f-105">The *display name* is a human-readable string, suitable for display in a user interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="b877f-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b877f-106">Data type</span></span>

<span data-ttu-id="b877f-107">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b877f-107">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="b877f-108">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b877f-108">Get/set</span></span>

<span data-ttu-id="b877f-109">Para obter esse atributo, chame [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="b877f-109">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b877f-110">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="b877f-110">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="b877f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b877f-111">Remarks</span></span>

<span data-ttu-id="b877f-112">Esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="b877f-112">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="b877f-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="b877f-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="b877f-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="b877f-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="b877f-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b877f-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b877f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b877f-116">Requirements</span></span>



| <span data-ttu-id="b877f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b877f-117">Requirement</span></span> | <span data-ttu-id="b877f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b877f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b877f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b877f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b877f-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b877f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b877f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b877f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b877f-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b877f-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b877f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b877f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b877f-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b877f-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b877f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b877f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b877f-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b877f-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b877f-127">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="b877f-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="b877f-128">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b877f-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




