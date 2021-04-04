---
title: função glGetLightfv (GL. h)
description: As funções glGetLightfv e glGetLightiv retornam valores de parâmetro de fonte de luz. | função glGetLightfv (GL. h)
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
keywords:
- função glGetLightfv OpenGL
topic_type:
- apiref
api_name:
- glGetLightfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf90cb9567822ef578bdf01805648a2dabd02db
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837772"
---
# <a name="glgetlightfv-function"></a>função glGetLightfv

As funções **glGetLightfv** e [**glGetLightiv**](glgetlightiv.md) retornam valores de parâmetro de fonte de luz.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetLightfv(
   GLenum  light,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*light* 
</dt> <dd>

Uma fonte de luz. O número de luzes possíveis depende da implementação, mas há suporte para pelo menos oito luzes. Elas são identificadas por nomes simbólicos do formulário GL \_ Light *i,* onde 0 = *i* < GL \_ máx de \_ luzes.

</dd> <dt>

*pname* 
</dt> <dd>

Um parâmetro de fonte de luz para *Light*. Os nomes simbólicos a seguir são aceitos.



| Valor                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**\_ambiente GL**</dt> </dl>                                            | O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que representam a intensidade de ambiente da fonte de luz. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interna, de modo que 1,0 é mapeado para o valor inteiro representável mais positivo e-1,0 é mapeado para o valor inteiro reapresentável mais negativo. Se o valor interno estiver fora do intervalo \[ -1, 1 \] , o valor de retorno de inteiro correspondente será indefinido.<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**\_difusão GL**</dt> </dl>                                            | O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que representam a intensidade difusa da fonte de luz. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interna, de modo que 1,0 é mapeado para o valor inteiro representável mais positivo e-1,0 é mapeado para o valor inteiro reapresentável mais negativo. Se o valor interno estiver fora do intervalo \[ -1, 1 \] , o valor de retorno de inteiro correspondente será indefinido.<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_ESPECULA GL**</dt> </dl>                                         | O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que representam a intensidade especular da fonte de luz. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interna, de modo que 1,0 é mapeado para o valor inteiro representável mais positivo e-1,0 é mapeado para o valor inteiro reapresentável mais negativo. Se o valor interno estiver fora do intervalo \[ -1, 1 \] , o valor de retorno de inteiro correspondente será indefinido.<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**\_posição GL**</dt> </dl>                                         | O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que representam a posição da fonte de luz. Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para o valor inteiro mais próximo. Os valores retornados são aqueles mantidos em coordenadas de olho. Eles não serão iguais aos valores especificados usando [**glLight**](gllight-functions.md), a menos que a matriz modelview tenha sido identificada no momento em que **glLight** foi chamado.<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**\_direção de spot GL \_**</dt> </dl>                      | O parâmetro *params* retorna três valores inteiros ou de ponto flutuante que representam a direção da fonte de luz. Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para o valor inteiro mais próximo. Os valores retornados são aqueles mantidos em coordenadas de olho. Eles não serão iguais aos valores especificados usando **glLight**, a menos que a matriz modelview tenha sido identificada no momento em que **glLight** foi chamado. Embora a direção Spot seja normalizada antes de ser usada na equação de iluminação, os valores retornados são as versões transformadas dos valores especificados antes da normalização.<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**\_expoente de spot de GL \_**</dt> </dl>                         | O parâmetro *params* retorna um único valor de inteiro ou de ponto flutuante que representa o expoente de spot da luz. Um valor inteiro, quando solicitado, é calculado por meio do arredondamento da representação de ponto flutuante interna para o número inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**\_corte de spot GL \_**</dt> </dl>                               | O parâmetro *params* retorna um único valor de inteiro ou de ponto flutuante que representa o ângulo de corte de spot da luz. Um valor inteiro, quando solicitado, é calculado por meio do arredondamento da representação de ponto flutuante interna para o número inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**\_atenuação de constante GL \_**</dt> </dl>    | O parâmetro *params* retorna um único valor inteiro ou de ponto flutuante que representa a atenuação constante (não relacionada à distância) da luz. Um valor inteiro, quando solicitado, é calculado por meio do arredondamento da representação de ponto flutuante interna para o número inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**\_atenuação linear do GL \_**</dt> </dl>          | O parâmetro *params* retorna um único valor de inteiro ou de ponto flutuante que representa a atenuação linear da luz. Um valor inteiro, quando solicitado, é calculado por meio do arredondamento da representação de ponto flutuante interna para o número inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**\_atenuação quadrática do GL \_**</dt> </dl> | O parâmetro *params* retorna um único valor de inteiro ou de ponto flutuante que representa a atenuação quadrática da luz. Um valor inteiro, quando solicitado, é calculado por meio do arredondamento da representação de ponto flutuante interna para o número inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glGetLight** retorna em *params* o valor ou os valores de um parâmetro de fonte de luz. O parâmetro *Light* nomeia a luz e é um nome simbólico do formulário GL \_ Light *i* para 0 = *i* < GL \_ Max \_ luzes, em que GL \_ Max \_ acende é uma constante dependente de implementação que é maior ou igual a oito. O parâmetro *pname* especifica um dos dez parâmetros de fonte de luz, novamente por nome simbólico.

É sempre o caso que o GL \_ Light *i* = GL \_ LIGHT0 + *i*.

Se um erro for gerado, nenhuma alteração será feita no conteúdo de *params*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> </dl>

 

 





