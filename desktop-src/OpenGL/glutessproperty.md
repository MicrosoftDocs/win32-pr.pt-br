---
title: função gluTessProperty (Glu. h)
description: A função gluTessProperty define a propriedade de um objeto de mosaico.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- função gluTessProperty OpenGL
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
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086295"
---
# <a name="glutessproperty-function"></a>função gluTessProperty

A função **gluTessProperty** define a propriedade de um objeto de mosaico.

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

*tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*Onde* 
</dt> <dd>

O valor da propriedade a ser definido. Os seguintes valores são válidos: GLU \_ Tess \_ rebobination \_ Rule, glu \_ Tess \_ limite e a \_ \_ tolerância Glu Tess \_ .



| Valor                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <dt>**\_regra de \_ contorno de Tess Glu \_**</dt> </dl>    | Determina quais partes do polígono estão no interior. O parâmetro de valor pode ser definido como um dos seguintes: GLU \_ Tess \_ enventor \_ Odd, glu \_ Tess \_ enrolamento \_ diferente de zero, glu \_ Tess de \_ entorno \_ positivo, glu \_ Tess de \_ enrolamento \_ negativo ou Glu \_ Tess de \_ enventor \_ ABS \_ GEQ \_ dois. <br/> Para entender como a regra de enrolamento funciona, primeiro considere que os contornos de entrada particionam o plano em regiões. A regra de enrolamento determina quais dessas regiões estão dentro do polígono.<br/> Para um C de contorno único, o número de enrolamento de um ponto x é simplesmente o número assinado de rotações que fazemos em torno de x enquanto viajamos uma vez em torno de C (onde o anti-horário é positivo). Quando há várias contornos, os números de enrolamento individuais são somados. Este procedimento associa um valor inteiro assinado a cada ponto x no plano. Observe que o número do enrolamento é o mesmo para todos os pontos em uma única região.<br/> A regra de enrolamento classifica uma região como "interna" se o número do enrolamento pertencer à categoria escolhida (ímpar, diferente de zero, positivo, negativo ou valor absoluto de pelo menos dois). O Tessellator GLU anterior (anterior ao GLU 1,2) usava a regra "Odd". A regra "de zero" (GLU \_ Tess \_ windos de \_ zero) é outra maneira comum de definir o interior. As outras três regras (GLU \_ Tess \_ enventor \_ positivos, glu \_ Tess \_ enrolamento \_ negativo, glu \_ Tess de \_ enrolamento \_ do ABS GEQ \_ \_ dois) são úteis para as operações do polígono CSG.<br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <dt>**\_ \_ somente limite de Tess Glu \_**</dt> </dl> | Especifica um valor booliano (defina Value como GL \_ true ou GL \_ false). Quando você define Value como GL \_ true, um conjunto de contornos fechados separando o interior do polígono e o exterior é retornado em vez de um mosaico. Os contornos exteriores são orientados no sentido anti-horário em relação ao normal; os contornos interiores são orientados no sentido horário. Os \_ \_ retornos de chamada Glu Tess Begin e Glu \_ Tess \_ begin \_ Data usam o \_ loop de linha do tipo GL \_ para cada contorno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <dt>**GLU \_ Tess \_ tolerância**</dt> </dl>              | Especifica uma tolerância para mesclar recursos para reduzir o tamanho da saída. Por exemplo, dois vértices muito próximos uns dos outros podem ser substituídos por um único vértice. A tolerância é multiplicada pela maior magnitude de coordenadas de qualquer vértice de entrada; Isso especifica a distância máxima que qualquer recurso pode mover como resultado de uma única operação de mesclagem. Se um único recurso faz parte de várias operações de mesclagem, a distância total movida pode ser maior. <br/> A mesclagem de recursos é completamente opcional; a tolerância é apenas uma dica. A implementação é gratuita para mesclar em alguns casos e não em outros, ou para nunca mesclar recursos. A tolerância padrão é zero.<br/> A implementação atual mesclará vértices somente se eles forem exatamente coincidentes, independentemente da tolerância atual. Um vértice se unirá a uma borda somente se a implementação não puder distinguir em qual lado da borda o vértice está. Duas bordas são mescladas somente quando os dois pontos de extremidade são idênticos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

*value* 
</dt> <dd>

O valor da propriedade indicada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluTessProperty** controla as propriedades armazenadas em um objeto de mosaico. Essas propriedades afetam a maneira como os polígonos são interpretados e renderizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**gluGetTessProperty**](glugettessproperty.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> </dl>

 

 





