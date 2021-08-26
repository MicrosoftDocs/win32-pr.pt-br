---
description: especifica as configurações de qualidade visual ideais a serem usadas para o codificador de perfil avançado do Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Propriedade MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e140a854999a5c634620d98958e40832acbe9439
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471722"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>\_Propriedade MFPKEY COMPRESSIONOPTIMIZATIONTYPE

especifica as configurações de qualidade visual ideais a serem usadas para o codificador de perfil avançado do Windows Media Video 9.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Essa propriedade fornece uma maneira rápida de configurar várias opções de codificação de vídeo. Pode ser definido como um dos valores a seguir.




| Valor | Descrição | 
|-------|-------------|
| 0 | O codec não forçará a otimização e usará quaisquer recursos especificados por outras propriedades. Em muitos casos, o codec usará lógica interna para determinar as configurações se elas não forem especificadas. Este é o valor padrão. | 
| 1 | Habilita os recursos que produzirão a melhor qualidade visual. O uso desse valor configura o codec como se você tivesse definido as seguintes propriedades:<br /><ul><li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li><li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li><li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li><li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</li><li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li><li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</li><li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li></ul>Se você definir qualquer uma das propriedades na lista anterior, o valor definido substituirá os valores associados a essa configuração, exceto por <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br /> | 




 

Definir o valor da propriedade MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE como 1 também tem o efeito de definir a configuração de registro de opção Dquant como 2 e a configuração do registro de método de custo de vetor de movimento como 1. para obter mais informações, consulte o artigo da web [usando o Configurações avançado do Codec de perfil avançado do Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

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

 

 




