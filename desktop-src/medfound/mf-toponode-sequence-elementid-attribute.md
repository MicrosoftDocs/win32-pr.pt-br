---
description: Especifica o elemento que contém esse nó de origem.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: MF_TOPONODE_SEQUENCE_ELEMENTID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00af7212013d26c51ecdf7d2ea4a22855f9b52524c5188d3514d34b5d6976b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739931"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>Atributo \_ ELEMENTID DE SEQUÊNCIA DE TOPNODE \_ \_ MF

Especifica o elemento que contém esse nó de origem.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica aos nós de origem **(NÓ SOURCESTREAM DA \_ \_ TOPOLOGIA \_ do MF).**

O pipeline de mídia usa esse atributo para descobrir quando as fontes de mídia fazem parte do mesmo elemento. O pipeline trata todos os nós de origem que fazem parte do mesmo elemento que ter o mesmo relógio.

Quando o pipeline enfilra uma nova topologia que contém nós de origem que fazem parte de um elemento que está presente na topologia anterior, o pipeline trata esses nós de origem como tendo o mesmo relógio que os nós de origem desse elemento na topologia anterior.

> [!Note]  
> O pipeline de mídia não corrige carimbos de data/hora para nós de origem com taxas de relógio diferentes.

 

Uma fonte de mídia que pode fornecer topologias deve implementar a interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) ou a interface [**IMFSequencerSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) Uma fonte de mídia que fornece topologias deve definir o atributo **MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID** em cada nó de origem que ele cria.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[Origem do Sequencer](sequencer-source.md)
</dt> </dl>

 

 




