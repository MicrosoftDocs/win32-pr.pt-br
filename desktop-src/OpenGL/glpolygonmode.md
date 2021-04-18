---
title: função glPolygonMode (GL. h)
description: A função glPolygonMode seleciona um modo de rasterização de polígono.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- função glPolygonMode OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756394"
---
# <a name="glpolygonmode-function"></a>função glPolygonMode

A função **glPolygonMode** seleciona um modo de rasterização de polígono.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sorridente* 
</dt> <dd>

Os polígonos aos quais o *modo* se aplica. Deve ser o GL \_ frontal para polígonos frontais, o GL \_ volta para polígonos traseiros ou o GL \_ frontal \_ e \_ posterior para polígonos frontais e traseiros.

</dd> <dt>

*mode* 
</dt> <dd>

A maneira como os polígonos serão rasterizados. Os modos a seguir são definidos e podem ser especificados no *modo*. O padrão é que o GL é \_ preenchido para polígonos frente e verso.



| Valor                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <dt>**\_ponto GL**</dt> </dl> | Os vértices do polígono marcados como o início de uma borda de limite são desenhados como pontos. Atributos de ponto como \_ \_ o tamanho do ponto GL \_ e \_ o ponto GL insuaves controlam a rasterização dos pontos. Os atributos de rasterização de polígono diferentes do \_ modo de polígono GL \_ não têm nenhum efeito.<br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <dt>**\_linha GL**</dt> </dl>    | As bordas de limite do polígono são desenhadas como segmentos de linha. Eles são tratados como segmentos de linha conectados para a linha stippling; o contador de Stipple de linha e o padrão não são redefinidos entre os segmentos (consulte [**glLineStipple**](gllinestipple.md)). Atributos de linha como \_ \_ a largura da linha gl \_ e \_ o controle Smooth de linha gl a rasterização das linhas. Os atributos de rasterização de polígono diferentes do \_ modo de polígono GL \_ não têm nenhum efeito.<br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <dt>**preenchimento do GL \_**</dt> </dl>    | O interior do polígono é preenchido. Atributos Polygon, como GL \_ Polygon \_ STIPPLE e GL \_ poligonal \_ controle Smooth a rasterização do polígono.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | A *face* ou o *modo* não era um valor aceito.<br/>                                                                         |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glPolygonMode** controla a interpretação de polígonos para rasterização. O parâmetro *facial* descreve a qual *modo* polígonos se aplica: polígonos (front-end \_ ), polígonos voltados (GL \_ traseiro) ou ambos (GL \_ frontal \_ e \_ posterior). O modo Polygon afeta apenas a rasterização final de polígonos. Em particular, os vértices de um polígono estão acesos e o polígono é recortado e possivelmente refigurados antes que esses modos sejam aplicados.

Para desenhar uma superfície com polígonos voltados para trás e com sublinhado polígonos, chame

**glPolygonMode**(GL \_ frontal, \_ linha GL);

Os vértices são marcados como limite ou não restritos com um sinalizador de borda. Os sinalizadores de borda são gerados internamente pelo OpenGL quando decompõem polígonos e podem ser definidos explicitamente usando [**glEdgeFlag**](gledgeflag-functions.md).

A função a seguir recupera informações relacionadas a **glPolygonMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com modo de polígono do Argument GL \_ \_

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

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





