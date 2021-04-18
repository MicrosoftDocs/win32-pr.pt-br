---
title: Estados do item de controle de guia (CommCtrl. h)
description: Os itens de controle de guia agora dão suporte a um estado de item para dar suporte à \_ mensagem TCM DESELECTALL. Além disso, a estrutura TCITEM dá suporte a valores de estado do item.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756023"
---
# <a name="tab-control-item-states"></a>Estados do item de controle de guia

Os itens de controle de guia agora dão suporte a um estado de item para dar suporte à mensagem [**TCM \_ DESELECTALL**](tcm-deselectall.md) . Além disso, a estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) dá suporte a valores de estado do item.



| Constante                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**TCIS \_ ButtonPressed**</dt> </dl> | [Versão 4,70](common-control-versions.md). O item de controle guia é selecionado. Esse Estado só será significativo se o sinalizador de estilo de [**\_ botões de TCS**](tab-control-styles.md) tiver sido definido.<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS \_ realçado**</dt> </dl>       | [Versão 4,71](common-control-versions.md). O item de controle guia é realçado e a guia e o texto são desenhados usando a cor de realce atual. Ao usar High-Color, essa será uma interpolação real, não uma cor dificada.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





