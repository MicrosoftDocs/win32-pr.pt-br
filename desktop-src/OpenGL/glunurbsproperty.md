---
title: função gluNurbsProperty (Glu. h)
description: A função gluNurbsProperty define uma propriedade B-spline racional não uniforme (NURBS).
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
keywords:
- função gluNurbsProperty OpenGL
topic_type:
- apiref
api_name:
- gluNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cbc52bd1405d15967db4aa1ef4941d0c4e166420d25d6d1fcb1ba4db0a6e744
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489026"
---
# <a name="glunurbsproperty-function"></a>função gluNurbsProperty

A função **gluNurbsProperty** define uma propriedade B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

A propriedade a ser definida. Os seguintes valores são válidos:



| Valor                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_SAMPLING_TOLERANCE"></span><span id="glu_sampling_tolerance"></span><dl> <dt>**\_tolerância de amostragem de Glu \_**</dt> </dl>       | Especifica o comprimento máximo, em pixels, a ser usado quando o método de amostragem é definido como GLU \_ comprimento do caminho \_ . O valor padrão é 50,0 pixels.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GLU_DISPLAY_MODE"></span><span id="glu_display_mode"></span><dl> <dt>**\_modo de exibição do Glu \_**</dt> </dl>                         | O parâmetro *Value* define como uma superfície NURBS deve ser renderizada. Você pode definir o *valor* para Glu \_ Fill, \_ polígono de estrutura de tópicos Glu \_ ou \_ patch de estrutura de tópicos Glu \_ . <br/> preenchimento de GLU \_ . A superfície é renderizada como um conjunto de polígonos. Esse é o valor padrão. <br/> \_polígono da estrutura de tópicos Glu \_ . A biblioteca NURBS desenha apenas os contornos dos polígonos criados pelo mosaico. <br/> PATCH do GLU \_ OUTLINE \_ . Somente os contornos de patches e as curvas de corte definidos pelo usuário são desenhados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CULLING"></span><span id="glu_culling"></span><dl> <dt>**remoção de GLU \_**</dt> </dl>                                         | O parâmetro *Value* é um valor booliano. Quando Value é definido como GL \_ true, as curvas NURBS cujos pontos de controle ficam fora do visor atual são descartadas antes do mosaico. O padrão é GL \_ false (porque uma curva NURBS não pode ficar totalmente dentro do convexa envoltória de seus pontos de controle).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GLU_AUTO_LOAD_MATRIX"></span><span id="glu_auto_load_matrix"></span><dl> <dt>**\_matriz de \_ carregamento \_ automático do Glu**</dt> </dl>            | O parâmetro *Value* é um valor booliano. Quando definido como GL \_ true, o código NURBS baixa a matriz de projeção, a matriz modelview e o visor do servidor OpenGL para computar a amostragem e a remoção de matrizes para cada curva NURBS que é renderizada. As matrizes de amostragem e de remoção são necessárias para determinar o mosaico de uma superfície NURBS em segmentos de linha ou polígonos e para examinar uma superfície NURBS se ela estiver fora do visor. <br/> Se esse modo for definido como GL \_ false, você deverá fornecer uma matriz de projeção, matriz modelview e visor para o renderizador NURBS usar para construir matrizes de amostragem e de remoção. Você pode fazer isso com a função [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md) .<br/> O padrão para esse modo é GL \_ true. A alteração desse modo de GL \_ true para GL \_ falso não afeta a amostragem e a remoção de matrizes até que você chame [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md). <br/> Os parâmetros de propriedade a seguir têm suporte na versão 1,1 ou posterior do GLU e não são válidos para a versão 1,0 do GLU: a \_ tolerância paramétrica Glu \_ , o \_ método de amostragem de Glu \_ , a \_ etapa GLU U e a \_ \_ etapa Glu V \_ .<br/> Os parâmetros de valor a seguir têm suporte no GLU versão 1,1 ou posterior e não são válidos para GLU versão 1,0: GLU \_ comprimento do caminho \_ , glu \_ erro paramétrica \_ e distância do domínio do Glu \_ \_ .<br/> |
| <span id="GLU_PARAMETRIC_TOLERANCE"></span><span id="glu_parametric_tolerance"></span><dl> <dt>**\_tolerância paramétrica \_ Glu**</dt> </dl> | Especifica a distância máxima, em pixels, a ser usada quando o método de amostragem é definido como GLU \_ erro paramétrico \_ . O valor padrão é 0,5.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_SAMPLING_METHOD"></span><span id="glu_sampling_method"></span><dl> <dt>**\_método de amostragem de Glu \_**</dt> </dl>                | Especifica como tessallate uma superfície NURBS. \_O método de amostragem Glu \_ pode ter um dos três valores a seguir. <br/> GLU \_ comprimento do caminho \_ . O valor padrão. Especifica que as superfícies renderizadas com o comprimento máximo, em pixels, das bordas dos polígonos de mosaico não são maiores que o valor especificado pela tolerância de amostragem de GLU \_ \_ . <br/> \_erro paramétrico Glu \_ . Especifica que, ao renderizar a superfície, o valor da \_ tolerância paramétrica Glu \_ especifica a distância máxima, em pixels, entre os polígonos de mosaico e as superfícies que eles aproximam. <br/> \_distância do domínio Glu \_ . Especifica, em coordenadas paramétricas, quantos pontos de amostra por comprimento de unidade executar nas dimensões *u* e *v* .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GLU_U_STEP"></span><span id="glu_u_step"></span><dl> <dt>**\_etapa Glu U \_**</dt> </dl>                                           | Especifica o número de pontos de exemplo por comprimento de unidade obtidos na dimensão *u* em coordenadas paramétricas. O valor da \_ etapa Glu U \_ é usado quando o \_ método de amostragem Glu \_ é definido como Glu \_ distância do domínio \_ . O valor padrão é 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_V_STEP"></span><span id="glu_v_step"></span><dl> <dt>**etapa do GLU \_ V \_**</dt> </dl>                                           | Especifica o número de pontos de exemplo por comprimento de unidade obtidos na dimensão *v* em coordenadas paramétricas. O valor da \_ etapa Glu V \_ é usado quando o \_ método de amostragem Glu \_ é definido como Glu \_ distância do domínio \_ . O valor padrão é 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*value* 
</dt> <dd>

