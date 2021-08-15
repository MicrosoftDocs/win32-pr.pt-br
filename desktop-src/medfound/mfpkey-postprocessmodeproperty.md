---
description: Especifica o modo de pós-processamento do decodificador.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: Propriedade MFPKEY_POSTPROCESSMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce916d0b74c25ae2a57a43acde128ce8c45e7eb42860c3d7a2f129ea2d5b3c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973545"
---
# <a name="mfpkey_postprocessmode-property"></a>\_Propriedade CREATEprocessmode do MFPKEY

Especifica o modo de pós-processamento do decodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

**g \_ wszWMVCForcePostProcessMode**

## <a name="data-type"></a>Tipo de Dados

**\_I4 VT**

## <a name="remarks"></a>Comentários

Defina essa propriedade como um dos valores a seguir.



| Valor | Significado                                                                                |
|-------|----------------------------------------------------------------------------------------|
| -1    | O decodificador define o modo de pós-processamento de maneira adaptável com base nos recursos de CPU disponíveis. |
| 0     | O decodificador não realiza nenhum pós-processamento.                                               |
| 1     | o decodificador da executa o desbloqueio rápido.                                                 |
| 2     | O decodificador executa o desbloqueio completo.                                                  |
| 3     | O decodificador executa o desbloqueio e o destoques rápidos.                                    |
| 4     | O decodificador executa o desbloqueio completo e o destoque.                                    |



 

Como o valor dessa propriedade vai de 0 a 4, a complexidade da decodificação, o uso de recursos da CPU e a qualidade da imagem aumentam.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| Cabeçalho<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




