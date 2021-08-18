---
description: Especifica o nível de qualidade desejado para codificação VBR (taxa de bits variável) baseada em qualidade (1 passagem) de fluxos de áudio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: MFPKEY_DESIRED_VBRQUALITY propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f52ab8cc791a5309b5df6537d133bce68e49d66a15ab79c12beeb7411cece8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939937"
---
# <a name="mfpkey_desired_vbrquality-property"></a>Propriedade MFPKEY \_ DESIRED \_ VBRQUALITY

Especifica o nível de qualidade desejado para codificação VBR (taxa de bits variável) baseada em qualidade (1 passagem) de fluxos de áudio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

**VT \_ UI4**

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Esse valor pode ser de 0 a 100, em que 100 é a qualidade máxima. Um valor de 0 indica que o método de codificação VBR baseado em qualidade não deve ser usado.

Para enumerar modos VBR que atendem a um determinado requisito de qualidade, de definir as propriedades do codificador a seguir.

-   De [**definir MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como **VARIANT \_ TRUE.**
-   De [**acordo com MFPKEY, \_ \_ RESTRIÇÃO DE \_ VBRQUALITY ENUMERADA como**](mfpkey-constrain-enumerated-vbrqualityproperty.md) VARIANT **\_ TRUE.**
-   De **definir MFPKEY \_ DESIRED \_ VBRQUALITY** com a qualidade desejada. Para modos sem perda, de definir a qualidade desejada como 100.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
