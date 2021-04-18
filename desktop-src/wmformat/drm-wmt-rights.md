---
title: Enumeração de WMT_RIGHTS (wmdrmsdk. h)
description: Define os direitos que podem ser especificados em uma licença DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- Formato de mídia do Windows de enumeração de WMT_RIGHTS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760650"
---
# <a name="wmt_rights-enumeration"></a><span data-ttu-id="92486-105">Enumeração de direitos de WMT \_</span><span class="sxs-lookup"><span data-stu-id="92486-105">WMT\_RIGHTS enumeration</span></span>

<span data-ttu-id="92486-106">O tipo de enumeração **\_ direitos WMT** define os direitos que podem ser especificados em uma licença DRM.</span><span class="sxs-lookup"><span data-stu-id="92486-106">The **WMT\_RIGHTS** enumeration type defines the rights that may be specified in a DRM license.</span></span>

## <a name="syntax"></a><span data-ttu-id="92486-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="92486-107">Syntax</span></span>


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a><span data-ttu-id="92486-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="92486-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="92486-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**reprodução da WMT \_ direita \_**</span><span class="sxs-lookup"><span data-stu-id="92486-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT\_RIGHT\_PLAYBACK**</span></span>
</dt> <dd>

<span data-ttu-id="92486-110">Especifica o direito de reproduzir conteúdo sem restrição.</span><span class="sxs-lookup"><span data-stu-id="92486-110">Specifies the right to play content without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="92486-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**\_cópia do WMT Right \_ \_ para \_ \_ dispositivo não SDMI \_**</span><span class="sxs-lookup"><span data-stu-id="92486-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="92486-112">Especifica o direito de copiar o conteúdo para um dispositivo não compatível com a SDMI (iniciativa de música digital) segura.</span><span class="sxs-lookup"><span data-stu-id="92486-112">Specifies the right to copy content to a device not compliant with the Secure Digital Music Initiative (SDMI).</span></span>

</dd> <dt>

<span data-ttu-id="92486-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT \_ à direita \_ copiar \_ para \_ CD**</span><span class="sxs-lookup"><span data-stu-id="92486-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT\_RIGHT\_COPY\_TO\_CD**</span></span>
</dt> <dd>

<span data-ttu-id="92486-114">Especifica o direito de copiar o conteúdo para um CD.</span><span class="sxs-lookup"><span data-stu-id="92486-114">Specifies the right to copy content to a CD.</span></span>

</dd> <dt>

<span data-ttu-id="92486-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT \_ direita \_ copiar \_ para \_ \_ dispositivo SDMI**</span><span class="sxs-lookup"><span data-stu-id="92486-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="92486-116">Especifica o direito de copiar o conteúdo para um dispositivo compatível com o SDMI.</span><span class="sxs-lookup"><span data-stu-id="92486-116">Specifies the right to copy content to a device compliant with the SDMI.</span></span>

</dd> <dt>

<span data-ttu-id="92486-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ \_ uma \_ vez à direita**</span><span class="sxs-lookup"><span data-stu-id="92486-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT\_RIGHT\_ONE\_TIME**</span></span>
</dt> <dd>

<span data-ttu-id="92486-118">Especifica o direito de reprodução de conteúdo apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="92486-118">Specifies the right to play content one time only.</span></span>

</dd> <dt>

<span data-ttu-id="92486-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ direito \_ Salvar \_ fluxo \_ protegido**</span><span class="sxs-lookup"><span data-stu-id="92486-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT\_RIGHT\_SAVE\_STREAM\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="92486-120">Especifica o direito de salvar o conteúdo de um servidor.</span><span class="sxs-lookup"><span data-stu-id="92486-120">Specifies the right to save content from a server.</span></span>

</dd> <dt>

