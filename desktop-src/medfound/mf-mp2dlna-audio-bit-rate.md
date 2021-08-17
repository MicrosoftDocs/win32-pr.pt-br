---
description: Especifica a taxa máxima de bits de áudio para o coletor de mídia DLNA (rede de vida digital).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: Atributo MF_MP2DLNA_AUDIO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed622a2f826e061dc4b909eec09490974fe83a7ac850cd0fcdfcede0abd578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104762"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a>\_Atributo de \_ taxa de bits de áudio MF MP2DLNA \_ \_

Especifica a taxa máxima de bits de áudio para o coletor de mídia DLNA (rede de vida digital).

## <a name="data-type"></a>Tipo de dados

**UINT32**

O valor é a taxa de bits máxima de destino para o fluxo de áudio codificado, em bits por segundo. O valor deve ser uma das taxas de bits permitidas para áudio MPEG-2 Layer 2 para DLNA. O valor padrão é 192000 (192 kbps).

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Para definir esse atributo no coletor de mídia DLNA, consulte o coletor de mídia para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Defina o atributo antes de o streaming começar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




