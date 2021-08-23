---
title: Função glGetLightfv (Gl.h)
description: As funções glGetLightfv e glGetLightiv retornam valores de parâmetro de fonte de luz. | Função glGetLightfv (Gl.h)
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
keywords:
- Função glGetLightfv OpenGL
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
ms.openlocfilehash: 5d642b0d253abca4ea7c5f224353f5544b5307df5237e958c32e37b98ff2e01f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741987"
---
# <a name="glgetlightfv-function"></a>Função glGetLightfv

As **funções glGetLightfv** e [**glGetLightiv**](glgetlightiv.md) retornam valores de parâmetro de fonte de luz.

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

Uma fonte de luz. O número de luzes possíveis depende da implementação, mas há suporte para pelo menos oito luzes. Eles são identificados por nomes simbólicos da forma GL \_ LIGHT *i,* em que 0 = *i* < GL \_ MAX \_ LIGHTS.

</dd> <dt>

*Pname* 
</dt> <dd>

Um parâmetro de fonte de luz para *luz.* Os nomes simbólicos a seguir são aceitos.



| Valor                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                                            | O *parâmetro params* retorna quatro valores inteiros ou de ponto flutuante que representam a intensidade do ambiente da fonte de luz. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interno, de modo que 1.0 mapeia para o valor inteiro representável mais positivo e -1,0 é mapeado para o valor inteiro representável mais negativo. Se o valor interno estiver fora do intervalo -1,1 , o valor de retorno de inteiro \[ \] correspondente será indefinido.<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFUSO**</dt> </dl>                                            | O *parâmetro params* retorna quatro valores inteiros ou de ponto flutuante que representam a intensidade difusa da fonte de luz. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interno, de modo que 1.0 mapeia para o valor inteiro representável mais positivo e -1,0 é mapeado para o valor inteiro representável mais negativo. Se o valor interno estiver fora do intervalo -1,1 , o valor de retorno de inteiro \[ \] correspondente será indefinido.<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                                         | O *parâmetro params* retorna quatro valores inteiros ou de ponto flutuante que representam a intensidade especular da fonte de luz. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interno, de modo que 1.0 mapeia para o valor inteiro representável mais positivo e -1,0 é mapeado para o valor inteiro representável mais negativo. Se o valor interno estiver fora do intervalo -1,1 , o valor de retorno de inteiro \[ \] correspondente será indefinido.<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**POSIÇÃO \_ GL**</dt> </dl>                                         | O *parâmetro params* retorna quatro valores inteiros ou de ponto flutuante que representam a posição da fonte de luz. Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante interno para o valor inteiro mais próximo. Os valores retornados são aqueles mantidos em coordenadas de olho. Eles não serão iguais aos valores especificados usando [**glLight,**](gllight-functions.md)a menos que a matriz modelview tenha sido identificada no momento em que **glLight** foi chamado.<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**DIREÇÃO \_ DO SPOT \_ GL**</dt> </dl>                      | O *parâmetro params* retorna três valores inteiros ou de ponto flutuante que representam a direção da fonte de luz. Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante interno para o valor inteiro mais próximo. Os valores retornados são aqueles mantidos em coordenadas de olho. Eles não serão iguais aos valores especificados usando **glLight,** a menos que a matriz modelview tenha sido identificada no momento em que **glLight** foi chamado. Embora a direção spot seja normalizada antes de ser usada na equação de iluminação, os valores retornados são as versões transformadas dos valores especificados antes da normalização.<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL \_ SPOT \_ EXPONENT**</dt> </dl>                         | O *parâmetro params* retorna um único inteiro ou valor de ponto flutuante que representa o expoente spot da luz. Um valor inteiro, quando solicitado, é calculado arredondando a representação de ponto flutuante interno para o inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**CORTE \_ DE PONTO DE \_ GL**</dt> </dl>                               | O *parâmetro params* retorna um único inteiro ou um valor de ponto flutuante que representa o ângulo de corte spot da luz. Um valor inteiro, quando solicitado, é calculado arredondando a representação de ponto flutuante interno para o inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**ATENUAÇÃO \_ \_ DE CONSTANTE GL**</dt> </dl>    | O *parâmetro params* retorna um único inteiro ou valor de ponto flutuante que representa a atenuação constante (não relacionada à distância) da luz. Um valor inteiro, quando solicitado, é calculado arredondando a representação de ponto flutuante interno para o inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**ATENUAÇÃO LINEAR GL \_ \_**</dt> </dl>          | O *parâmetro params* retorna um único inteiro ou valor de ponto flutuante que representa a atenuação linear da luz. Um valor inteiro, quando solicitado, é calculado arredondando a representação de ponto flutuante interno para o inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**\_ATENUAÇÃO \_ QUADRÁTICA GL**</dt> </dl> | O *parâmetro params* retorna um único inteiro ou valor de ponto flutuante que representa a atenuação quadrática da luz. Um valor inteiro, quando solicitado, é calculado arredondando a representação de ponto flutuante interno para o inteiro mais próximo.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função glGetLight** retorna em *parâmetros o* valor ou os valores de um parâmetro de fonte de luz. O *parâmetro* light nomeia a luz e é um nome simbólico do formato GL LIGHT i para \_ 0 = *i* < GL MAX LIGHTS, em que GL MAX LIGHTS é uma constante dependente de implementação maior ou igual a \_ \_ \_ \_ oito. O *parâmetro pname* especifica um dos dez parâmetros de fonte de luz, novamente por nome simbólico.

É sempre o caso de GL \_ LIGHT *i* = GL \_ LIGHT0 + *i*.

Se um erro for gerado, nenhuma alteração será feita no conteúdo *de params*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> </dl>

 

 





