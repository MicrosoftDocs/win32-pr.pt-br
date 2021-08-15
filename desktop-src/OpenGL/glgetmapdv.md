---
title: Função glGetMapdv (Gl.h)
description: As funções glGetMapdv, glGetMapfv e glGetMapiv retornam parâmetros do avaliador. | Função glGetMapdv (Gl.h)
ms.assetid: 3b4fc03b-ada4-4f4a-a234-fa6439f2e5c8
keywords:
- Função glGetMapdv OpenGL
topic_type:
- apiref
api_name:
- glGetMapdv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1603d87004e9b97e635e5fa6a52efa97c5e760ccd9010aa6f86fc62eb3ee7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360304"
---
# <a name="glgetmapdv-function"></a>Função glGetMapdv

As **funções glGetMapdv**, [**glGetMapfv**](glgetmapfv.md)e [**glGetMapiv**](glgetmapiv.md) retornam parâmetros do avaliador.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetMapdv(
   GLenum   target,
   GLenum   query,
   GLdouble *v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O nome simbólico de um mapa. Os seguintes valores são aceitos: GL \_ MAP1 \_ COLOR \_ 4, GL \_ MAP1 \_ INDEX, GL \_ MAP1 \_ NORMAL, GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD 2, GL \_ \_ \_ MAP1 TEXTURE \_ \_ COORD 3, GL \_ MAP1 TEXTURE \_ \_ \_ COORD 4, GL \_ MAP1 \_ \_ VERTEX 3, GL \_ MAP1 \_ VERTEX \_ 4, GL \_ \_ MAP2 COLOR \_ \_ 4, GL \_ MAP2 INDEX, GL \_ MAP2 \_ NORMAL, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 3, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 \_ VERTEX 3 e \_ GL \_ MAP2 \_ VERTEX \_ 4.

</dd> <dt>

*consulta* 
</dt> <dd>

Especifica qual parâmetro retornar. Os nomes simbólicos a seguir são aceitos.



| Valor                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**GL \_ COEFF**</dt> </dl>    | O *parâmetro v* retorna os pontos de controle para a função do avaliador. Os avaliadores unidimensionais retornam *pontos* de controle de ordem e os avaliadores bidimensionais retornam pontos de controle *uorder* *x* *vorder.* Cada ponto de controle consiste em um, dois, três ou quatro inteiros, valores de ponto flutuante de precisão simples ou de ponto flutuante de precisão dupla, dependendo do tipo do avaliador. Os pontos de controle bidimensionais são retornados em ordem de linha principal, incrementando o *índice uorder* rapidamente e o índice *vorder* após cada linha. Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para os valores inteiros mais próximos.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**GL \_ ORDER**</dt> </dl>    | O *parâmetro v* retorna a ordem da função do avaliador. Os avaliadores unidimensionais retornam um único valor, *ordem*. Os avaliadores bidimensionais retornam dois valores, *uorder* e *vorder.*<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**DOMÍNIO \_ GL**</dt> </dl> | O *parâmetro v* retorna os parâmetros de mapeamento linear *u* e *v.* Os avaliadores unidimensionais retornam dois valores, *u* 1 e *u* 2, conforme especificado por [**glMap1**](glmap1.md). Os avaliadores bidimensionais retornam quatro valores (*u1*, *u2*, *v1* e *v2*) conforme especificado por [**glMap2**](glmap2.md). Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para os valores inteiros mais próximos.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*v* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* ou *query* não era um valor aceito.<br/>                                                                             |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glGetMap** retorna parâmetros do avaliador. (As **funções glMap1** e **glMap2** definem avaliadores.) O *parâmetro* de destino especifica um mapa, *a* consulta seleciona um parâmetro específico e *v* aponta para o armazenamento em que os valores serão retornados.

Os valores aceitáveis para o *parâmetro de* destino são descritos [**em glMap1**](glmap1.md) e [**glMap2.**](glmap2.md)

Se um erro for gerado, nenhuma alteração será feita no conteúdo de *v*.

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





