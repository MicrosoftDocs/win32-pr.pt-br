---
title: Função glGetPointerv (Gl.h)
description: A função glGetPointerv retorna o endereço de uma matriz de dados de vértice.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- Função glGetPointerv OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbef5cc17a547e82dfa55876d927ef9fed87f106d9e5fa0d5d1c36a5ce269b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493916"
---
# <a name="glgetpointerv-function"></a>Função glGetPointerv

A **função glGetPointerv** retorna o endereço de uma matriz de dados de vértice.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

O tipo de ponteiro de matriz a ser retornada das seguintes constantes simbólicas: GL \_ COLOR \_ ARRAY \_ POINTER, GL EDGE FLAG \_ ARRAY \_ \_ \_ POINTER, GL FEEDBACK BUFFER \_ \_ \_ POINTER, GL INDEX ARRAY \_ \_ \_ POINTER, GL NORMAL ARRAY \_ \_ \_ POINTER, GL TEXTURE \_ \_ COORD ARRAY POINTER, GL SELECTION BUFFER POINTER e \_ GL \_ \_ \_ \_ \_ VERTEX \_ ARRAY \_ POINTER.

</dd> <dt>

*params* 
</dt> <dd>

Retorna o valor do ponteiro de matriz especificado por *pname*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                             | Significado                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl> | *pname* não era um valor aceito.<br/> |



## <a name="remarks"></a>Comentários

A **função glGetPointerv** retorna informações de ponteiro de matriz. O *parâmetro pname* é uma constante simbólica que especifica o tipo de ponteiro de matriz a ser retornado e *params* é um ponteiro para um local para colocar os dados retornados.

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





