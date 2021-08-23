---
title: Função glLightiv (Gl.h)
description: A função glLightiv retorna valores de parâmetro de origem clara.
ms.assetid: 927f6a7e-be42-46ab-9c23-6ce87f96bd8a
keywords:
- Função glLightiv OpenGL
topic_type:
- apiref
api_name:
- glLightiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b497c6cbac510b57814303f07ee060398e255b02dd1c8f9d7cd129f386d776
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493246"
---
# <a name="gllightiv-function"></a>Função glLightiv

A **função glLightiv** retorna valores de parâmetro de origem clara.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glLightiv(
         GLenum light,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*light* 
</dt> <dd>

O identificador de uma luz. O número de luzes possíveis depende da implementação, mas há suporte para pelo menos oito luzes. Eles são identificados por nomes simbólicos da forma GL LIGHT i, em que i é um \_ valor: 0 a GL MAX LIGHTS -  \_ \_ 1.

</dd> <dt>

*Pname* 
</dt> <dd>

Um parâmetro de fonte de luz para *luz.* Os nomes simbólicos a seguir são aceitos.



| Valor                                                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                                                                                                                                                                                                | O *parâmetro params* contém quatro valores inteiros que especificam a intensidade RGBA do ambiente da luz. Os valores inteiros são mapeados linearmente de modo que o valor representável mais positivo seja mapeado para 1,0 e o valor representável mais negativo seja mapeado para -1,0. Os valores de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. A intensidade de luz ambiente padrão é (0,0, 0,0, 0,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFUSO**</dt> </dl>                                                                                                                                                                                                | O *parâmetro params* contém quatro valores inteiros que especificam a intensidade difusa de RGBA da luz. Os valores inteiros são mapeados linearmente de modo que o valor representável mais positivo seja mapeado para 1,0 e o valor representável mais negativo seja mapeado para -1,0. Os valores de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. A intensidade difusa padrão é (0,0, 0,0, 0,0, 1,0) para todas as luzes que não são de zero claro. A intensidade difusa padrão de zero claro é (1,0, 1,0, 1,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                                                                                                                                                                                             | O *parâmetro params* contém quatro valores inteiros que especificam a intensidade RGBA especular da luz. Os valores inteiros são mapeados linearmente de modo que o valor representável mais positivo seja mapeado para 1,0 e o valor representável mais negativo seja mapeado para 1,0. Os valores de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. A intensidade especular padrão é (0,0, 0,0, 0,0, 1,0) para todas as luzes que não são claras zero. A intensidade especular padrão da luz zero é (1,0, 1,0, 1,0, 1,0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**POSIÇÃO \_ GL**</dt> </dl>                                                                                                                                                                                             | O *parâmetro params* contém quatro valores inteiros que especificam a posição da luz em coordenadas de objeto homogêneas. Os valores inteiro e de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. <br/> A posição é transformada pela matriz modelview quando [**glLightiv**](gllightfv.md) é chamado (como se fosse um ponto) e é armazenado em coordenadas de olho. Se o *componente w* da posição for 0,0, a luz será tratada como uma fonte direcional. Cálculos de iluminação difusa e especular levam em conta a direção da luz, mas não sua posição real, e a atenuação está desabilitada. Caso contrário, cálculos de iluminação difusa e especular baseiam-se na localização real da luz nas coordenadas de olho e a atenuação está habilitada. A posição padrão é (0,0,1,0); portanto, a fonte de luz padrão é direcional, paralela a e na direção do eixo *- z.*<br/> |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**DIREÇÃO \_ DO SPOT \_ GL**</dt> </dl>                                                                                                                                                                          | O *parâmetro params* contém três valores inteiros que especificam a direção da luz em coordenadas de objeto homogêneas. Os valores inteiro e de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. <br/> A direção do ponto é transformada pelo inverso da matriz modelview quando **glLightiv** é chamado (como se fosse normal) e é armazenado em coordenadas de olho. Isso é significativo somente quando GL \_ SPOT \_ CUTOFF não é 180, que é por padrão. A direção padrão é (0,0,1).<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL \_ SPOT \_ EXPONENT**</dt> </dl>                                                                                                                                                                             | O *parâmetro params* é um único valor inteiro que especifica a distribuição de intensidade da luz. Valores inteiros e de ponto flutuante são mapeados diretamente. Somente valores no intervalo \[ 0, 128 \] são aceitos. <br/> A intensidade de luz efetiva é atenuada pelo cosseno do ângulo entre a direção da luz e a direção da luz para o vértice que está sendo avistado, elevado à potência do expoente spot. Portanto, expoentes de ponto mais altos resultam em uma fonte de luz mais focada, independentemente do ângulo de corte spot. O expoente spot padrão é 0, resultando em distribuição uniforme de luz.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**CORTE \_ DE PONTO DE \_ GL**</dt> </dl>                                                                                                                                                                                   | O *parâmetro params* é um único valor inteiro que especifica o ângulo máximo de propagação de uma fonte de luz. Valores inteiros e de ponto flutuante são mapeados diretamente. Somente os valores no intervalo \[ 0, 90 \] e no valor especial 180 são aceitos. <br/> Se o ângulo entre a direção da luz e a direção da luz para o vértice que está sendo acessado for maior que o ângulo de corte spot, a luz será completamente mascarada. Caso contrário, sua intensidade será controlada pelo expoente spot e pelos fatores de atenuação. O corte spot padrão é 180, resultando em distribuição uniforme de luz.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**ATENUAÇÃO \_ \_ CONSTANTE GL, \_ ATENUAÇÃO LINEAR \_ GL, \_ ATENUAÇÃO QUADRÁTICA \_ GL**</dt> </dl> | O *parâmetro params* é um único valor inteiro que especifica um dos três fatores de atenuação de luz. Valores inteiros e de ponto flutuante são mapeados diretamente. Somente valores não informativos são aceitos. <br/> Se a luz for posicional, em vez de direcional, sua intensidade será atenuada pela soma recíproca de: o fator constante, o fator linear multiplicado pela distância entre a luz e o vértice que está sendo claro e o fator quadrático multiplicado pelo quadrado da mesma distância. Os fatores de atenuação padrão são (1,0,0), resultando em nenhuma atenuação.<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Especifica o valor para o que o *parâmetro pname* da luz da fonte *de* luz será definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *light* ou *pname* não era um valor aceito.<br/>                                                                                                                                                                  |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | Um valor expoente spot foi especificado fora do intervalo 0, 128 ou corte spot foi especificado fora do intervalo 0, 90 (exceto pelo valor especial \[ \] \[ 180) ou um fator de atenuação negativo foi \] especificado.<br/> |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/>                                                                                     |



## <a name="remarks"></a>Comentários

A **função glLightiv** define o valor ou os valores de parâmetros de fonte de luz individuais. O *parâmetro light* nomeia a luz e é um nome simbólico do formato GL LIGHT i, em que \_ 0 = i *<* GL MAX \_ \_ LIGHTS.

O *parâmetro pname* especifica um dos parâmetros de fonte de luz, novamente por nome simbólico. O *parâmetro params* é um único valor ou um ponteiro para uma matriz que contém os novos valores.

O cálculo de iluminação é habilitado e desabilitado [**usando glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o argumento GL \_ LIGHTING. Quando a iluminação está habilitada, as fontes de luz habilitadas contribuem para o cálculo de iluminação. A fonte *de luz i* está habilitada e desabilitada usando **glEnable** e **glDisable** com o argumento GL \_ LIGHT *i*.

É sempre o caso de GL \_ LIGHT *i* = GL \_ LIGHT0 + *i*.

As seguintes funções recuperam informações relacionadas à **função glLightiv:**

[**glGetLight**](glgetlight.md)

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ LIGHTING

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





