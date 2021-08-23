---
description: Use esta anotação para associar um parâmetro de efeito a um controle de interface do usuário no ambiente de host. Isso permitirá que um usuário controle interativamente um parâmetro de efeito por meio do aplicativo host.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Anotação da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9e8816bb34ada52794694a2c6ae63ff663787a5db7419e9bf27a40f5aa0cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044064"
---
# <a name="ui-annotation"></a>Anotação da interface do usuário

Use esta anotação para associar um parâmetro de efeito a um controle de interface do usuário no ambiente de host. Isso permitirá que um usuário controle interativamente um parâmetro de efeito por meio do aplicativo host.

DXSAS define um conjunto de controles padrão em termos do modelo de dados e do comportamento básico que os autores de efeito podem esperar de aplicativos de host. A anotação de controle é usada da seguinte maneira:


```
string SasUiControl = "ControlType";
```



onde


```
ControlType
```



 é um dos seguintes:



| ControlType | Descrição                                                                                                                                                                     | Tipo de dados interno                                                                                 | Anotações de propriedade de controle                                                                                 |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Nenhum        | Nenhum controle deve ser mostrado. Observe que um controle ficará visível se [SasUiVisible](#sasuivisible) for true e o tipo de controle for qualquer tipo diferente de None.                           | n/d                                                                                                | n/d                                                                                                          |
| Qualquer         | Isso implica que nenhum controle especial é solicitado. O controle apresentado é o resultado do comportamento definido pelo aplicativo.                                                         | n/d                                                                                                | n/d                                                                                                          |
| ColorPicker | Representa um valor de cor como uma amostra de cor. O valor é empacotado nos componentes XYZ do vetor associado. O componente W do vetor associado sempre é definido como um. | float *n* , em que *n* é de 1 a 4, inclusive.                                                            | [SasUiEnum](#sasuienum)                                                                                      |
| Direção   | Um vetor de direção.                                                                                                                                                             | float *n* , em que *n* é de 2 a 4, inclusive.                                                            | Nenhum                                                                                                         |
| FilePicker  | Uma caixa de diálogo que permite ao usuário procurar e selecionar um arquivo.                                                                                                                  | string                                                                                             | Nenhum                                                                                                         |
| ListPicker  | Uma lista de valores de cadeia de caracteres da qual o usuário pode selecionar uma entrada. Os valores são gerados a partir da anotação [SasUiEnum](#sasuienum) .                                         | Uma matriz de cadeias de caracteres junto com um valor inteiro que contém o índice do valor da cadeia de caracteres selecionada. | [SasUiEnum](#sasuienum)                                                                                      |
| Numérico     | Um conjunto de controles de entrada numéricos (como caixas de texto).                                                                                                                         | float *m* x *N* em que *m* e *N* são de 1 a 4, inclusive.                                               | [SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)                                    |
| Controle deslizante      | Um conjunto de controles deslizantes.                                                                                                                                                               | float *m* x *N* em que *m* e *N* são de 1 a 4, inclusive                                                | [SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower) |
| String      | Uma caixa de texto para editar o conteúdo da cadeia de caracteres.                                                                                                                                         | string                                                                                             | Nenhum                                                                                                         |



 

Se o tipo de dados interno não for idêntico ao tipo do parâmetro associado, a conversão ocorrerá quando os dados forem transferidos do parâmetro aplicativo host para o parâmetro de efeito.

O padrão é a cadeia de caracteres "None".

## <a name="ui-common-properties"></a>Propriedades comuns da interface do usuário

### <a name="sasuidescription"></a>SasUiDescription

Use esta anotação para especificar uma cadeia de caracteres para descrever uma ferramenta. Isso pode ser usado para elementos da interface do usuário, como dicas de ferramenta.


```
string SasUiDescription = "descriptive string";
```



Por exemplo:


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



O padrão é uma cadeia de caracteres vazia.

### <a name="sasuilabel"></a>SasUiLabel

Use esta anotação para especificar uma cadeia de caracteres para rotular qualquer controle de interface do usuário.


```
string SasUiLabel = "some label;
```



Veja um exemplo:


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



O padrão é uma cadeia de caracteres vazia.

### <a name="sasuivisible"></a>SasUiVisible

Use essa anotação para especificar se o parâmetro associado deve ser exibido ao usuário.


```
bool SasUiVisible = false;
```



Se definido como true, o aplicativo host deverá exibir um controle de interface do usuário para editar o parâmetro de efeito anotado. Se for false, nenhuma interface do usuário será exibida no aplicativo host.

Veja um exemplo:


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



O padrão é True.

## <a name="ui-control-properties"></a>Propriedades do controle da interface do usuário

As anotações de propriedade de controle são modificadores adicionais que ajudam a determinar como um controle específico Opera.

### <a name="sasuienum"></a>SasUiEnum

Essa anotação permite restringir o intervalo de valores para um controle. A anotação contém uma cadeia de caracteres de valores delimitada por vírgulas.

O padrão é uma cadeia de caracteres vazia.

### <a name="sasuimax"></a>SasUiMax

Esta Anotação especifica o valor máximo do parâmetro associado. Ele só pode ser associado a um parâmetro de tipo numérico. O valor máximo do parâmetro, na verdade, será calculado como:


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



\_Tipo \_ de parâmetro Max é o valor máximo para o tipo usado pelo parâmetro associado. Isso significa que o valor do parâmetro, levando em conta a anotação [SasUiMax](#sasuimax) é calculada como:


```
ParameterValue = min(NewParameterValue, MaxValue);
```



O valor padrão é FLT \_ Max, conforme definido em Math. h.

### <a name="sasuimin"></a>SasUiMin

Esta Anotação especifica o valor mínimo do parâmetro associado. Ele só pode ser associado a qualquer parâmetro de tipo numérico. O valor mínimo do parâmetro será realmente calculado como:


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



\_Tipo \_ de parâmetro min é o valor mínimo para o tipo usado pelo parâmetro associado. Isso significa que o valor do parâmetro, levando em conta a anotação [SasUiMin](#sasuimin) é calculada como:


```
ParameterValue = max(NewParameterValue, MinValue);
```



O valor padrão é-FLT \_ Max, conforme definido em Math. h.

### <a name="sasuisteps"></a>SasUiSteps

Esta Anotação especifica o número de etapas que podem ser usadas ao incrementar ou decrementar o valor do parâmetro associado. A anotação só é significativa em um parâmetro de tipo numérico. Zero Especifica que o aplicativo host escolherá um número razoável de etapas.

O valor padrão é 0.

### <a name="sasuistepspower"></a>SasUiStepsPower

Esta Anotação especifica o expoente na função Power, que tem o intervalo \[ 0,0 f, 1,0 f \] . Os aplicativos host devem implementar o seguinte método ao calcular valores de parâmetro:


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



O valor padrão é 1,0f.

### <a name="sasuistride"></a>SasUiStride

Essa anotação especifica o incremento que deve ser usado ao incrementar ou decrementar esse valor. Ao contrário de [SasUiSteps,](#sasuisteps) [SasUiStride](#sasuistride) é útil com um controle de rotação, por exemplo, em que os dados não são unidos e o usuário prefere incrementar o valor do parâmetro por stride em vez de por um número de etapas pré-definido. Os aplicativos host devem incrementar (ou decrementar dependendo do comportamento de controle) pelo valor de SasUiStride da seguinte forma:


```
ParameterValue = ParameterValue +/- SasUiStride
```



O valor padrão é 1,0f.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de semântica e anotações padrão do DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



