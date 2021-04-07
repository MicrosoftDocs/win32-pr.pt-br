---
description: Especifica a lógica que o codec usará para detectar o vídeo de origem entrelaçado.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: Propriedade MFPKEY_VTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827550"
---
# <a name="mfpkey_vtype-property"></a>\_Propriedade MFPKEY VTYPE

Especifica a lógica que o codec usará para detectar o vídeo de origem entrelaçado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVType

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Essa propriedade pode ser definida como um dos valores a seguir.



| Valor | Descrição                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | O codec usará a lógica de detecção de tipo de quadro padrão.                                                                                 |
| 1     | O codec tratará todos os quadros de vídeo de origem como quadros entrelaçados.                                                                          |
| 2     | O codec tratará todos os quadros de vídeo de origem como campos de vídeo entrelaçado.                                                                 |
| 3     | O codec determinará automaticamente se os quadros de vídeo de entrada são quadros entrelaçados ou campos de vídeo entrelaçado.                      |
| 4     | O codec determinará automaticamente se os quadros de vídeo de entrada são quadros progressivos, quadros entrelaçados ou campos de vídeo entrelaçado. |



 

Essa propriedade determina o método de codificação de imagem usado para codificação de vídeo progressiva ou entrelaçada.

Se nenhum tipo de vídeo for especificado, o codec usará a codificação de quadro progressivo para sessões de codificação progressiva e a codificação entrelaçada de campo para sessões de codificação entrelaçadas. O tipo de sessão de codificação de vídeo (progressiva ou entrelaçada) é definido usando a propriedade [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) .

> [!Note]  
> A propriedade [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) deve ser definida como Variant \_ true para produzir uma saída entrelaçada; caso contrário, a definição da \_ Propriedade MPFKEY VTYPE não terá efeito.

 

Quando o vídeo entrelaçado está sendo codificado, é possível especificar vários métodos de codificação de imagem. Normalmente, a maneira mais eficiente de codificar vídeo entrelaçado é usar o método entrelaçado de campo (2). Se o vídeo de origem contiver muito pouco movimento, o método entrelaçado do quadro (1) ou o método de quadro/campo automático (2) poderá ser mais adequado.

Ao codificar conteúdo misto (contendo quadros progressivos e entrelaçados), é melhor usar o método de valor quadro automático/campo/progressivo (4).

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

 

 




