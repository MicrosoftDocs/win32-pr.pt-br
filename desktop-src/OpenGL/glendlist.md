---
title: função glEndList (GL. h)
description: As funções glNewList e glEndList criam ou substituem uma lista de exibição. | função glEndList (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- função glEndList OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105780196"
---
# <a name="glendlist-function"></a>função glEndList

As funções [**glNewList**](glnewlist.md) e **glEndList** criam ou substituem uma lista de exibição.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Significado                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | **glEndList** foi chamado sem um **glNewList** anterior ou se **glNewList** foi chamado enquanto uma lista de exibição estava sendo definida.<br/> |



## <a name="remarks"></a>Comentários

As listas de exibição são grupos de comandos OpenGL que foram armazenados para execução subsequente. As listas de exibição são criadas com [**glNewList**](glnewlist.md). Todos os comandos subsequentes são colocados na lista de exibição, na ordem emitida, até que **glEndList** seja chamado.

A função [**glNewList**](glnewlist.md) tem dois parâmetros. O primeiro parâmetro, *lista*, é um inteiro positivo que se torna o nome exclusivo da lista de exibição. Os nomes podem ser criados e reservados com [**glGenLists**](glgenlists.md) e testados para exclusividade com [**glIsList**](glislist.md). O segundo parâmetro, *Mode*, é uma constante simbólica que pode assumir um dos dois valores anteriores.

Determinados comandos não são compilados na lista de exibição, mas são executados imediatamente, independentemente do modo da lista de exibição. Esses comandos são [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**GlIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)e todas as rotinas de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .

Da mesma forma, [**glTexImage2D**](glteximage2d.md) e [**glTexImage1D**](glteximage1d.md) são executados imediatamente e não são compilados na lista de exibição quando seu primeiro argumento \_ é GL de proxy \_ \_ \_ \_ \_

Quando a função **glEndList** é encontrada, a definição da lista de exibição é concluída pela Associação da lista com a *lista* de nomes exclusivas (especificada no comando [**glNewList**](glnewlist.md) ). Se já existir uma lista de exibição com a *lista* de nomes, ela será substituída somente quando **glEndList** for chamado.

As funções [**glCallList**](glcalllist.md) e [**glCallLists**](glcalllists.md) podem ser inseridas em listas de exibição. Os comandos na lista de exibição ou listas executadas por **glCallList** ou **glCallLists** não são incluídos na lista de exibição que está sendo criada, mesmo que o modo de criação de lista seja GL \_ Compilar \_ e \_ executar.

A função a seguir recupera informações relacionadas a [**glNewList**](glnewlist.md):

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

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





