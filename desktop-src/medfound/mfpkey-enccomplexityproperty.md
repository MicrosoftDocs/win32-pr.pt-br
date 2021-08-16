---
description: Especifica a complexidade do algoritmo de codificação.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: MFPKEY_ENCCOMPLEXITY propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93abe02b50f862fec706f75449e00643228a3917bc22ca9dafa9285d9d46be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690121"
---
# <a name="mfpkey_enccomplexity-property"></a>Propriedade MFPKEY \_ ENCCOMPLEXITY

Especifica a complexidade do algoritmo de codificação. O valor é um inteiro entre 0 e 100, em que 0 especifica o algoritmo menos complexo e 100 especifica o algoritmo mais complexo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

**VT \_ UI4**

## <a name="default-value"></a>Valor padrão

100 para Windows Media Audio 10 e Windows Media Audio 10 Professional

100 para a versão Windows Vista do Windows Media Audio 10 Sem perda

0 para a versão Windows 7 Windows Media Audio 10 Sem perda

## <a name="remarks"></a>Comentários

Se a [**propriedade MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) tiver um valor **de VARIANT \_ TRUE**, o codificador ajustará a complexidade de seu algoritmo de acordo com o valor dessa propriedade.

Para o codificador Windows Media Audio 1 Windows 0 e o codificador Professional media audio 10, se o valor dessa propriedade for 100, o codificador coloca uma alta demanda na CPU e produz a saída de qualidade mais alta. À medida que o valor dessa propriedade diminui, a demanda na CPU diminui, mas a qualidade da saída também diminui.

Para o codificador Windows Media Audio 10 Sem perda, se o valor dessa propriedade for 0, o codificador coloca uma baixa demanda na CPU. À medida que o valor dessa propriedade aumenta, a demanda na CPU aumenta e o tamanho da saída do codificador diminui ligeiramente. A saída é sem perda, independentemente do valor dessa propriedade.

Se você deixar essa propriedade com seu valor padrão **VARIANT \_ FALSE**, o codificador usará seu algoritmo padrão. O algoritmo padrão depende de qual codificador você está usando e qual versão do Windows está em execução. A tabela a seguir descreve o comportamento padrão para as diferentes combinações.



| Sistema operacional | Comportamento padrão                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Os codificadores Windows Media Audio 10, Windows Media Audio 10 Professional e Windows Media Audio 10 Lossless usam o algoritmo mais complexo por padrão.                                                    |
| Windows 7        | Os codificadores Windows Media Audio 10 e Windows Media Audio 10 Professional usam o algoritmo mais complexo por padrão. O codificador Windows Media Audio 10 Sem Perda usa o algoritmo menos complexo por padrão. |



 

Se a [**propriedade MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) tiver um valor **de VARIANT \_ FALSE**, o codificador ignorará essa propriedade.

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

 

 
