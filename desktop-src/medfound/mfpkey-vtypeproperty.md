---
description: Especifica a lógica que o codec usará para detectar o vídeo de origem entrelaçados.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: MFPKEY_VTYPE propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f406f0bc91e3431672c2b7f92cc544273e2a64403017a22eb4567054cef0155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973335"
---
# <a name="mfpkey_vtype-property"></a>Propriedade \_ VTYPE MFPKEY

Especifica a lógica que o codec usará para detectar o vídeo de origem entrelaçados.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVType

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Essa propriedade pode ser definida como um dos valores a seguir.



| Valor | Descrição                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | O codec usará a lógica de detecção de tipo de quadro padrão.                                                                                 |
| 1     | O codec tratará todos os quadros de vídeo de origem como quadros entrelaçados.                                                                          |
| 2     | O codec tratará todos os quadros de vídeo de origem como campos de vídeo entrelaçados.                                                                 |
| 3     | O codec determinará automaticamente se os quadros de vídeo de entrada são quadros entrelaçados ou campos de vídeo entrelaçados.                      |
| 4     | O codec determinará automaticamente se os quadros de vídeo de entrada são quadros progressivos, quadros entrelaçados ou campos de vídeo entrelaçados. |



 

Essa propriedade determina o método de codificação de imagem usado para codificação de vídeo progressiva ou entrelaçada.

Se nenhum tipo de vídeo for especificado, o codec usará a codificação de quadro progressivo para sessões de codificação progressiva e a codificação entrelaçada de campo para sessões de codificação entrelaçadas. O tipo de sessão de codificação de vídeo (progressivo ou entrelaçado) é definido usando a propriedade [MFPKEY \_ INTERLACEDCODINGENABLED.](mfpkey-interlacedcodingenabledproperty.md)

> [!Note]  
> A [propriedade MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) deve ser definida como VARIANT TRUE para produzir uma saída entrelaçada; caso contrário, definir a propriedade \_ MPFKEY VTYPE não terá \_ nenhum efeito.

 

Quando o vídeo entrelaçado está sendo codificado, é possível especificar vários métodos de codificação de imagem. Normalmente, a maneira mais eficiente de codificar vídeo entrelaçados é usar o método entrelaçado de campo (2). Se o vídeo de origem contiver muito pouco movimento, o método entrelaçado por quadro (1) ou o método de quadro/campo automático (2) poderá ser mais adequado.

Ao codificar conteúdo misto (contendo quadros progressivos e entrelaçados), é melhor usar o método frame/field/progressive (4) do valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




