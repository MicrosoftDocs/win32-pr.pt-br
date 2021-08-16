---
description: Especifica se o carregador de topologia habilita o processador de vídeo transcodificar (XVP). para conversões, habilitando a conversão de cores acelerada por hardware.
title: Atributo MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Mfidl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: 3f315463ce1719617c5a48066401219f4b971f0a555cadf2af43b055a2b0e9a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875718"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>\_Topologia MF \_ habilitar \_ XVP \_ para \_ atributo de reprodução

Especifica se o carregador de topologia habilita o processador de vídeo transcodificar (XVP). para conversões, habilitando a conversão de cores acelerada por hardware.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

Se esse atributo for definido, o carregador de topologia efetuará o Pull do processador de vídeo, se necessário, durante a resolução da topologia sem transcodificação. Quando você estiver usando a topologia para criar seu próprio [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) , esse atributo instruirá o carregador a usar o XVP para conversões em vez do conversor de cores herdado, habilitando, assim, a conversão de cores acelerada por hardware; o conversor de cores herdado é somente para software.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gerenciador de Dispositivos Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




