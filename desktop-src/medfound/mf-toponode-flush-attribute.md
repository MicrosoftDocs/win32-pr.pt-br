---
description: Especifica quando uma transformação é liberada.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: Atributo MF_TOPONODE_FLUSH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67e02c297efa68c6e6c585837675a46b729ec2382be072828059fd795d1c67a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663876"
---
# <a name="mf_toponode_flush-attribute"></a>\_Atributo de \_ liberação MF TOPONODE

Especifica quando uma transformação é liberada.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de transformação (**\_ nó de \_ transformação \_ de topologia MF**).

O valor do atributo é um membro da enumeração do [**\_ modo de \_ liberação \_ MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) . Se esse atributo não estiver definido, o valor padrão será **\_ TOPONODE de \_ movimentação \_ de MF sempre**.

A liberação é executada chamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) na transformação com a mensagem de [**\_ liberação de \_ comando \_ da mensagem MFT**](mft-message-command-flush.md) . Para obter mais informações, consulte Enumeração de [**\_ \_ tipo de mensagem MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .

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

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




