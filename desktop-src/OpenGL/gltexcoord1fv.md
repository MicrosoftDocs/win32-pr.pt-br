---
title: função glTexCoord1fv (GL. h)
description: Define as coordenadas de textura atuais. | função glTexCoord1fv (GL. h)
ms.assetid: 8f128cb7-3617-4bde-aa6e-4d197b481d34
keywords:
- função glTexCoord1fv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord1fv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdc6330d16fa9ab637bc0e46ad2af8b400dcd523
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172792"
---
# <a name="gltexcoord1fv-function"></a>função glTexCoord1fv

Define as coordenadas de textura atuais.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexCoord1fv(
   const GLfloat *v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*l* 
</dt> <dd>

Um ponteiro para uma matriz de coordenadas de textura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função [**glTexCoord**](gltexcoord-functions.md) define as coordenadas de textura atuais que fazem parte dos dados associados a vértices de polígono. A função **glTexCoord** especifica as coordenadas de textura em uma, duas, três ou quatro dimensões. A função glTexCoord1 define as coordenadas de textura atuais como (s, 0, 0, 1); uma chamada para glTexCoord2 os define como (s, t, 0, 1). Da mesma forma, glTexCoord3 especifica as coordenadas de textura como (s, t, r, 1) e glTexCoord4 define todos os quatro componentes explicitamente como (s, t, r, p). Você pode atualizar as coordenadas de textura atuais a qualquer momento. Em particular, você pode chamar glTexCoord entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md). A função a seguir recupera informações relacionadas a **glTexCoord**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ CoOrds de textura atual \_

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





