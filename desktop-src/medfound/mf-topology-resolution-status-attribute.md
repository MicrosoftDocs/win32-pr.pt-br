---
description: Especifica o status de uma tentativa de resolver uma topologia.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: Atributo MF_TOPOLOGY_RESOLUTION_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827619"
---
# <a name="mf_topology_resolution_status-attribute"></a>\_Atributo de \_ status de resolução de topologia MF \_

Especifica o status de uma tentativa de resolver uma topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O carregador de topologia ou a sessão de mídia pode definir esse atributo em uma topologia. O valor desse atributo é um bit a bit **ou** de sinalizadores da enumeração de sinalizadores de [**status de \_ \_ resolução de \_ \_ topologia MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




