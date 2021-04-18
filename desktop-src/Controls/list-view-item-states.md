---
title: Estados do item de List-View (CommCtrl. h)
description: O valor de estado de um item consiste no estado do item, um índice de máscara de sobreposição opcional e um índice de máscara de imagem de estado opcional.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752798"
---
# <a name="list-view-item-states"></a>List-View Estados do item

O valor de estado de um item consiste no estado do item, um índice de máscara de sobreposição opcional e um índice de máscara de imagem de estado opcional.

O estado de um item determina sua aparência e funcionalidade. O estado pode ser zero ou um ou mais dos seguintes valores:



| Constante                                                                                                                                                                        | Descrição                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <dt>**ativação do LVIS \_**</dt> </dl>             | Não há suporte no momento.<br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ recortar**</dt> </dl>                                  | O item é marcado para uma operação de recortar e colar.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | O item é realçado como um destino do tipo "arrastar e soltar".<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS com \_ foco**</dt> </dl>                      | O item tem o foco, portanto, está circundado por um retângulo de foco padrão. Embora mais de um item possa ser selecionado, somente um item pode ter o foco.<br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | O índice de imagem de sobreposição do item é recuperado por uma máscara.<br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ selecionado**</dt> </dl>                   | O item está selecionado. A aparência de um item selecionado depende de se ele tem o foco e também das cores do sistema usadas para seleção.<br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | O índice de imagem de estado do item é recuperado por uma máscara.<br/>                                                                                                      |



## <a name="remarks"></a>Comentários

Você pode usar a máscara **LVIS \_ OVERLAYMASK** para isolar o índice baseado em um da imagem de sobreposição. Você pode usar a máscara **LVIS \_ STATEIMAGEMASK** para isolar o índice baseado em um da imagem de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





