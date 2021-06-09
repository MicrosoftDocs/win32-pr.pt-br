---
title: packoffset
description: Palavra-chave de empacotamento constante de sombreador opcional, que usa a sintaxe a seguir
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826075"
---
# <a name="packoffset"></a>packoffset

Palavra-chave de empacotamento constante de sombreador opcional, que usa a seguinte sintaxe:

: packoffset ( \[ subcomponente de c \] \[ . componente \] )



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                                                                                 | Descrição                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**<br/>                                                                                                  | Palavra-chave required.<br/>                                                                                                                         |
| <span id="c"></span><span id="C"></span>**&**<br/>                                                                                                                             | A embalagem se aplica somente a registros constantes (c). <br/>                                                                                          |
| <span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponente \] \[ . componente\]**<br/> | Subcomponentes e componentes opcionais. Um subcomponente é um número de registro, que é um inteiro. Um componente está na forma de \[ . xyzw \] .<br/> |



 

## <a name="remarks"></a>Comentários

Use essa palavra-chave para empacotar manualmente uma constante de sombreador ao [declarar um tipo de variável](dx-graphics-hlsl-variable-syntax.md).

Ao empacotar uma constante, você não pode misturar tipos constantes.

O compilador se comporta de forma ligeiramente diferente para constantes globais e uniformes:

-   Uma constante global. Uma variável global é adicionada como uma constante global a um *$global* CBuffer pelo compilador. Os elementos empacotados automaticamente (aqueles declarados sem packoffset) serão exibidos após a última variável de pacote manual. Você pode misturar tipos ao empacotar constantes globais.
-   Uma constante uniforme. Um parâmetro uniforme na lista de parâmetros de uma função será adicionado a um buffer de constante *$param* pelo compilador quando o sombreador for compilado fora da estrutura de efeitos. Quando compilado dentro da estrutura de efeito, uma constante uniforme deve resolver para uma variável uniforme definida no escopo global. Uma constante uniforme não pode ser deslocada manualmente; seu uso recomendado é apenas para especialização de sombreadores em que eles fazem o alias de volta para os globais, não como um meio de passar dados de aplicativos para o sombreador.

Aqui estão alguns exemplos adicionais: [constantes de empacotamento usando o modelo de sombreador 4](dx-graphics-hlsl-packing-rules.md).

## <a name="examples"></a>Exemplos

Aqui estão vários exemplos de constantes de sombreador de empacotamento manual.

Pacotes subcomponentes de vetores e escalares cujo tamanho é grande o suficiente para evitar o cruzamento dos limites de registro. Por exemplo, todos eles são válidos:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de Variável](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variáveis (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





