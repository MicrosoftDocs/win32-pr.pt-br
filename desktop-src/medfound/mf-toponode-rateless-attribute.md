---
description: Especifica se o coletor de mídia associado a este nó de topologia é sem taxa.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: Atributo MF_TOPONODE_RATELESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4de6b132bf2b49e327be45588a497374043794ec73925eb61f2dab16fd1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448866"
---
# <a name="mf_toponode_rateless-attribute"></a>\_Atributo MF TOPONODE sem \_ taxa

Especifica se o coletor de mídia associado a este nó de topologia é sem taxa.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de saída (**\_ nó de \_ saída \_ da topologia MF**).

Se o valor desse atributo for diferente de zero, a sessão de mídia tratará o coletor de mídia como um coletor sem taxas, independentemente de o coletor de mídia retornar a característica sem **\_ taxa de MEDIASINK** . Se esse atributo não estiver definido, supõe-se que o coletor de mídia não seja sem taxa.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSink:: getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




