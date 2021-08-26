---
title: Estados do item de controle de tabulação (CommCtrl.h)
description: Os itens de controle de tabulação agora são suportados por um estado de item para dar suporte à mensagem \_ TCM DESELECTALL. Além disso, a estrutura TCITEM dá suporte a valores de estado de item.
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
ms.openlocfilehash: 75f3bba0ecd29c7ab84c6b68010f8af52c8db2cfc9dc4080fb73e37b408ee1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919276"
---
# <a name="tab-control-item-states"></a>Estados do item de controle de tabulação

Os itens de controle de tabulação agora são suportados por um estado de item para dar suporte à mensagem [**\_ TCM DESELECTALL.**](tcm-deselectall.md) Além disso, a estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) dá suporte a valores de estado de item.



| Constante                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**BOTÃO TCIS \_ COMPACTADO**</dt> </dl> | [Versão 4.70.](common-control-versions.md) O item de controle de tabulação está selecionado. Esse estado só será significativo se o sinalizador [**de estilo \_ TCS BUTTONS**](tab-control-styles.md) tiver sido definido.<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS \_ REALÇADA**</dt> </dl>       | [Versão 4.71.](common-control-versions.md) O item de controle de tabulação é realçada e a guia e o texto são desenhados usando a cor de realçada atual. Ao usar a cor alta, essa será uma interpolação verdadeira, não uma cor dithered.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