O valor para o qual definir a propriedade indicada. O parâmetro *Value* pode ser um valor numérico ou um dos três valores a seguir: Glu \_ comprimento do caminho \_ , \_ erro Glu paramétrica \_ ou distância do domínio do Glu \_ \_ .



| Valor                                                                                                                                                                               | Significado                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_PATH_LENGTH"></span><span id="glu_path_length"></span><dl> <dt>**\_comprimento do caminho de Glu \_**</dt> </dl>                | O valor padrão. Especifica que as superfícies renderizadas com o comprimento máximo, em pixels, das bordas dos polígonos de mosaico não são maiores que o valor especificado pela tolerância de amostragem de GLU \_ \_ .<br/> |
| <span id="GLU_PARAMETRIC_ERROR"></span><span id="glu_parametric_error"></span><dl> <dt>**\_erro paramétrico \_ Glu**</dt> </dl> | Especifica que, ao renderizar a superfície, o valor da \_ tolerância paramétrica Glu \_ especifica a distância máxima, em pixels, entre os polígonos de mosaico e as superfícies que eles aproximam.<br/>       |
| <span id="GLU_DOMAIN_DISTANCE"></span><span id="glu_domain_distance"></span><dl> <dt>**\_distância do domínio Glu \_**</dt> </dl>    | Especifica, em coordenadas paramétricas, quantos pontos de amostra por comprimento de unidade executar nas dimensões *u* e *v* .<br/>                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluNurbsProperty** para controlar as propriedades armazenadas em um objeto NURBS. Essas propriedades afetam a maneira como uma curva NURBS é renderizada.





 

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

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluGetString**](glugetstring.md)
</dt> <dt>

[**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





