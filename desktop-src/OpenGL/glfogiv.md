---
title: Função glFogiv (Gl.h)
description: A função glFogiv especifica parâmetros de parâmetros de parâmetros de parâmetro. | Função glFogiv (Gl.h)
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
keywords:
- Função glFogiv OpenGL
topic_type:
- apiref
api_name:
- glFogiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4e22fddbd6c89a219c296c4fa0161f3992be195a91b38ab512c493241430fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061659"
---
# <a name="glfogiv-function"></a>Função glFogiv

A **função glFogfv** especifica parâmetros de parâmetros de parâmetros de parâmetro.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glFogiv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

Especifica um parâmetro de parâmetro de parâmetro de parâmetro.

Aceita um dos valores a seguir.



| Valor                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**MODO \_ GL MODE \_**</dt> </dl>          | O *parâmetro params* é um único valor inteiro que especifica a equação a ser usada para calcular o fator de mesclagem do blend, *f*. Três constantes simbólicas são aceitas: GL \_ LINEAR, GL \_ EXP e GL \_ EXP2. As equações correspondentes a essas constantes simbólicas são definidas na seção Comentários a seguir. O modo de redução padrão é GL \_ EXP.<br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**DENSIDADE \_ GL BP \_**</dt> </dl> | O *parâmetro params* é um único valor inteiro que especifica a densidade *,* a densidade de densidade usada em ambas as equações de equação exponencial. Somente as densidades não associativas são aceitas. A densidade de 1.0 padrão é de 1.0.<br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**GL \_ BP \_ START**</dt> </dl>       | O *parâmetro params* é um único valor inteiro que especifica *start*, a distância próxima usada na equação linear de equação de equação. A distância próxima padrão é 0,0.<br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**GL \_ BP \_ END**</dt> </dl>             | O *parâmetro params* é um único valor inteiro que especifica *end*, a distância distante usada na equação linear da equação de equações lineares. A distância padrão é 1,0.<br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**GL \_ FOG \_ INDEX**</dt> </dl>       | O *parâmetro params* é um único valor inteiro que especifica *i*<sub>f</sub> , o índice de cor de cinza. O índice de 100% padrão é 0,0.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <dt>**COR \_ GL COLOR \_**</dt> </dl>       | O *parâmetro params* contém quatro valores inteiros ou de ponto flutuante que *especificam C*<sub>f</sub> , a cor da cinza. Os valores inteiros são mapeados linearmente de modo que o valor representável mais positivo seja mapeado para 1,0 e o valor representável mais negativo seja mapeado para -1,0. Os valores de ponto flutuante são mapeados diretamente. Após a conversão, todos os componentes de cor são fixados no intervalo \[ 0,1 \] . A cor padrão da coloração é (0,0,0,0).<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Especifica o valor ou os valores a serem atribuídos ao *pname.* GL \_ COLOR EXIGE uma matriz de quatro \_ valores. Todos os outros parâmetros aceitam uma matriz que contém apenas um único valor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *pname* não era um valor aceito.<br/>                                                                                         |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

Você habilita e desabilita [**a função com glEnable**](glenable.md) e [**glDisable**](gldisable.md)usando o argumento GL \_ GL GL. Enquanto habilitada, a geometria rasterizada, os bitmaps e os blocos de pixel, mas não as operações de limpar buffer.

A **função glFogiv** atribui o valor ou os valores em *parâmetros params* ao parâmetro de parâmetro especificado por *pname*.

O blend combina uma cor de cinza com a cor pós-texto de cada fragmento de pixel rasterizado usando um fator de *mesclagem f*. O *fator f* é calculado de uma das três maneiras, dependendo do modo de modo de espera. Deixe *z* ser a distância nas coordenadas de olho da origem para o fragmento que está sendo destruído. A equação para o brilho \_ LINEAR GL é:

![Equação mostrando o valor do fator de mesclagem GL_LINEAR modo de métrica como uma função de distância.](images/fog01.png)

A equação para GL \_ EXP é:

![Equação mostrando o valor do fator de mesclagem no GL_EXP modo de métrica.](images/fog02.png)

A equação para GL \_ EXP2 é:

![Equação mostrando o valor do fator de mesclagem no GL_EXP2 modo de métrica.](images/fog03.png)

Independentemente do modo de ressarpetivo, *f* é fixado ao intervalo \[ 0,1 \] depois de computado. Em seguida, se OpenGL estiver no modo de cor RGBA, a cor do fragmento *C*<sub>r</sub> será substituída por

![Equação mostrando a cor do fragmento colorido como uma função da combinação de fator e cor da coloração.](images/fog04.png)

No modo de índice de cores, o índice de cores do fragmento *é*<sub></sub> substituído por

![Equação que mostra o índice de cores do fragmento colorido como uma função do fator de mesclagem e da cor indexada.](images/fog05.png)

As funções a seguir recuperam informações relacionadas às **funções glFog:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ COLOR \_

**glGet** com o argumento GL \_ INDEX \_

**glGet** com o argumento GL \_ BP \_ DENSITY

**glGet** com o argumento GL \_ BP \_ START

**glGet** com o argumento GL \_ BP \_ END

**glGet** com o argumento GL \_ MODE \_

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ BP

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





