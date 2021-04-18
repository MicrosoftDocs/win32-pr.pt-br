---
description: Especifica o nível de qualidade desejado para codificação de taxa de bits variável (VBR) baseada em qualidade (1-pass) de fluxos de áudio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: Propriedade MFPKEY_DESIRED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751538"
---
# <a name="mfpkey_desired_vbrquality-property"></a>MFPKEY \_ desired \_ VBRQUALITY Property

Especifica o nível de qualidade desejado para codificação de taxa de bits variável (VBR) baseada em qualidade (1-pass) de fluxos de áudio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**\_UI4 VT**

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Esse valor pode ser de 0 a 100, onde 100 é a qualidade máxima. Um valor de 0 indica que o método de codificação VBR com base em qualidade não deve ser usado.

Para enumerar modos de VBR que atendam a um determinado requisito de qualidade, defina as propriedades do codificador a seguir.

-   Defina [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como **Variant \_ true**.
-   Defina [**MFPKEY \_ restringir \_ enumerated \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) para **Variant \_ true**.
-   Defina **MFPKEY \_ desired \_ VBRQUALITY** para a qualidade desejada. Para modos sem perdas, defina a qualidade desejada como 100.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
