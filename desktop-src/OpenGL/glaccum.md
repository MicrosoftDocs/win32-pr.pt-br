---
title: função glAccum (GL. h)
description: A função glAccum opera no buffer de acumulação.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- função glAccum OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644761"
---
# <a name="glaccum-function"></a>função glAccum

A função **glAccum** opera no buffer de acumulação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*parar* 
</dt> <dd>

A operação de buffer de acumulação. As constantes simbólicas aceitas são as seguintes.



| Valor                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <dt>**GL \_ Accum**</dt> </dl>    | Obtém R, G, B e valores do buffer selecionado no momento para leitura (consulte [**glReadBuffer**](glreadbuffer.md)). Cada valor de componente é dividido por 2 *n*  1, em que *n* é o número de bits alocados para cada componente de cor no buffer selecionado no momento. O resultado é um valor de ponto flutuante no intervalo de \[ 0, 1 \] , que é multiplicado pelo *valor* e adicionado ao componente de pixel correspondente no buffer de acumulação, atualizando assim o buffer de acumulação.<br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <dt>**\_carga GL**</dt> </dl>       | Semelhante ao GL \_ Accum, exceto pelo fato de que o valor atual no buffer de acumulação não é usado no cálculo do novo valor. Ou seja, os valores R, G, B e a do buffer selecionado atualmente são divididos por 2 *n*  1, multiplicados por *valor* e, em seguida, armazenados na célula de buffer de acumulação correspondente, substituindo o valor atual.<br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <dt>**adição de GL \_**</dt> </dl>          | Adiciona o *valor* a cada R, G, B e a no buffer de acumulação.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <dt>**\_mult GL**</dt> </dl>       | Multiplica cada R, G, B e A no buffer de acumulação por *valor* e retorna o componente dimensionado para seu local de buffer de acumulação correspondente.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <dt>**retorno do GL \_**</dt> </dl> | Transfere valores de buffer de acumulação para o buffer de cores ou buffers selecionados atualmente para gravação. Cada R, G, B e um componente é multiplicado por *valor*, então multiplicado por 2 *n*  1, clamped ao intervalo de \[ 0, 2 *n*  1 \] e armazenado na célula de buffer de exibição correspondente. As únicas operações de fragmento que são aplicadas a essa transferência são propriedade de pixel, mola, pontilhamento e writemasks de cor.<br/>                                                                        |



 

</dd> <dt>

*value* 
</dt> <dd>

Um valor de ponto flutuante usado na operação de buffer de acumulação. O parâmetro *op* determina como o *valor* é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *op* não era um valor aceito.<br/>                                                                                                                                            |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | Não havia um buffer de acumulação ou a função **glAccum** foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

O buffer de acumulação é um buffer de cores de intervalo estendido. As imagens não são renderizadas nela. Em vez disso, as imagens renderizadas em um dos buffers de cor são adicionadas ao conteúdo do buffer de acumulação após a renderização. Você pode criar efeitos como anti-aliasing (de pontos, linhas e polígonos), Desfoque de movimento e profundidade de campo acumulando imagens geradas com matrizes de transformação diferentes.

Cada pixel no buffer de acumulação consiste em valores vermelho, verde, azul e alfa. O número de bits por componente no buffer de acumulação depende da implementação. Você pode examinar esse número chamando [**glGetIntegerv**](glgetintegerv.md) quatro vezes, com os argumentos GL \_ Accum \_ vermelho \_ bits, GL \_ Accum \_ verde \_ bits, GL \_ Accum \_ bits azuis \_ e GL \_ Accum \_ \_ bits alfa, respectivamente. Independentemente do número de bits por componente, no entanto, o intervalo de valores armazenados por cada componente é \[ 1,? 1 \] . Os pixels do buffer de acumulação são mapeados um para um com framebuffer pixels.

A função **glAccum** opera no buffer de acumulação. O primeiro argumento, *op*, é uma constante simbólica que seleciona uma operação de buffer de acumulação. O segundo argumento, *Value*, é um valor de ponto flutuante a ser usado nessa operação. Cinco operações são especificadas: GL \_ Accum, GL \_ upload, GL \_ Add, GL \_ mult, e GL \_ Return.

Todas as operações de buffer de acumulação são limitadas à área da caixa de tesoura atual e são aplicadas de forma idêntica aos componentes vermelho, verde, azul e alfa de cada pixel. O conteúdo de um componente de pixel do buffer de acumulação será indefinido se a operação **glAccum** resultar em um valor fora do intervalo \[ 1, 1 \] .

Para limpar o buffer de acumulação, use a função [**glClearAccum**](glclearaccum.md) para especificar R, G, B e valores para defini-lo e emitir uma função [**glClear**](glclear.md) com o buffer de acumulação habilitado.

Somente os pixels dentro da caixa de tesoura atual são atualizados por qualquer operação **glAccum** .

As funções a seguir recuperam informações relacionadas à função **glAccum** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ accuum \_ \_ bits vermelhos

**glGet** com Argument GL \_ accuum \_ \_ bits verdes

**glGet** com argumento GL \_ Accum \_ \_ bits azuis

**glGet** com Argument GL \_ accuum \_ \_ bits alfa

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





