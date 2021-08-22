---
title: Função glStencilFunc (Gl.h)
description: A função glStencilFunc define a função e o valor de referência para teste de estêncil.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- Função glStencilFunc OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e529bd83cff8ffb25c8853b7d896926e63982370387f7e2fb5d2ca30a394c1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491506"
---
# <a name="glstencilfunc-function"></a>Função glStencilFunc

A **função glStencilFunc** define a função e o valor de referência para teste de estêncil.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*func* 
</dt> <dd>

A função de teste. Os oito tokens a seguir são válidos.



| Valor                                                                                                                                                   | Significado                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ NEVER**</dt> </dl>          | Sempre falha.<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | Passa se (*máscara*  &  *ref*) < (*máscara de estêncil*  &  ).<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Passa se (*ref*  &  *mask*) = (*máscara de estêncil*  &  ).<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ GREATER**</dt> </dl>    | Passa se (*máscara*  &  *ref*) > (*máscara de estêncil*  &  ).<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Passa se (*ref*  &  *mask*) = (*máscara de estêncil*  &  ).<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ EQUAL**</dt> </dl>          | Passa se (*ref*  &  *mask*) = (*máscara de estêncil*  &  ).<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | Passa se (*ref*  &  *mask*) ? (*estêncil*  &  *mask*).<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ ALWAYS**</dt> </dl>       | Sempre passa.<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

O valor de referência para o teste de estêncil. O *parâmetro ref* é fixado ao intervalo \[ 0, 2 *n* 1, em que n é o número de \] bitplanes no buffer de estêncil. 

</dd> <dt>

*mask* 
</dt> <dd>

Uma máscara que é **AND** ed com o valor de referência e o valor de estêncil armazenado quando o teste é feito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *func* não era um dos oito valores aceitos.<br/>                                                                           |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A cerca, como *z*-buffering, habilita e desabilita o desenho por pixel. Você desenha nos planos de estêncil usando primitivos de desenho OpenGL e, em seguida, renderiza geometria e imagens, usando os planos de estêncil para mascarar partes da tela. Normalmente, a estrutura é usada em algoritmos de renderização multipasso para obter efeitos especiais, como decalques, estrutura de estrutura de estrutura e renderização de geometria sólida construtiva.

O teste de estêncil elimina condicionalmente um pixel com base no resultado de uma comparação entre o valor de referência e o valor no buffer de estêncil. O teste é habilitado por [**glEnable e**](glenable.md) [**glDisable com**](gldisable.md) o argumento GL \_ STENCIL \_ TEST. As ações realizadas com base no resultado do teste de estêncil são especificadas com [**glStencilOp**](glstencilop.md).

O *parâmetro func* é uma constante simbólica que determina a função de comparação de estêncil. Ele aceita um dos oito valores mostrados acima. O *parâmetro ref* é um valor de referência de inteiro que é usado na comparação de estêncil. Ele é fixado no intervalo \[ 0, 2 *n* 1, em que n é o número de \] bitplanes no buffer de estêncil.  O *parâmetro* mask é **AND** bit a bit com o valor de referência e o valor de estêncil armazenado, com os valores **AND** ed participando da comparação.

Se *o estêncil* representar o valor armazenado no local do buffer de estêncil correspondente, a lista anterior mostrará o efeito de cada função de comparação que pode ser especificada pelo *func*. Somente se a comparação for bem-sucedida é o pixel passado para o próximo estágio no processo de rasterização (consulte [**glStencilOp**](glstencilop.md)). Todos os testes tratam valores de *estêncil* como inteiros sem sinal no intervalo 0, 2 n 1 , em que n é o número de \[ bitplanes no buffer de \] estêncil. 

Inicialmente, o teste de estêncil está desabilitado. Se não houver nenhum buffer de estêncil, nenhuma modificação de estêncil poderá ocorrer e será como se o teste de estêncil sempre fosse aprovado.

As seguintes funções recuperam informações relacionadas **a glStencilFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ STENCIL \_ FUNC

**glGet** com o argumento GL \_ STENCIL \_ VALUE \_ MASK

**glGet** com argumento GL \_ STENCIL \_ REF

**glGet** com o argumento GL \_ STENCIL \_ BITS

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ STENCIL \_ TEST

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





