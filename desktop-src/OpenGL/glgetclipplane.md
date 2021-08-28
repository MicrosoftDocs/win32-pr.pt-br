---
title: Função glGetClipPlane (Gl.h)
description: A função glGetClipPlane retorna os coeficientes do plano de recorte especificado.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- Função glGetClipPlane OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf551356088db2b99b79a28a396be785ab60f2196cc3e27353cb867d4b151dd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742026"
---
# <a name="glgetclipplane-function"></a>Função glGetClipPlane

A **função glGetClipPlane** retorna os coeficientes do plano de recorte especificado.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*avião* 
</dt> <dd>

Um plano de recorte. O número de planos de recorte depende da implementação, mas há suporte para pelo menos seis planos de recorte. Eles são identificados por nomes simbólicos da forma GL CLIP PLANE i, em que \_ \_ 0 = *i* < GL MAX CLIP  \_ \_ \_ PLANES.

</dd> <dt>

*Equação* 
</dt> <dd>

Retorna quatro valores de precisão dupla que são os coeficientes da equação do plano *do plano nas* coordenadas de olho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *plane* não era um valor aceito.<br/>                                                                                         |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glGetClipPlane** retorna na *equação* os quatro coeficientes da equação do plano para *o plano*.

É sempre o caso de GL \_ CLIP \_ PLANE *i* = GL \_ CLIP \_ PLANE0 + *i*.

Se um erro for gerado, nenhuma alteração será feita no conteúdo da *equação*.

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

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





