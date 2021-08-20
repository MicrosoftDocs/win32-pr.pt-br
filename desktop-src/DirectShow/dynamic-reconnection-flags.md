---
description: Os sinalizadores a seguir especificam o nível de reconexão dinâmica a ser usado durante a renderização.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Sinalizadores de reconexão dinâmica (Qedit.h)
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
ms.openlocfilehash: f7bd2ff28c0928c59c632df501e6545b50707cfd948dd57e4ff1bd1cf01d1721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966236"
---
# <a name="dynamic-reconnection-flags"></a>Sinalizadores de reconexão dinâmica

\[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

Os sinalizadores a seguir especificam o nível de reconexão dinâmica a ser usado durante a renderização.



| Constante/valor                                                                                                                                                                                                                                            | Descrição                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_ DYNAMIC \_ NONE**</dt> <dt>0x00</dt> </dl>          | Nenhuma reconexão dinâmica. Carregue tudo antes de renderizar o projeto.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_ FONTES \_ DINÂMICAS**</dt> <dt>0x01</dt> </dl> | Carregue as fontes somente conforme necessário.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_ EFEITOS \_ DINÂMICOS**</dt> <dt>0X02</dt> </dl> | Reservado. Não use.<br/>                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




