---
description: Especifica se o carregador de topologia habilita o XVP (Transcode Video Processor). para conversões, habilitando a conversão de cores acelerada por hardware.
title: MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK atributo (Mfidl.h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: 3f315463ce1719617c5a48066401219f4b971f0a555cadf2af43b055a2b0e9a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875718"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>Atributo MF \_ TOPOLOGY \_ ENABLE \_ XVP \_ FOR \_ PLAYBACK

Especifica se o carregador de topologia habilita o XVP (Transcode Video Processor). para conversões, habilitando a conversão de cores acelerada por hardware.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

Se esse atributo for definido, o carregador de topologia efetuará pull do processador de vídeo, se necessário, durante a resolução de topologia não transcodificada. Quando você estiver usando a topologia para criar sua própria [IMFTopology,](/windows/win32/api/mfidl/nn-mfidl-imftopology) esse atributo informa ao carregador para usar XVP para conversões em vez do conversor de cores herdado, permitindo, assim, a conversão de cores acelerada de hardware; o conversor de cores herdado é somente software.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Direct3D Gerenciador de Dispositivos](direct3d-device-manager.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




