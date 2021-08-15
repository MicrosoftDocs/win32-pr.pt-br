---
description: Especifica as configurações de qualidade visual ideais a ser usadas para o codificador de perfil avançado Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7171990280fe004b12c306a09af3b617ba2de0a7cfa274edb3d9191b16a886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242875"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>Propriedade MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE

Especifica as configurações de qualidade visual ideais a ser usadas para o codificador de perfil avançado Windows Media Video 9.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Essa propriedade fornece uma maneira rápida de configurar várias opções de codificação de vídeo. Ele pode ser definido como um dos valores a seguir.



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
<td>O codec não força a otimização e usará quaisquer recursos especificados por outras propriedades. Em muitos casos, o codec usará a lógica interna para determinar as configurações se elas não são especificadas. Este é o valor padrão.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Habilita os recursos que produzirão a melhor qualidade visual. Usar esse valor configura o codec como se você tivesse definido as seguintes propriedades:<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
Se você definir qualquer uma das propriedades na lista anterior, o valor definido substituirá os valores associados a essa configuração, exceto MFPKEY_COMPLEXITYEX <a href="mfpkey-complexityexproperty.md">.</a><br/></td>
</tr>
</tbody>
</table>



 

Definir o valor da propriedade MFPKEY COMPRESSIONOPTIMIZATIONTYPE como 1 também tem o efeito de definir a configuração do Registro de Opção Dquant como 2 e a configuração do Registro método de custo do vetor de movimento \_ como 1. Para obter mais informações, consulte o artigo da Web Usando o Configurações avançado do [Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




