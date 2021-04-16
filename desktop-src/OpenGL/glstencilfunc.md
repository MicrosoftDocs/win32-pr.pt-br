---
title: função glStencilFunc (GL. h)
description: A função glStencilFunc define a função e o valor de referência para teste de estêncil.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- função glStencilFunc OpenGL
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
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759355"
---
# <a name="glstencilfunc-function"></a>função glStencilFunc

A função **glStencilFunc** define a função e o valor de referência para teste de estêncil.

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
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ nunca**</dt> </dl>          | Sempre falha.<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ menos**</dt> </dl>             | Passa se (  &  *máscara* de referência) < (máscara de *estêncil*  &  ).<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**\_LEQUAL GL**</dt> </dl>       | Passa se (  &  *máscara* de referência) = (máscara de *estêncil*  &  ).<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ maior**</dt> </dl>    | Passa se (  &  *máscara* de referência) > (máscara de *estêncil*  &  ).<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**\_GEQUAL GL**</dt> </dl>       | Passa se (  &  *máscara* de referência) = (máscara de *estêncil*  &  ).<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ igual a**</dt> </dl>          | Passa se (  &  *máscara* de referência) = (máscara de *estêncil*  &  ).<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL não \_ igual**</dt> </dl> | Passa se (  &  *máscara* de referência)? (*estêncil*  &  *Mask*).<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ sempre**</dt> </dl>       | Sempre passa.<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

O valor de referência para o teste de estêncil. O parâmetro *ref* é clamped para o intervalo de \[ 0, 2 *n* 1 \] , em que *n* é o número de bitplanes no buffer de estêncil.

</dd> <dt>

*mascara* 
</dt> <dd>

Uma máscara que é **e** Ed com o valor de referência e o valor de estêncil armazenado quando o teste é concluído.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *Func* não era um dos oito valores aceitos.<br/>                                                                           |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

O estêncil, como o armazenamento em buffer *z*, habilita e desabilita o desenho em uma base por pixel. Você desenha nos planos de estêncil usando primitivas de desenho OpenGL e, em seguida, renderiza a geometria e as imagens, usando os planos de estêncil para mascarar partes da tela. A criação de estêncil normalmente é usada em algoritmos de renderização de passagem multipassadas para obter efeitos especiais, como decals, estrutura de tópicos e renderização de geometria sólida construtivas.

O teste de estêncil elimina condicionalmente um pixel com base no resultado de uma comparação entre o valor de referência e o valor no buffer do estêncil. O teste é habilitado por [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o teste de estêncil do Argument GL \_ \_ . Ações executadas com base no resultado do teste de estêncil são especificadas com [**glStencilOp**](glstencilop.md).

O parâmetro *Func* é uma constante simbólica que determina a função de comparação de estêncil. Ele aceita um dos oito valores mostrados acima. O parâmetro *ref* é um valor de referência de inteiro que é usado na comparação de estêncil. É clamped para o intervalo de \[ 0, 2 *n* 1 \] , em que *n* é o número de bitplanes no buffer de estêncil. O parâmetro *Mask* é bit-a **and** Ed com o valor de referência e o valor de estêncil armazenado, com os valores **e** Ed que participam da comparação.

Se *stencil* representa o valor armazenado no local do buffer de estêncil correspondente, a lista anterior mostra o efeito de cada função de comparação que pode ser especificada por *Func*. Somente se a comparação for realizada com êxito, o pixel passado para o próximo estágio no processo de rasterização (consulte [**glStencilOp**](glstencilop.md)). Todos os testes tratam valores de *estêncil* como inteiros não assinados no intervalo de \[ 0, 2 *n* 1 \] , em que *n* é o número de bitplanes no buffer de estêncil.

Inicialmente, o teste de estêncil está desabilitado. Se não houver nenhum buffer de estêncil, nenhuma modificação de estêncil poderá ocorrer e será como se o teste de estêncil sempre passar.

As funções a seguir recuperam informações relacionadas ao **glStencilFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with o estêncil GL do argumento \_ \_ Func

 máscara de valor de estêncil glGet com Argument GL \_ \_ \_

**glGet** com ref de estêncil do Argument GL \_ \_

**glGet** com bits de estêncil do Argument GL \_ \_

teste de estêncil [**glIsEnabled**](glisenabled.md) com Argument GL \_ \_

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

 

 





