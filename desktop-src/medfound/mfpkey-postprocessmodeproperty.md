---
description: Especifica o modo de pós-processamento para o decodificador.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: MFPKEY_POSTPROCESSMODE propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce916d0b74c25ae2a57a43acde128ce8c45e7eb42860c3d7a2f129ea2d5b3c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973545"
---
# <a name="mfpkey_postprocessmode-property"></a>Propriedade POSTPROCESSMODE MFPKEY \_

Especifica o modo de pós-processamento para o decodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

**g \_ wszWMVCForcePostProcessMode**

## <a name="data-type"></a>Tipo de Dados

**VT \_ I4**

## <a name="remarks"></a>Comentários

De definir essa propriedade como um dos valores a seguir.



| Valor | Significado                                                                                |
|-------|----------------------------------------------------------------------------------------|
| -1    | O decodificador define o modo de pós-processamento de forma adaptável com base nos recursos de CPU disponíveis. |
| 0     | O decodificador não executa nenhum pós-processamento.                                               |
| 1     | fO decodificador executa o desbloqueio rápido.                                                 |
| 2     | O decodificador executa o desbloqueio completo.                                                  |
| 3     | O decodificador executa o desbloqueio e o deringing rápidos.                                    |
| 4     | O decodificador executa o desbloqueio e a dering completos.                                    |



 

Como o valor dessa propriedade vai de 0 a 4, a complexidade de decodificação, o uso de recursos de CPU e a qualidade da imagem aumentam.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| Cabeçalho<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




