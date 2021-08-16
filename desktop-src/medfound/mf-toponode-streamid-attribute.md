---
description: O identificador de fluxo do sink de fluxo associado a esse nó de topologia.
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: MF_TOPONODE_STREAMID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cf1edc8918af91144de4f408e7913c3f40b1f0246059bc5bf9e4f1193a1cf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739885"
---
# <a name="mf_toponode_streamid-attribute"></a>Atributo \_ STREAMID TOPONODE \_ MF

O identificador de fluxo do sink de fluxo associado a esse nó de topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de saída **(NÓ DE SAÍDA \_ DE TOPOLOGIA \_ \_ MF).**

Quando a Sessão de Mídia carrega a topologia, ela consulta o sink de mídia para um sink de fluxo com o identificador especificado. Se isso falhar, ele tentará adicionar um novo sink de fluxo ao sink de mídia.

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

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




