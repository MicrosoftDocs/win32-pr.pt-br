---
description: Os sinalizadores a seguir especificam o nível de reconexão dinâmica a ser usado durante a renderização.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Sinalizadores de reconexão dinâmica (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780636"
---
# <a name="dynamic-reconnection-flags"></a>Sinalizadores de reconexão dinâmica

\[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

Os sinalizadores a seguir especificam o nível de reconexão dinâmica a ser usado durante a renderização.



| Constante/valor                                                                                                                                                                                                                                            | Descrição                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_ DINÂMICO \_ nenhum**</dt> <dt>0x00</dt> </dl>          | Nenhuma reconexão dinâmica. Carregar tudo antes de renderizar o projeto.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_ \_Origens dinâmicas**</dt> <dt>0x01</dt> </dl> | Carregue as fontes somente conforme necessário.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_ \_Efeitos dinâmicos**</dt> <dt>0x02</dt> </dl> | Reservado. Não use.<br/>                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




