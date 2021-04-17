---
title: função glGetClipPlane (GL. h)
description: A função glGetClipPlane retorna os coeficientes do plano de recorte especificado.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- função glGetClipPlane OpenGL
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
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761407"
---
# <a name="glgetclipplane-function"></a>função glGetClipPlane

A função **glGetClipPlane** retorna os coeficientes do plano de recorte especificado.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*aérea* 
</dt> <dd>

Um plano de recorte. O número de planos de recorte depende da implementação, mas há suporte para pelo menos seis planos de recorte. Elas são identificadas por nomes simbólicos do formulário GL de \_ clipe \_ *i,* em que 0 = *i* < GL \_ Max \_ recortes \_ .

</dd> <dt>

*subscrito* 
</dt> <dd>

Retorna quatro valores de precisão dupla que são os coeficientes da equação de plano do *plano* em coordenadas de olho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *plano* não era um valor aceito.<br/>                                                                                         |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGetClipPlane** retorna na *equação* os quatro coeficientes da equação de plano para o *plano*.

É sempre o caso que o GL \_ clip \_ avião *i* = GL \_ clip \_ PLANE0 + *i*.

Se um erro for gerado, nenhuma alteração será feita no conteúdo da *equação*.

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

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





