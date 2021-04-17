---
description: Especifica quando uma transformação é descarregada.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: Atributo MF_TOPONODE_DRAIN (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808318"
---
# <a name="mf_toponode_drain-attribute"></a>\_Atributo de \_ dreno TOPONODE MF

Especifica quando uma transformação é descarregada.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de transformação (**\_ nó de \_ transformação \_ de topologia MF**).

O valor do atributo é um membro da enumeração do [**\_ modo de \_ descarga \_ TOPONODE MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) . Se esse atributo não for definido, o valor padrão será **o \_ \_ \_ padrão MF TOPONODE de dreno**.

O descarregamento é executado chamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) na transformação com a mensagem [**MFT \_ \_ comando de \_ drenagem**](mft-message-command-drain.md) . Para obter mais informações, consulte Enumeração de [**\_ \_ tipo de mensagem MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .

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

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




