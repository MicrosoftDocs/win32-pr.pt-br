---
description: Especifica a complexidade do algoritmo de codificação.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: Propriedade MFPKEY_ENCCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827912"
---
# <a name="mfpkey_enccomplexity-property"></a>\_Propriedade MFPKEY ENCCOMPLEXITY

Especifica a complexidade do algoritmo de codificação. O valor é um inteiro entre 0 e 100, em que 0 especifica o algoritmo menos complexo e 100 especifica o algoritmo mais complexo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**\_UI4 VT**

## <a name="default-value"></a>Valor padrão

100 para áudio do Windows Media 10 e Windows Media Audio 10 Professional

100 para a versão Windows Vista do Windows Media Audio 10 sem perdas

0 para a versão do Windows 7 Windows Media Audio 10 sem perdas

## <a name="remarks"></a>Comentários

Se a propriedade [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) tiver um valor de **Variant \_ true**, o codificador ajustará a complexidade de seu algoritmo de acordo com o valor dessa propriedade.

Para o codificador do Windows Media Audio 10 e o codificador do Windows Media Audio 10 Professional, se o valor dessa propriedade for 100, o codificador colocará uma alta demanda na CPU e produzirá a saída de qualidade mais alta. Como o valor dessa propriedade diminui, a demanda na CPU diminui, mas a qualidade da saída também diminui.

Para o codificador Windows Media áudio 10 Lossless, se o valor dessa propriedade for 0, o codificador colocará uma baixa demanda na CPU. À medida que o valor dessa propriedade aumenta, a demanda da CPU aumenta e o tamanho da saída do codificador diminui ligeiramente. A saída é sem perdas, independentemente do valor dessa propriedade.

Se você deixar essa propriedade com seu valor padrão de **variante \_ false**, o codificador usará seu algoritmo padrão. O algoritmo padrão depende de qual codificador você está usando e qual versão do Windows está em execução. A tabela a seguir descreve o comportamento padrão para as diferentes combinações.



| Sistema operacional | Comportamento padrão                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Os codificadores do Windows Media Audio 10, do Windows Media Audio 10 Professional e do Windows Media Audio 10 sem perdas usam o algoritmo mais complexo por padrão.                                                    |
| Windows 7        | Os codificadores do Windows Media Audio 10 e do Windows Media Audio 10 Professional usam o algoritmo mais complexo por padrão. O codificador do Windows Media Audio 10 sem perdas usa o algoritmo menos complexo por padrão. |



 

Se a propriedade [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) tiver um valor de **Variant \_ false**, o codificador ignorará essa propriedade.

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

 

 
