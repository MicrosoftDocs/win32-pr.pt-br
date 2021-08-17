---
description: Especifica a entrada atual na caixa de descrição de exemplo para um tipo de mídia MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660f74c1f9335556b514607cc2100f7ef59a00fba84f6cfe90412b91e1ff500a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877030"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>Atributo \_ MT \_ MPEG4 \_ CURRENT SAMPLE \_ \_ ENTRY

Especifica a entrada atual na caixa de descrição de exemplo para um tipo de mídia MPEG-4.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Em um arquivo MP4 ou 3GP, a caixa de descrição de exemplo descreve a codificação usada para um fluxo no arquivo. A caixa de descrição de exemplo pode conter várias entradas. Esse atributo especifica qual entrada usar. O valor é um índice baseado em zero na lista.

Atualmente, o único valor com suporte é 0. O atributo foi definido para extensibilidade futura.

A origem do arquivo MPEG-4 sempre define o valor como 0. Os sinks de arquivo MP4 e 3GP ignorarão o valor desse atributo se ele estiver presente.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[MF \_ MT \_ MPEG4 \_ SAMPLE \_ DESCRIPTION](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




