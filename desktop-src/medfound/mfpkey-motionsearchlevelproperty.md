---
description: Especifica como as informações de cores são usadas em operações de pesquisa de movimento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: Propriedade MFPKEY_MOTIONSEARCHLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010842"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




