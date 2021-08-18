---
description: Constantes usadas para definir a prioridade de um recurso em setanteriority.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 367d50292b283cc7a0dcdef42b2e2c270099e314dc61c8d590e7ef2a1091a4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751325"
---
# <a name="d3d9_resource_priority"></a>\_Prioridade do recurso d3d9 \_

Constantes usadas para definir a prioridade de um recurso em [**Setanteriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).



| Constante/valor                                                                                                                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <dt>**D3d9 \_ 0x28000000 \_ \_ mínimo de prioridade de recurso**</dt> <dt></dt> </dl> | O recurso tem a menor prioridade possível. Essa constante marca o recurso como não usado e para remoção. O recurso deve ser removido assim que outro recurso exigir o espaço de memória que o recurso ocupa.<br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <dt>**D3d9 \_ Prioridade de recurso \_ \_ baixa**</dt> <dt>0x50000000</dt> </dl>             | O recurso está agendado com baixa prioridade. O posicionamento do recurso não é crítico e o sistema operacional executa o mínimo de trabalho para encontrar um local para o recurso. Marcar um recurso como prioridade baixa permite que outros recursos mais críticos ocupem a memória mais rápida.<br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <dt>**D3d9 \_ 0x78000000 \_ \_ normal de prioridade de recurso**</dt> <dt></dt> </dl>    | O recurso está agendado com prioridade normal. O posicionamento do recurso é importante para o desempenho, mas não é crítico. O sistema operacional deve tentar posicionar o recurso que está marcado como normal no local preferido do recurso, em vez de um recurso de baixa prioridade. Normalmente, as texturas são marcadas como normais.<br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <dt>**D3d9 \_ Prioridade de recurso \_ \_ alta**</dt> <dt>0xA0000000</dt> </dl>          | O recurso está agendado com alta prioridade. O posicionamento do recurso é crítico para o desempenho. O sistema operacional sempre tenta posicionar o recurso que está marcado como alto no local preferido do recurso, em vez de um recurso de baixa prioridade ou de prioridade normal. Normalmente, os destinos de renderização são marcados como altos.<br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <dt>**D3d9 \_ 0xc8000000 \_ \_ máxima de prioridade de recurso**</dt> <dt></dt> </dl> | O recurso tem a prioridade máxima possível. Essa constante marca a prioridade do recurso como fixado flexível. Um recurso fixo por software será removido da memória somente se não houver nenhuma outra maneira de resolver o requisito de memória de um buffer de DMA. O sistema operacional tenta dividir um buffer de DMA para seu tamanho mínimo e remover todos os outros recursos que não estão fixados e não são fixados antes de remover um recurso fixado por software. <br/> |



## <a name="remarks"></a>Comentários

Valores diferentes de **\_ prioridade de recurso d3d9 \_ \_ mínimo** e máximo de **\_ prioridade de recurso \_ \_ d3d9** são tratados como dicas pelo Agendador.

Você pode usar níveis de prioridade diferentes dos valores definidos anteriormente neste tópico. Por exemplo, marcar um recurso com um nível de prioridade de 0x78000001 indica que a prioridade do recurso está um pouco acima do normal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
