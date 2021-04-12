---
description: Contém o nome de um fluxo.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: Atributo MF_SD_STREAM_NAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297473"
---
# <a name="mf_sd_stream_name-attribute"></a><span data-ttu-id="c45d6-103">\_Atributo de \_ nome de fluxo SD MF \_</span><span class="sxs-lookup"><span data-stu-id="c45d6-103">MF\_SD\_STREAM\_NAME attribute</span></span>

<span data-ttu-id="c45d6-104">Contém o nome de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="c45d6-104">Contains the name of a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c45d6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c45d6-105">Data type</span></span>

<span data-ttu-id="c45d6-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="c45d6-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="c45d6-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="c45d6-107">Get/set</span></span>

<span data-ttu-id="c45d6-108">Para obter esse atributo, chame [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="c45d6-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="c45d6-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="c45d6-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c45d6-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c45d6-110">Applies to</span></span>

[<span data-ttu-id="c45d6-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c45d6-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="c45d6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c45d6-112">Remarks</span></span>

<span data-ttu-id="c45d6-113">A fonte de mídia AVI define esse atributo se o arquivo AVI contiver um bloco ' strn '.</span><span class="sxs-lookup"><span data-stu-id="c45d6-113">The AVI media source sets this attribute if the AVI file contains a 'strn' chunk.</span></span>

<span data-ttu-id="c45d6-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c45d6-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c45d6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c45d6-115">Requirements</span></span>



| <span data-ttu-id="c45d6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c45d6-116">Requirement</span></span> | <span data-ttu-id="c45d6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c45d6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c45d6-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c45d6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c45d6-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c45d6-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c45d6-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c45d6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c45d6-121">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="c45d6-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c45d6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c45d6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c45d6-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c45d6-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c45d6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c45d6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45d6-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c45d6-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c45d6-126">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="c45d6-126">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




