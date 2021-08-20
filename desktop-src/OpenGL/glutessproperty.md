---
title: Função gluTessProperty (Glu.h)
description: A função gluTessProperty define a propriedade de um objeto de mosaico.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- Função gluTessProperty OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595139b91e0fb19ac6ef479831604663dea1981e401aa807ba2bb3cd24a29a41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488426"
---
# <a name="glutessproperty-function"></a>Função gluTessProperty

A **função gluTessProperty** define a propriedade de um objeto de mosaico.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*Que* 
</dt> <dd>

O valor da propriedade a ser definido. Os seguintes valores são válidos: GLU \_ TESS \_ WINDING \_ RULE, GLU \_ TESS \_ BOUNDARY ONLY e GLU TESS \_ \_ \_ TOLERANCE.



| Valor                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <dt>**REGRA DE VENTO DE GLU \_ TESS \_ \_**</dt> </dl>    | Determina quais partes do polígono estão no interior. O parâmetro value pode ser definido como um dos seguintes: GLU \_ TESS \_ \_ WINDING ODD, GLU \_ TESS \_ WINDING \_ NONZERO, GLU \_ TESS \_ WINDING \_ POSITIVE, GLU TESS WINDING NEGATIVE ou GLU TESS \_ \_ \_ \_ \_ WINDING \_ ABS \_ GEQ \_ TWO. <br/> Para entender como a regra de vento funciona, primeiro considere que os particionamentos de entrada do plano em regiões. A regra de vento determina quais dessas regiões estão dentro do polígono.<br/> Para um único contorno C, o número sinuoso de um ponto x é simplesmente o número assinado de revoluções que fazemos em torno de x quando percorremos uma vez em C (em que no sentido anti-horário é positivo). Quando há vários contornos, os números de vento individuais são somados. Este procedimento associa um valor inteiro com sinal a cada ponto x no plano. Observe que o número de vento é o mesmo para todos os pontos em uma única região.<br/> A regra de vento classifica uma região como "dentro" se seu número de vento pertence à categoria escolhida (ímpar, diferente de zero, positivo, negativo ou absoluto de pelo menos dois). O mosaico GLU anterior (antes do GLU 1.2) usava a regra "ímpar". A regra "diferente de zero" (GLU \_ TESS \_ WINDING \_ NONZERO) é outra maneira comum de definir o interior. As outras três regras (GLU \_ TESS \_ WINDING \_ POSITIVE, GLU \_ TESS \_ WINDING NEGATIVE, GLU TESS WINDING ABS GEQ TWO) são úteis para operações de \_ \_ \_ CSG de \_ \_ \_ polígono.<br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <dt>**LIMITE DE GLU \_ TESS \_ \_ SOMENTE**</dt> </dl> | Especifica um valor booliana (valor definido como GL \_ TRUE ou GL \_ FALSE). Quando você definir o valor como GL TRUE, um conjunto de contornos fechados que separam o interior do polígono e o exterior é retornado em vez de \_ um mosaico. Os exteriores são orientados no sentido anti-horário em relação ao normal; interiores são orientados no sentido horário. Os retornos de chamada GLU TESS BEGIN e \_ GLU TESS BEGIN DATA usam o tipo GL LINE LOOP para cada \_ \_ \_ \_ \_ \_ contorno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <dt>**TOLERÂNCIA \_ A GLU TESS \_**</dt> </dl>              | Especifica uma tolerância para mesclar recursos para reduzir o tamanho da saída. Por exemplo, dois vértices muito próximos uns dos outros podem ser substituídos por um único vértice. A tolerância é multiplicada pela maior magnitude de coordenadas de qualquer vértice de entrada; isso especifica a distância máxima que qualquer recurso pode mover como resultado de uma única operação de mesclagem. Se um único recurso participar de várias operações de mesclagem, a distância total movida poderá ser maior. <br/> A mesclação de recursos é completamente opcional; a tolerância é apenas uma dica. A implementação é livre para mesclar em alguns casos e não em outros ou nunca mesclar recursos. A tolerância padrão é zero.<br/> A implementação atual mescla vértices somente se eles são exatamente coincidentes, independentemente da tolerância atual. Um vértice será spliced em uma borda somente se a implementação não puder distinguir em qual lado da borda o vértice está. Duas bordas são mescladas somente quando ambos os pontos de extremidade são idênticos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

*value* 
</dt> <dd>

O valor da propriedade indicada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função gluTessProperty** controla as propriedades armazenadas em um objeto de mosaico. Essas propriedades afetam a maneira como os polígonos são interpretados e renderizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**gluGetTessProperty**](glugettessproperty.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> </dl>

 

 





