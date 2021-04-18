---
description: Especifica o número máximo de amostras de PCM adicionais que podem ser retornadas ao final de após a decodificação de um arquivo.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: Propriedade MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793927"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>\_Propriedade MaxNumPCMSamplesWithPaddedSilence do decodificador MFPKEY \_

Especifica o número máximo de amostras de PCM adicionais que podem ser retornadas ao final de após a decodificação de um arquivo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

2.048

## <a name="remarks"></a>Comentários

Essa propriedade pode ser usada para estimar o silêncio artificial que é inserido entre as músicas à medida que elas são alimentadas no decodificador, uma após a outra.

Para os decodificadores de áudio do Windows Media 10 Professional e Windows Media 9 sem perdas, essa propriedade é sempre igual a 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
