---
description: Especifica como as informações de cores são usadas em operações de pesquisa de movimento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: Propriedade MFPKEY_MOTIONSEARCHLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b53c6bf8f94b2b9817249d96cffbfa0da251dbbcb0545c141230de90f80485af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555406"
---
# <a name="mfpkey_motionsearchlevel-property"></a>\_Propriedade MFPKEY MOTIONSEARCHLEVEL

Especifica como as informações de cores são usadas em operações de pesquisa de movimento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionSearchLevel

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Essa propriedade pode ser definida como um dos valores a seguir.



| Valor | Informações de vídeo usadas                           |
|-------|--------------------------------------------------|
| 0     | Somente Luma.                                       |
| 1     | Luma com croma de inteiro mais próximo.                |
| 2     | Luma com a croma verdadeira.                           |
| -1    | Macrobloco-adaptativo com verdadeiro croma.            |
| -2    | Macrobloco-Adaptive com croma de inteiros mais próximo. |



 

Por padrão, o codec executa a pesquisa de movimento somente no canal Luma. Incluir informações de croma em estimativa de movimento pode melhorar significativamente a qualidade do vídeo codificado. A pesquisa de movimento com Luma e true croma resultará na melhor qualidade de vídeo, mas com o custo de desempenho mais alto. Os dois modos dinâmicos (-1 e-2) e o Luma com o modo de croma de inteiro mais próximo fornecerão comprometimentos razoáveis entre qualidade e desempenho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




