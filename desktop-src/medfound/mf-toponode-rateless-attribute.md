---
description: Especifica se o sink de mídia associado a esse nó de topologia é rateless.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: MF_TOPONODE_RATELESS atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4de6b132bf2b49e327be45588a497374043794ec73925eb61f2dab16fd1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448866"
---
# <a name="mf_toponode_rateless-attribute"></a>Atributo MF \_ TOPONODE \_ RATELESS

Especifica se o sink de mídia associado a esse nó de topologia é rateless.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Trate como um valor booliana.

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de saída **(NÓ DE SAÍDA \_ DE TOPOLOGIA \_ \_ MF).**

Se o valor desse atributo for diferente de zero, a Sessão de Mídia tratará o sink de mídia como um sinkless rateless, independentemente de o sink de mídia retornar a característica **MEDIASINK \_ RATELESS.** Se esse atributo não estiver definido, o sink de mídia será presumido como não ser rateless.

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

[**IMFMediaSink::GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




