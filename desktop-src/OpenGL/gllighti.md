---
title: função glLighti (GL. h)
description: A função glLighti retorna valores de parâmetro de fonte de luz.
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
keywords:
- função glLighti OpenGL
topic_type:
- apiref
api_name:
- glLighti
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52225c4db8eaa31c17d12a25590b918cf94b4c3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824492"
---
# <a name="gllighti-function"></a>função glLighti

A função **glLighti** retorna valores de parâmetro de fonte de luz.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glLighti(
   GLenum light,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*light* 
</dt> <dd>

O identificador de uma luz. O número de luzes possíveis depende da implementação, mas há suporte para pelo menos oito luzes. Eles são identificados por nomes simbólicos do formulário GL \_ Light *i,* onde *eu* é um valor: 0 a GL \_ número máximo \_ de luzes-1.

</dd> <dt>

*pname* 
</dt> <dd>

Um parâmetro de fonte de luz de valor único para *Light*. Os nomes simbólicos a seguir são aceitos.



| Valor                                                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**\_expoente de spot de GL \_**</dt> </dl>                                                                                                                                                                             | O parâmetro *param* é um único valor inteiro que especifica a distribuição de intensidade da luz. Valores de ponto flutuante e inteiro são mapeados diretamente. Somente os valores no intervalo de \[ 0, 128 \] são aceitos. <br/> A intensidade de luz efetiva é atenuada pelo cosseno do ângulo entre a direção da luz e a direção da luz até o vértice ser iluminado, elevado à potência do expoente Spot. Assim, os expoentes de pontos mais altos resultam em uma fonte de luz mais focada, independentemente do ângulo de corte de spot. O expoente de spot padrão é 0, resultando em distribuição de luz uniforme.<br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**\_corte de spot GL \_**</dt> </dl>                                                                                                                                                                                   | O parâmetro *param* é um único valor inteiro que especifica o ângulo de propagação máximo de uma fonte de luz. Valores de ponto flutuante e inteiro são mapeados diretamente. Somente os valores no intervalo de \[ 0, 90 \] e o valor especial 180 são aceitos. <br/> Se o ângulo entre a direção da luz e a direção da luz até o vértice que está sendo iluminado for maior que o ângulo de corte de spot, a luz será completamente mascarada. Caso contrário, sua intensidade é controlada pelo expoente de spot e pelos fatores de atenuação. O corte de spot padrão é 180, resultando em distribuição de luz uniforme.<br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**atenuação constante do GL, atenuação linear do GL \_ \_ \_ \_ , \_ atenuação quadrática do GL \_**</dt> </dl> | O parâmetro *param* é um valor inteiro único que especifica um dos três fatores de atenuação leves. Valores de ponto flutuante e inteiro são mapeados diretamente. Somente valores não negativos são aceitos. <br/> Se a luz for posicional, em vez de direcional, sua intensidade será atenuada pelo recíproco da soma de: o fator de constante, o fator linear multiplicado pela distância entre a luz e o vértice que está sendo iluminado, e o fator quadrática multiplicado pelo quadrado da mesma distância. Os fatores de atenuação padrão são (1, 0, 0), resultando em nenhuma atenuação.<br/>                   |



 

</dd> <dt>

*param* 
</dt> <dd>

Especifica o valor para o qual o parâmetro *pname* da *luz* da fonte de luz será definido como.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *Light* ou *pname* não era um valor aceito.<br/>                                                                                                                                                                  |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | Um valor de expoente de spot foi especificado fora do intervalo \[ 0, 128 \] ou o corte de spot foi especificado fora do intervalo \[ 0, 90 \] (exceto pelo valor especial 180) ou um fator atenuante negativo foi especificado.<br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>                                                                                     |



## <a name="remarks"></a>Comentários

A função **glLighti** define o valor ou os valores de parâmetros de fonte de luz individuais. O parâmetro *Light* nomeia a luz e é um nome simbólico do formulário GL \_ Light *i*, em que 0 = *i* < GL \_ Max \_ acende.

O parâmetro *pname* especifica um dos parâmetros de origem da luz, novamente pelo nome simbólico. O parâmetro *param* é um único valor ou um ponteiro para uma matriz que contém os novos valores.

O cálculo de iluminação é habilitado e desabilitado usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com a iluminação do Argument GL \_ . Quando a iluminação está habilitada, as fontes de luz habilitadas contribuem para o cálculo de iluminação. Fonte de luz *eu estou* habilitada e desabilitada usando **glEnable** e **glDisable** com o argumento GL \_ Light *i*.

É sempre o caso que o GL \_ Light *i* = GL \_ LIGHT0 + *i*.

As funções a seguir recuperam informações relacionadas à função **glLighti** :

[**glGetLight**](glgetlight.md)

[**glIsEnabled**](glisenabled.md) com iluminação do argumento GL \_

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





