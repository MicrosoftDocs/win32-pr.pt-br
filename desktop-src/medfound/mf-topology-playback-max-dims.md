---
description: Especifica o tamanho da janela de destino para reprodução de vídeo.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: MF_TOPOLOGY_PLAYBACK_MAX_DIMS atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98575a32b1d68414cb4d94a547273aa4986e03dc707023d5c40f9860b77b5a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604776"
---
# <a name="mf_topology_playback_max_dims-attribute"></a>Atributo MF \_ TOPOLOGY \_ PLAYBACK MAX \_ \_ DIMS

Especifica o tamanho da janela de destino para reprodução de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).

Para definir esse atributo, chame [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

O carregador de topologia usa esse atributo para otimizar o pipeline antes do início da reprodução. Se você definir esse atributo, de definir também o atributo [ \_ MF TOPOLOGY \_ STATIC PLAYBACK \_ \_ OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) como **TRUE.**

Os 32 bits superiores do valor do atributo contêm a largura e os 32 bits inferiores contêm a altura, ambos em pixels.

A constante GUID para esse atributo é exportada de mfuuid.lib.

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

[Atributos de topologia](topology-attributes.md)
</dt> <dt>

[Gerenciamento de qualidade de vídeo](video-quality-management.md)
</dt> </dl>

 

 




