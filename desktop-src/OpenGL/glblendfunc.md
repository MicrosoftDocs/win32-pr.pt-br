---
title: função glBlendFunc (GL. h)
description: A função glBlendFunc especifica a aritmética de pixel.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- função glBlendFunc OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4b079d0eb83f401eb7e906cb399fab18e5b2fd22f06299fcc62b1e6b4a02e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082126"
---
# <a name="glblendfunc-function"></a>função glBlendFunc

A função **glBlendFunc** especifica a aritmética de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sfactor* 
</dt> <dd>

Especifica como os fatores de mistura de origem em vermelho, verde, azul e alfa são computados. Nove constantes simbólicas são aceitas: GL \_ zero, GL \_ One, GL \_ DST \_ Color, GL \_ um \_ menos a \_ \_ cor de DST, GL \_ src \_ alfa, GL \_ um \_ menos \_ src \_ Alpha, GL \_ DST \_ Alpha, GL \_ um \_ menos \_ DST \_ alfa e GL \_ src \_ Alpha \_ saturação.

</dd> <dt>

*dfactor* 
</dt> <dd>

Especifica como os fatores de mesclagem de destino vermelho, verde, azul e alfa são computados. Oito constantes simbólicas são aceitas: GL \_ zero, GL \_ One, GL \_ src \_ Color, GL \_ um \_ menos a \_ \_ cor src, GL \_ src \_ alfa, GL \_ um \_ menos \_ src \_ Alpha, GL \_ DST \_ Alpha e GL \_ um \_ menos \_ DST \_ Alpha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *Sfactor* ou *dfactor* não era um valor aceito.<br/>                                                                   |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

