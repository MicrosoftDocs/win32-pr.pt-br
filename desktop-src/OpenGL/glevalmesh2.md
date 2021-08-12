---
title: função glEvalMesh2 (GL. h)
description: Computa uma grade bidimensional de pontos ou linhas.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- função glEvalMesh2 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5f1a16b1ceda2c13f24a779032b0e920d364db46167a9dc02ca2b27277262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616102"
---
# <a name="glevalmesh2-function"></a>função glEvalMesh2

Computa uma grade bidimensional de pontos ou linhas.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

Um valor que especifica se deve-se computar uma malha bidimensional de pontos, linhas ou polígonos. As seguintes constantes simbólicas são aceitas: GL \_ Point, GL \_ line e GL \_ Fill.

</dd> <dt>

*I1* 
</dt> <dd>

O primeiro valor inteiro para a variável de domínio de grade i.

</dd> <dt>

*i2* 
</dt> <dd>

O último valor inteiro para a variável de domínio de grade i.

</dd> <dt>

*j1* 
</dt> <dd>

O primeiro valor inteiro para a variável de domínio de grade j.

</dd> <dt>

*j2* 
</dt> <dd>

O último valor inteiro para a variável de domínio de grade j.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | Indica que o *modo* não é um valor aceito. <br/>                                                                            |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md). <br/> |



## <a name="remarks"></a>Comentários

Use [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) em tandem para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme. A função **glEvalMesh** percorre o domínio inteiro de uma grade de uma ou duas dimensões, cujo intervalo é o domínio dos mapas de avaliação especificados por [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md). O parâmetro mode determina se os vértices resultantes são conectados como pontos, linhas ou polígonos preenchidos.

No caso bidimensional, **glEvalMesh2**, Let

? u = (U2 U1)/n

? v = (v2 v1)/m,

em que n, U1, U2, m, v1 e v2 são os argumentos para a função [**glMapGrid2**](glmapgrid-functions.md) mais recente. Em seguida, se *Mode* for GL \_ Fill, **glEvalMesh2** será equivalente a:

para (j = J1; j < J2; j + = 1)

{

[**glBegin**](glbegin.md)(GL \_ Quad \_ strip);

for (i = i1; i <= i2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), j? v + v1);

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), (j + 1)? v + v1);

}

[**glEnd**](glend.md)(); }

Se *Mode* for uma \_ linha gl, uma chamada para **glEvalMesh2** será equivalente a:

para (j = J1; j <= J2; j + = 1)

{

[**glBegin**](glbegin.md)( \_ faixa de linha gl \_ );

for (i = i1; i <= i2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

[**glEnd**](glend.md)();

}

for (i = i1; i <= i2; i + = 1)

{

[**glBegin**](glbegin.md)( \_ faixa de linha gl \_ );

para (j = J1; j <= J1; j + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

glEnd( );

}

E, finalmente, se *Mode* for um \_ ponto GL, uma chamada para **glEvalMesh2** será equivalente a:

[**glBegin**](glbegin.md)( \_ pontos GL);

para (j = J1; j <= J2; j + = 1)

{

for (i = i1; i <= i2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

}

[**glEnd**](glend.md)();

Em todos os três casos, os únicos requisitos numéricos absolutos são que, se eu = n, o valor calculado a partir de i? u + U1 é exatamente U2 e, se j = m, o valor calculado a partir de j? o v + v1 é exatamente v2. As funções a seguir recuperam informações relacionadas a **glEvalMesh**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP1 \_ grade \_ Domain

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ map2 \_ grade \_ Domain

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ MAP1 \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ map2 \_ \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

 





