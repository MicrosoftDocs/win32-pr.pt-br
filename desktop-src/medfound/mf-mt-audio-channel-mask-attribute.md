---
description: Em um tipo de mídia de áudio, especifica a atribuição de canais de áudio para as posições do orador.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: Atributo MF_MT_AUDIO_CHANNEL_MASK (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5293f5387a2c293b97ee32db54fcfb3f3ff304d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010714"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a><span data-ttu-id="1201c-103">\_Atributo de \_ máscara de canal de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="1201c-103">MF\_MT\_AUDIO\_CHANNEL\_MASK attribute</span></span>

<span data-ttu-id="1201c-104">Em um tipo de mídia de áudio, especifica a atribuição de canais de áudio para as posições do orador.</span><span class="sxs-lookup"><span data-stu-id="1201c-104">In an audio media type, specifies the assignment of audio channels to speaker positions.</span></span>

## <a name="data-type"></a><span data-ttu-id="1201c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1201c-105">Data type</span></span>

<span data-ttu-id="1201c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1201c-106">**UINT32**</span></span>

<span data-ttu-id="1201c-107">O valor desse atributo é uma operação bit a bit **ou** dos sinalizadores a seguir, que são definidos no arquivo de cabeçalho Mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="1201c-107">The value of this attribute is a bitwise **OR** of the following flags, which are defined in the header file mmreg.h.</span></span>

<dl> <dt>

<span data-ttu-id="1201c-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**Palestrante \_ FRONTAL \_ esquerdo** (0x1)</span><span class="sxs-lookup"><span data-stu-id="1201c-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**SPEAKER\_FRONT\_LEFT** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**Palestrante \_ FRONTAL \_ direito** (0x2)</span><span class="sxs-lookup"><span data-stu-id="1201c-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**SPEAKER\_FRONT\_RIGHT** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**Palestrante \_ FRONT \_ Center** (0x4)</span><span class="sxs-lookup"><span data-stu-id="1201c-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**SPEAKER\_FRONT\_CENTER** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**Palestrante \_ BAIXA \_ frequência** (0x8)</span><span class="sxs-lookup"><span data-stu-id="1201c-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**SPEAKER\_LOW\_FREQUENCY** (0x8)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**Palestrante \_ VOLTAR \_ à esquerda** (0x10)</span><span class="sxs-lookup"><span data-stu-id="1201c-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**SPEAKER\_BACK\_LEFT** (0x10)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**Palestrante \_ VOLTAR \_ à direita** (0x20)</span><span class="sxs-lookup"><span data-stu-id="1201c-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**SPEAKER\_BACK\_RIGHT** (0x20)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**Palestrante \_ FRONTAL \_ à esquerda \_ do \_ Centro** (0x40)</span><span class="sxs-lookup"><span data-stu-id="1201c-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**SPEAKER\_FRONT\_LEFT\_OF\_CENTER** (0x40)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**Palestrante \_ FRONTAL \_ direita \_ do \_ Centro** (0x80)</span><span class="sxs-lookup"><span data-stu-id="1201c-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**SPEAKER\_FRONT\_RIGHT\_OF\_CENTER** (0x80)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**Palestrante \_ BACK \_ Center** (0x100)</span><span class="sxs-lookup"><span data-stu-id="1201c-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**SPEAKER\_BACK\_CENTER** (0x100)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**Palestrante \_ LATERAL \_ esquerda** (0x200)</span><span class="sxs-lookup"><span data-stu-id="1201c-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**SPEAKER\_SIDE\_LEFT** (0x200)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**Palestrante \_ LATERAL \_ direita** (0x400)</span><span class="sxs-lookup"><span data-stu-id="1201c-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**SPEAKER\_SIDE\_RIGHT** (0x400)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**Palestrante \_ SUPERIOR \_ central** (0x800)</span><span class="sxs-lookup"><span data-stu-id="1201c-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**SPEAKER\_TOP\_CENTER** (0x800)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**Palestrante \_ SUPERIOR \_ frontal \_ esquerdo** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="1201c-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**SPEAKER\_TOP\_FRONT\_LEFT** (0x1000)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**Palestrante \_ SUPERIOR \_ frontal \_ central** (0x2000)</span><span class="sxs-lookup"><span data-stu-id="1201c-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**SPEAKER\_TOP\_FRONT\_CENTER** (0x2000)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**Palestrante \_ SUPERIOR \_ frontal \_ direita** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="1201c-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**SPEAKER\_TOP\_FRONT\_RIGHT** (0x4000)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**Palestrante \_ SUPERIOR \_ \_ esquerdo posterior** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="1201c-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**SPEAKER\_TOP\_BACK\_LEFT** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**Palestrante \_ SUPERIOR \_ \_ central** (0x10000)</span><span class="sxs-lookup"><span data-stu-id="1201c-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**SPEAKER\_TOP\_BACK\_CENTER** (0x10000)</span></span>
</dt> <dt>

<span data-ttu-id="1201c-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**Palestrante \_ SUPERIOR \_ \_ direito** (0x20000)</span><span class="sxs-lookup"><span data-stu-id="1201c-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**SPEAKER\_TOP\_BACK\_RIGHT** (0x20000)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1201c-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1201c-126">Remarks</span></span>

<span data-ttu-id="1201c-127">Esse atributo corresponde ao membro **dwChannelMask** da estrutura [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="1201c-127">This attribute corresponds to the **dwChannelMask** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="1201c-128">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1201c-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1201c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1201c-129">Requirements</span></span>



| <span data-ttu-id="1201c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1201c-130">Requirement</span></span> | <span data-ttu-id="1201c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1201c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1201c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1201c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1201c-133">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="1201c-133">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1201c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1201c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1201c-135">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1201c-135">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1201c-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1201c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1201c-137"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1201c-137"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1201c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1201c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1201c-139">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1201c-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1201c-140">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1201c-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1201c-141">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="1201c-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1201c-142">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1201c-142">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1201c-143">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="1201c-143">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
