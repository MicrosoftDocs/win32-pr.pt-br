---
description: Especifica se a transformação associada a um nó de topologia dá suporte a DXVA (aceleração de vídeo do DirectX).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: Atributo MF_TOPONODE_D3DAWARE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461332"
---
# <a name="mf_toponode_d3daware-attribute"></a>\_Atributo MF TOPONODE \_ D3DAWARE

Especifica se a transformação associada a um nó de topologia dá suporte a DXVA (aceleração de vídeo do DirectX).

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de transformação (**\_ nó de \_ transformação \_ de topologia MF**).

Normalmente, os aplicativos não usam esse atributo diretamente. A sessão de mídia define esse atributo em um nó de transformação se a transformação de Media Foundation subjacente tiver o atributo de [**\_ \_ \_ reconhecimento de D3D SA do MF**](mf-sa-d3d-aware-attribute.md) .

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

 

 




