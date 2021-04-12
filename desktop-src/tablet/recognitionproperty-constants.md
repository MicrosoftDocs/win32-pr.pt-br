---
description: Define os valores que especificam as propriedades de uma alternativa de reconhecimento. A API (interface de programação de aplicativo) do Tablet PC usa identificadores globais exclusivos (GUIDs) para identificar Propriedades de pacote, que na automação são cadeias de caracteres constantes.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Constantes rerecognitionproperty (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297376"
---
# <a name="recognitionproperty-constants"></a>Constantes rerecognitionproperty

Define os valores que especificam as propriedades de uma alternativa de reconhecimento. A API (interface de programação de aplicativo) do Tablet PC usa identificadores globais exclusivos (GUIDs) para identificar Propriedades de pacote, que na automação são cadeias de caracteres constantes.

A tabela a seguir lista os campos GUID (identificador global exclusivo) da propriedade alternativa de reconhecimento disponíveis. Use esses GUIDs para acessar as propriedades de um objeto [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) chamando o método [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Nome da constante</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </dl></td>
<td style="text-align: left;">O GUID que identifica a propriedade para o número de linha do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/> LineNumber especifica as alternativas com um número de linha específico.<br/>
<blockquote>
[!Note]<br />
Este campo não tem suporte para reconhecedores de caracteres do leste asiático.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </dl></td>
<td style="text-align: left;">O GUID que identifica a propriedade para a segmentação do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/> Segmentação especifica o fragmento de tinta básico ou a unidade que o reconhecedor usa para produzir um resultado de reconhecimento.<br/>
<blockquote>
[!Note]<br />
Não implementado.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </dl></td>
<td style="text-align: left;">O GUID que identifica a propriedade para o ponto de acesso de reconhecimento do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </dl></td>
<td style="text-align: left;">O GUID que identifica a propriedade para a contagem máxima de traços do resultado de reconhecimento do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/>
<blockquote>
[!Note]<br />
Não implementado.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </dl></td>
<td style="text-align: left;">O GUID que identifica a propriedade para a métrica de pontos por polegada do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/>
<blockquote>
[!Note]<br />
Não implementado.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </dl></td>
<td style="text-align: left;">O GUID que identifica a propriedade para o nível de confiança que o reconhecedor tem no resultado do reconhecimento.<br/>
<blockquote>
[!Note]<br />
A avaliação de confiança está disponível apenas para o Estados Unidos Inglês e todos os reconhecedores de gestos no Microsoft Windows XP Tablet PC Edition e no Windows Vista. Métodos que fornecem a propriedade de confiança para qualquer outro reconhecedor retornam E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </dl></td>
<td style="text-align: left;">O GUID que identifica a propriedade para as métricas de linha do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> , que é a linha para a qual as métricas serão recuperadas. <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Em C++, você pode acessar essas constantes no arquivo de cabeçalho Msinkaut. h, que está localizado no <systemdrive> diretório: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ include se você instalou o SDK no local padrão.

> [!Note]  
> Em C++, essas constantes são WCHARs, não BSTRs. Converta-os em BSTRs antes de usar. Para obter mais informações sobre o tipo de dados BSTR, consulte [usando a biblioteca com](using-the-com-library.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método AlternatesWithConstantPropertyValues**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[**Propriedade ConfidenceAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[**Propriedade LineAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[**Interface IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




