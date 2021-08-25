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
ms.openlocfilehash: 3a48c9ce3a276f060ac90dd15100ca8612e35116e124588e27f4ee36c1a0b8a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930736"
---
# <a name="wmt_rights-enumeration"></a>Enumeração de direitos de WMT \_

O tipo de enumeração **\_ direitos WMT** define os direitos que podem ser especificados em uma licença DRM.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**reprodução da WMT \_ direita \_**
</dt> <dd>

Especifica o direito de reproduzir conteúdo sem restrição.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**\_cópia do WMT Right \_ \_ para \_ \_ dispositivo não SDMI \_**
</dt> <dd>

Especifica o direito de copiar o conteúdo para um dispositivo não compatível com a SDMI (iniciativa de música digital) segura.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT \_ à direita \_ copiar \_ para \_ CD**
</dt> <dd>

Especifica o direito de copiar o conteúdo para um CD.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT \_ direita \_ copiar \_ para \_ \_ dispositivo SDMI**
</dt> <dd>

Especifica o direito de copiar o conteúdo para um dispositivo compatível com o SDMI.

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ \_ uma \_ vez à direita**
</dt> <dd>

Especifica o direito de reprodução de conteúdo apenas uma vez.

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ direito \_ Salvar \_ fluxo \_ protegido**
</dt> <dd>

Especifica o direito de salvar o conteúdo de um servidor.

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT \_ a \_ cópia direita**
</dt> <dd>

Especifica o direito de copiar o conteúdo. Windows O DRM 10 de mídia regula os dispositivos nos quais o conteúdo pode ser copiado usando os níveis de proteção de saída (OPLs).

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ de \_ colaboração à \_ direita**
</dt> <dd>

Especifica o direito de reproduzir conteúdo como parte de um cenário online em que vários participantes podem contribuir com músicas de sua coleção para uma lista de reprodução compartilhada.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**\_gatilho WMT direito de \_ SDMI \_**
</dt> <dd>

Reservado para uso futuro. Não use.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ direito de \_ SDMI \_ NOMORECOPIES**
</dt> <dd>

Reservado para uso futuro. Não use.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses valores são sinalizadores de bits, de modo que um ou mais podem ser definidos combinando-os com **o operador OR** .

ao usar Windows mídia DRM 10, **WMT \_ à \_ direita \_ copiar \_ para \_ \_ dispositivo não SDMI**, **WMT \_ à direita \_ copiar \_ para \_ \_ dispositivo SDMI** e **WMT \_ a cópia à direita \_ \_ para \_ CD** são substituídas pela **cópia de WMT \_ à direita \_**. As limitações nos dispositivos nos quais o conteúdo pode ser copiado são especificadas usando os níveis de proteção de saída (OPLs).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> </dl>

 

 





