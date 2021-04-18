---
description: Especifica o elemento que contém este nó de origem.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: Atributo MF_TOPONODE_SEQUENCE_ELEMENTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798468"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>\_ \_ Atributo ElementID da sequência MF TOPONODE \_

Especifica o elemento que contém este nó de origem.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**).

O pipeline de mídia usa esse atributo para descobrir quando as fontes de mídia fazem parte do mesmo elemento. O pipeline trata todos os nós de origem que fazem parte do mesmo elemento como tendo o mesmo relógio.

Quando o pipeline enfileira uma nova topologia que contém nós de origem que fazem parte de um elemento que está presente na topologia anterior, o pipeline trata esses nós de origem como tendo o mesmo relógio que os nós de origem desse elemento na topologia anterior.

> [!Note]  
> O pipeline de mídia não corrige carimbos de data/hora para nós de origem com taxas de clock diferentes.

 

Uma fonte de mídia que pode fornecer topologias deve implementar a interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) ou a interface [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) . Uma fonte de mídia que fornece topologias deve definir o atributo **\_ TOPONODE \_ Sequence \_ ElementID** em cada nó de origem que ele cria.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 




