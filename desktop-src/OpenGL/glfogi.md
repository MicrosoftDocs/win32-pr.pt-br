---
title: Função glFogi (Gl.h)
description: A função glFogi especifica parâmetros de neblina.
ms.assetid: c2ffb41d-3d97-4b72-b16d-cfbffa1179d1
keywords:
- função glFogi OpenGL
topic_type:
- apiref
api_name:
- glFogi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc718a007035204f6e984eea87f1e21ba09ac8f0
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103837551"
---
# <a name="glfogi-function"></a>função glFogi

A função **glFogi** especifica parâmetros de neblina.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glFogi(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* 
</dt> <dd>

Especifica um parâmetro de neblina de valor único.

Aceita um dos valores a seguir.



| Valor                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**\_modo de neblina GL \_**</dt> </dl>          | O parâmetro *params* é um único valor inteiro que especifica a equação a ser usada para calcular o fator de mistura de neblina, *f*. Três constantes simbólicas são aceitas: GL \_ linear, GL \_ exp e GL \_ EXP2. As equações correspondentes a essas constantes simbólicas são definidas na seção comentários a seguir. O modo de neblina padrão é GL \_ exp.<br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**\_densidade de neblina GL \_**</dt> </dl> | O parâmetro *params* é um único valor inteiro que especifica a *densidade*, a densidade de neblina usada em equações de neblina exponencial. Somente as densidades não negativas são aceitas. A densidade de neblina padrão é 1,0.<br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**\_início da neblina do GL \_**</dt> </dl>       | O parâmetro *params* é um único valor inteiro que especifica *Start*, a distância próxima usada na equação de neblina linear. O padrão próximo à distância é de 0,0.<br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**\_fim da neblina do GL \_**</dt> </dl>             | O parâmetro *params* é um único valor inteiro que especifica *end*, a distância mais usada na equação de neblina linear. A distância padrão é 1,0.<br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**\_índice de neblina GL \_**</dt> </dl>       | O parâmetro *params* é um único valor inteiro que especifica *i*<sub>f</sub> , o índice de cores de neblina. O índice de neblina padrão é 0,0.<br/>                                                                                                                                                                                                           |



 

</dd> <dt>

*param* 
</dt> <dd>

Especifica o valor para o qual *pname* será definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *pname* não era um valor aceito.<br/>                                                                                         |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Você habilita e desabilita a neblina com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), usando o argumento GL \_ neblina. Enquanto habilitado, a neblina afeta a geometria, os bitmaps e os blocos de pixels rasterizados, mas não as operações de limpeza de buffer.

A função **glFogi** atribui o valor ou valores em *params* para o parâmetro de neblina especificado por *pname*.

A neblina combina uma cor de neblina com cada cor de posttexturing do fragmento de pixel rasterizado usando um fator de mistura *f*. O fator *f* é calculado de uma das três maneiras, dependendo do modo de neblina. Deixe que *z* seja a distância em coordenadas de olho da origem para o fragmento sendo fogged. A equação para a \_ neblina linear do GL é:

![Equação mostrando o valor de GL_LINEAR neblina.](images/fog01.png)

A equação para o GL \_ exp neblina é:

![Equação mostrando o valor do fator de mesclagem no modo GL_EXP neblina.](images/fog02.png)

A equação para o GL \_ EXP2 neblina é:

![Equação mostrando o valor do fator de mesclagem no modo GL_EXP2 neblina.](images/fog03.png)

Independentemente do modo de neblina, *f* é clamped para o intervalo de \[ 0, 1 \] após ser computado. Em seguida, se OpenGL estiver no modo de cor RGBA, a cor *C*<sub>r</sub> do fragmento será substituída por

![Equação mostrando a cor do fragmento fogged como uma função de fator de mesclagem e cor de neblina.](images/fog04.png)

No modo de índice de cor, o índice de cores do fragmento *i*<sub>r</sub> é substituído por

![Equação mostrando o índice de cores do fragmento fogged como uma função de fator de mesclagem e cor indexada.](images/fog05.png)

As funções a seguir recuperam informações relacionadas às funções **glFog** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a \_ cor de neblina do argumento GL \_

**glGet** com índice de neblina do argumento GL \_ \_

**glGet** com densidade de neblina de Argument GL \_ \_

início da sombra do **glGet** com Argument GL \_ \_

**glGet** com término da neblina do argumento GL \_ \_

**glGet** com o \_ modo de sombra do argumento GL \_

[**glIsEnabled**](glisenabled.md) com sombra do argumento GL \_

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

 

 





