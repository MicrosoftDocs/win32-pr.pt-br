---
description: Especifica como o carregador de topologia conecta esse nó de topologia e se esse nó é opcional.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: Atributo MF_TOPONODE_CONNECT_METHOD (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171331"
---
# <a name="mf_toponode_connect_method-attribute"></a>\_Atributo do método MF TOPONODE \_ Connect \_

Especifica como o carregador de topologia conecta esse nó de topologia e se esse nó é opcional.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a todos os tipos de nó.

O valor do atributo é um bit a bit **ou** dos sinalizadores da enumeração do [**\_ \_ método de conexão MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) . Se esse atributo não for definido, o valor padrão será **MF \_ Connect \_ permitir \_ decodificador**.

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

 

 




