---
description: Especifica a entrada atual na caixa de descrição de exemplo para um tipo de mídia MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: Atributo MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751579"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>\_Atributo de \_ \_ entrada de \_ exemplo atual do MF MT MPEG4 \_

Especifica a entrada atual na caixa de descrição de exemplo para um tipo de mídia MPEG-4.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Em um arquivo MP4 ou 3GP, a caixa Descrição de exemplo descreve a codificação usada para um fluxo no arquivo. A caixa Descrição de exemplo pode conter várias entradas. Esse atributo especifica qual entrada usar. O valor é um índice de base zero na lista.

Atualmente, o único valor com suporte é 0. O atributo foi definido para extensibilidade futura.

A origem do arquivo MPEG-4 sempre define o valor como 0. Os coletores de arquivos MP4 e 3GP ignoram o valor desse atributo se ele estiver presente.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[\_Descrição de \_ exemplo de MPEG4 \_ \_ do MF MT](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




