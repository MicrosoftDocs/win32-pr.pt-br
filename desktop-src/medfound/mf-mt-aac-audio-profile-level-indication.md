---
description: Especifica o perfil de áudio e o nível de um fluxo AAC (codificação de áudio avançado).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: Atributo MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bfc2b41cff3cbd92fc9a60be150ea598e1cc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812022"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a><span data-ttu-id="dc664-103">\_Atributo de \_ \_ indicação de \_ nível de perfil de áudio MF \_ MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="dc664-103">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION attribute</span></span>

<span data-ttu-id="dc664-104">Especifica o perfil de áudio e o nível de um fluxo AAC (codificação de áudio avançado).</span><span class="sxs-lookup"><span data-stu-id="dc664-104">Specifies the audio profile and level of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="dc664-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dc664-105">Data type</span></span>

<span data-ttu-id="dc664-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dc664-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="dc664-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="dc664-107">Get/set</span></span>

<span data-ttu-id="dc664-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="dc664-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="dc664-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="dc664-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="dc664-110">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="dc664-110">Applies To</span></span>

[<span data-ttu-id="dc664-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="dc664-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="dc664-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc664-112">Remarks</span></span>

<span data-ttu-id="dc664-113">Esse atributo contém o valor do campo **audioProfileLevelIndication** , conforme definido por ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="dc664-113">This attribute contains the value of the **audioProfileLevelIndication** field, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="dc664-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dc664-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc664-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc664-115">Requirements</span></span>



| <span data-ttu-id="dc664-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc664-116">Requirement</span></span> | <span data-ttu-id="dc664-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dc664-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc664-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc664-118">Header</span></span><br/> | <dl> <span data-ttu-id="dc664-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc664-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc664-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc664-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc664-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc664-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dc664-122">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="dc664-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




