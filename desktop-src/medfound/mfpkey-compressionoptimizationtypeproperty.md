---
description: Especifica as configurações de qualidade visual ideais a serem usadas para o codificador de perfil avançado do Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Propriedade MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781380"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>\_Propriedade MFPKEY COMPRESSIONOPTIMIZATIONTYPE

Especifica as configurações de qualidade visual ideais a serem usadas para o codificador de perfil avançado do Windows Media Video 9.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Essa propriedade fornece uma maneira rápida de configurar várias opções de codificação de vídeo. Pode ser definido como um dos valores a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>O codec não forçará a otimização e usará quaisquer recursos especificados por outras propriedades. Em muitos casos, o codec usará lógica interna para determinar as configurações se elas não forem especificadas. Este é o valor padrão.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Habilita os recursos que produzirão a melhor qualidade visual. O uso desse valor configura o codec como se você tivesse definido as seguintes propriedades:<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
Se você definir qualquer uma das propriedades na lista anterior, o valor definido substituirá os valores associados a essa configuração, exceto por <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
</tbody>
</table>



 

Definir o valor da propriedade MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE como 1 também tem o efeito de definir a configuração de registro de opção Dquant como 2 e a configuração do registro de método de custo de vetor de movimento como 1. Para obter mais informações, consulte o artigo da Web [usando as configurações avançadas do codec de perfil avançado do Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

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

 

 




