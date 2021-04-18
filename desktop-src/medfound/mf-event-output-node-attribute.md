---
description: Identifica o nó de topologia para um coletor de fluxo.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: Atributo MF_EVENT_OUTPUT_NODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754897"
---
# <a name="mf_event_output_node-attribute"></a>\_Atributo de \_ nó de saída de evento MF \_

Identifica o nó de topologia para um coletor de fluxo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Tratar como [**TOPOID**](topoid.md).

## <a name="remarks"></a>Comentários

O valor desse atributo é um identificador de nó para um nó de saída na topologia atual. Para obter um ponteiro para o nó associado, chame [**IMFTopology:: GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) na topologia.

Esse atributo é usado com os seguintes eventos:

-   [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)
-   [MESinkInvalidated](mesinkinvalidated.md)

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




