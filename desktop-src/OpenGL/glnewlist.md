---
title: função glNewList (GL. h)
description: As funções glNewList e glEndList criam ou substituem uma lista de exibição. | função glNewList (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- função glNewList OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105755980"
---
# <a name="glnewlist-function"></a>função glNewList

As funções **glNewList** e [**glEndList**](glendlist.md) criam ou substituem uma lista de exibição.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*list* 
</dt> <dd>

O nome da lista de exibição.

</dd> <dt>

*mode* 
</dt> <dd>

O modo de compilação. Os valores a seguir são aceitos.



| Valor                                                                                                                                                                                      | Significado                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <dt>**\_compilação GL**</dt> </dl>                                       | Os comandos são meramente compilados.<br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <dt>**GL \_ Compilar \_ e \_ executar**</dt> </dl> | Os comandos são executados conforme são compilados na lista de exibição.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *lista* era zero.<br/>                                                                                                           |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

As listas de exibição são grupos de comandos OpenGL que foram armazenados para execução subsequente. As listas de exibição são criadas com **glNewList**. Todos os comandos subsequentes são colocados na lista de exibição, na ordem emitida, até que **glEndList** seja chamado.

A função **glNewList** tem dois parâmetros. O primeiro parâmetro, *lista*, é um inteiro positivo que se torna o nome exclusivo da lista de exibição. Os nomes podem ser criados e reservados com [**glGenLists**](glgenlists.md) e testados para exclusividade com [**glIsList**](glislist.md). O segundo parâmetro, *Mode*, é uma constante simbólica que pode assumir um dos dois valores anteriores.

Determinados comandos não são compilados na lista de exibição, mas são executados imediatamente, independentemente do modo da lista de exibição. Esses comandos são [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**GlIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)e todas as rotinas de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .

Da mesma forma, [**glTexImage2D**](glteximage2d.md) e [**glTexImage1D**](glteximage1d.md) são executados imediatamente e não são compilados na lista de exibição quando seu primeiro argumento \_ é GL de proxy \_ \_ \_ \_ \_

Quando a função **glEndList** é encontrada, a definição da lista de exibição é concluída pela Associação da lista com a *lista* de nomes exclusivas (especificada no comando **glNewList** ). Se já existir uma lista de exibição com a *lista* de nomes, ela será substituída somente quando **glEndList** for chamado.

As funções [**glCallList**](glcalllist.md) e [**glCallLists**](glcalllists.md) podem ser inseridas em listas de exibição. Os comandos na lista de exibição ou listas executadas por **glCallList** ou **glCallLists** não são incluídos na lista de exibição que está sendo criada, mesmo que o modo de criação de lista seja GL \_ Compilar \_ e \_ executar.

A função a seguir recupera informações relacionadas a **glNewList**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEndList**](glendlist.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> </dl>

 

 





