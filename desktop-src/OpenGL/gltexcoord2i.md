---
title: função glTexCoord2i (GL. h)
description: Define as coordenadas de textura atuais. | função glTexCoord2i (GL. h)
ms.assetid: 7a5ff9a7-8dcd-47a0-868c-3909e011a592
keywords:
- função glTexCoord2i OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c2ee5b7a1a1986f9d24a9650b97bc364e60b80f403f95d9e9ed15820a9f734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491246"
---
# <a name="gltexcoord2i-function"></a>função glTexCoord2i

Define as coordenadas de textura atuais.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexCoord2i(
   GLint s,
   GLint t
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*s* 
</dt> <dd>

A coordenada de textura s.

</dd> <dt>

*t* 
</dt> <dd>

A coordenada de textura t.

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

 

 





