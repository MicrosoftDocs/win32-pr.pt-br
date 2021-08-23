---
title: Função glTexCoord4dv (Gl.h)
description: Define as coordenadas de textura atuais. | Função glTexCoord4dv (Gl.h)
ms.assetid: 43d3fb1c-c1cf-4f81-aac2-24a5b4c5b29d
keywords:
- Função glTexCoord4dv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d5e2fdfb25d11c2834de3b4cbe164baf3b830e4557ebbdcb0e7792f0ef4252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777836"
---
# <a name="gltexcoord4dv-function"></a>Função glTexCoord4dv

Define as coordenadas de textura atuais.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexCoord4dv(
   const GLdouble *v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*v* 
</dt> <dd>

Um ponteiro para uma matriz de quatro elementos, que, por sua vez, especifica as coordenadas de textura s, t, r e q.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A [**função glTexCoord**](gltexcoord-functions.md) define as coordenadas de textura atuais que fazem parte dos dados associados aos vértices de polígono. A **função glTexCoord** especifica coordenadas de textura em uma, duas, três ou quatro dimensões. A função glTexCoord1 define as coordenadas de textura atuais como (s, 0, 0, 1); uma chamada para glTexCoord2 os define como (s, t, 0, 1). Da mesma forma, glTexCoord3 especifica as coordenadas de textura como (s, t, r, 1) e glTexCoord4 define todos os quatro componentes explicitamente como (s, t, r, q). Você pode atualizar as coordenadas de textura atuais a qualquer momento. Em particular, você pode chamar glTexCoord entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md). A função a seguir recupera informações relacionadas **a glTexCoord:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CURRENT \_ TEXTURE \_ COORDS

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