<span data-ttu-id="92486-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT \_ a \_ cópia direita**</span><span class="sxs-lookup"><span data-stu-id="92486-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT\_RIGHT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="92486-122">Especifica o direito de copiar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="92486-122">Specifies the right to copy content.</span></span> <span data-ttu-id="92486-123">O Windows Media DRM 10 regula os dispositivos nos quais o conteúdo pode ser copiado usando os níveis de proteção de saída (OPLs).</span><span class="sxs-lookup"><span data-stu-id="92486-123">Windows Media DRM 10 regulates the devices to which the content can be copied by using output protection levels (OPLs).</span></span>

</dd> <dt>

<span data-ttu-id="92486-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ de \_ colaboração à \_ direita**</span><span class="sxs-lookup"><span data-stu-id="92486-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT\_RIGHT\_COLLABORATIVE\_PLAY**</span></span>
</dt> <dd>

<span data-ttu-id="92486-125">Especifica o direito de reproduzir conteúdo como parte de um cenário online em que vários participantes podem contribuir com músicas de sua coleção para uma lista de reprodução compartilhada.</span><span class="sxs-lookup"><span data-stu-id="92486-125">Specifies the right to play content as part of an online scenario where multiple participants can contribute songs from their collection to a shared playlist.</span></span>

</dd> <dt>

<span data-ttu-id="92486-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**\_gatilho WMT direito de \_ SDMI \_**</span><span class="sxs-lookup"><span data-stu-id="92486-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT\_RIGHT\_SDMI\_TRIGGER**</span></span>
</dt> <dd>

<span data-ttu-id="92486-127">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="92486-127">Reserved for future use.</span></span> <span data-ttu-id="92486-128">Não use.</span><span class="sxs-lookup"><span data-stu-id="92486-128">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="92486-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ direito de \_ SDMI \_ NOMORECOPIES**</span><span class="sxs-lookup"><span data-stu-id="92486-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT\_RIGHT\_SDMI\_NOMORECOPIES**</span></span>
</dt> <dd>

<span data-ttu-id="92486-130">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="92486-130">Reserved for future use.</span></span> <span data-ttu-id="92486-131">Não use.</span><span class="sxs-lookup"><span data-stu-id="92486-131">Do not use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92486-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="92486-132">Remarks</span></span>

<span data-ttu-id="92486-133">Esses valores são sinalizadores de bits, de modo que um ou mais podem ser definidos combinando-os com **o operador OR** .</span><span class="sxs-lookup"><span data-stu-id="92486-133">These values are bit flags, so one or more can be set by combining them with the bitwise **OR** operator.</span></span>

<span data-ttu-id="92486-134">Ao usar o Windows Media DRM 10, o **WMT \_ Right \_ Copie \_ para um \_ \_ \_ dispositivo não SDMI**, **\_ a cópia do WMT Right \_ para o \_ \_ \_ dispositivo SDMI** e **\_ a cópia do WMT à direita \_ para o \_ \_ CD** são substituídas pela **cópia de WMT \_ à direita \_**.</span><span class="sxs-lookup"><span data-stu-id="92486-134">When using Windows Media DRM 10, **WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**, **WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**, and **WMT\_RIGHT\_COPY\_TO\_CD** are superseded by **WMT\_RIGHT\_COPY**.</span></span> <span data-ttu-id="92486-135">As limitações nos dispositivos nos quais o conteúdo pode ser copiado são especificadas usando os níveis de proteção de saída (OPLs).</span><span class="sxs-lookup"><span data-stu-id="92486-135">Limitations on the devices to which the content may be copied are specified by using output protection levels (OPLs).</span></span>

## <a name="requirements"></a><span data-ttu-id="92486-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92486-136">Requirements</span></span>



| <span data-ttu-id="92486-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="92486-137">Requirement</span></span> | <span data-ttu-id="92486-138">Valor</span><span class="sxs-lookup"><span data-stu-id="92486-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92486-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92486-139">Header</span></span><br/> | <dl> <span data-ttu-id="92486-140"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="92486-140"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92486-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="92486-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92486-142">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="92486-142">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