No modo RGB, os pixels podem ser desenhados usando uma função que combina os valores de RGBA de entrada (origem) com os valores RGBA que já estão no framebuffer (os valores de destino). Por padrão, a mesclagem está desabilitada. Use [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o \_ argumento GL Blend para habilitar e desabilitar a mesclagem.

Quando habilitado, **glBlendFunc** define a operação de mesclagem. O parâmetro *sfactor* especifica qual dos nove métodos é usado para dimensionar os componentes de cor de origem. O parâmetro *dfactor* especifica qual dos oito métodos é usado para dimensionar os componentes de cor de destino. Os onze métodos possíveis são descritos na tabela a seguir. Cada método define quatro fatores de escala, um para vermelho, verde, azul e alfa.

Na tabela e nas equações subsequentes, os componentes de cor de origem e de destino são chamados de (*R*? , *G*? , *B*? , *Um*? ) e (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ). Eles são compreendidos para ter valores inteiros entre zero e (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>r</sub> , *k*<sub>A</sub> ), em que

*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1

*k*<sub>g</sub> = 2 <sup>m</sup>*G* -1

*k*<sub>b</sub> = 2 <sup>m</sup>*B* -1

*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1

e (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>a</sub> ) é o número de bitplanes vermelho, verde, azul e alfa.

Os fatores de escala de origem e destino são referidos como (*s*<sub>r</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>a</sub> ) e (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>a</sub> ). Os fatores de escala descritos na tabela, denotados (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), representam fatores de origem ou de destino. Todos os fatores de escala têm o intervalo \[ de 0, 1 \] .



| Parâmetro                  | (*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ zero                   | (0,0,0,0)                                                                                                                                                    |
| GL \_ um                    | (1, 1, 1, 1)                                                                                                                                                    |
| \_cor de src GL \_             | (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ um \_ menos \_ cor de src \_ | (1, 1, 1, 1)-(*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                             |
| \_cor de DST do GL \_             | (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>G</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )             |
| GL \_ um \_ menos \_ cor do DST \_ | (1, 1, 1, 1)-(*r*<sub>d</sub>  /  *k*<sub>r</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> ) |
| \_origem GL \_ alfa             | (*A*? / *k*<sub>a</sub> , *A*? / *k*<sub>a</sub> , *A*? / *k*<sub>a</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ um \_ menos \_ src \_ Alpha | (1, 1, 1, 1)-(*A*? / *k*<sub>a</sub> , *A*? / *k*<sub>a</sub> , *A*? / *k*<sub>a</sub> , *A*? / *k*<sub>A</sub> )                                             |
| GL \_ DST \_ Alpha             | (*A*<sub>d</sub>  /  *k*<sub>a</sub> , *a d* k a, a <sub>d k a</sub>  /  <sub></sub> <sub></sub>  /  <sub></sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )             |
| GL \_ um \_ menos o \_ DST \_ Alpha | (1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , *a d k*<sub></sub>  /  <sub></sub> <sub></sub>  /  <sub></sub> <sub></sub>  /  <sub></sub> a, a d k a) |
| GL \_ src \_ alfa \_ saturado   | (*i, i, i,* 1)                                                                                                                                                 |



 

Na tabela,

*i* = min (*A*? , *k*<sub>a</sub>   -  <sub>d</sub> )/ *k*<sub>A</sub>

Para determinar os valores de RGBA misturados de um pixel ao desenhar no modo RGBA, o sistema usa as seguintes equações:

*R* (*d*) = min ( *k*<sub>r</sub> , *r*? *s*<sub>r r</sub>  +  <sub>d</sub> <sub></sub> r)

*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  *g*<sub>d</sub> <sub>g</sub> )

*B* (*d*) = min ( *k*<sub>b</sub> *, B*? *s*<sub>b</sub>  +  *b*<sub>d</sub> *b*<sub></sub> )

*A* (*d*) = min ( *k*<sub>A</sub> , *A*? *a*<sub></sub>  +  <sub>d</sub> *d*<sub></sub> a)

Apesar da precisão aparente das equações acima, a aritmética de mistura não é exatamente especificada, pois a mesclagem opera com valores de cor de inteiros imprecisos. No entanto, um fator de mistura que deve ser igual a um está garantido para não modificar seu multiplicando, e um fator de mistura igual a zero reduz seu multiplicando para zero. Portanto, por exemplo, quando *sfactor* é GL \_ src \_ Alpha, *dfactor* é GL \_ um \_ menos \_ src \_ alfa e *a*? é igual a *k*<sub>a</sub>, as equações são reduzidas para substituição simples:

*R*<sub>d</sub>  =  *r*?

*G*<sub>d</sub>  =  *g*?

B <sub>d</sub>  =  *b*?

*A*<sub>d</sub>  =  *A*?

## <a name="examples"></a>Exemplos

A transparência é melhor implementada usando **glBlendFunc**(GL \_ SRC \_ ALPHA, GL \_ ONE MINUS \_ SRC ALPHA) com \_ \_ primitivos organizados do mais distante para o mais próximo. Observe que esse cálculo de transparência não requer a presença de bitplanes alfa no framebuffer.

Você também pode usar **glBlendFunc**(GL SRC ALPHA, GL ONE MINUS SRC ALPHA) para renderizar pontos e linhas \_ \_ \_ \_ \_ \_ antialiasdos em ordem arbitrária.

Para otimizar a antialiação de polígono, use **glBlendFunc**(GL \_ SRC \_ ALPHA \_ SATURATE, GL ONE) com polígonos classificação do mais próximo ao \_ mais distante. (Consulte o GL \_ Argumento \_ POLYGON SMOOTH [**em glEnable para**](glenable.md) obter informações sobre suavização de polígono.) Os bitplanes alfa de destino, que devem estar presentes para que essa função blend opere corretamente, armazene a cobertura acumulada.

O alfa de entrada (origem) é uma opacidade de material, variando de 1,0 (*K*<sub>A</sub> ), representando opacidade completa, a 0,0 (0), representando transparência completa.

Quando você habilita mais de um buffer de cores para desenho, cada buffer habilitado é mesclado separadamente e o conteúdo do buffer é usado para a cor de destino. (Consulte [**glDrawBuffer**](gldrawbuffer.md).)

A combinação afeta apenas a renderização RGBA. Ele é ignorado por renderadores de índice de cores.

As seguintes funções recuperam informações relacionadas **a glBlendFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ BLEND \_ SRC

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ BLEND \_ DST

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ BLEND

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





