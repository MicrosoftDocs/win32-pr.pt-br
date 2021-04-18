---
title: função glGetPointerv (GL. h)
description: A função glGetPointerv retorna o endereço de uma matriz de dados de vértice.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- função glGetPointerv OpenGL
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
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794438"
---
# <a name="glgetpointerv-function"></a>função glGetPointerv

A função **glGetPointerv** retorna o endereço de uma matriz de dados de vértice.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* 
</dt> <dd>

O tipo de ponteiro de matriz a ser retornado das seguintes constantes simbólicas: o ponteiro da matriz de cores GL, o indicador de borda do GL Flag, o ponteiro do buffer de comentários do GL, o ponteiro da matriz de índice GL, o ponteiro de matriz normal do GL, o ponteiro de \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ matriz coord de textura GL, o marcador de \_ buffer de \_ \_ \_ seleção GL e o \_ \_ \_ \_ \_ ponteiro

</dd> <dt>

*params* 
</dt> <dd>

Retorna o valor do ponteiro de matriz especificado por *pname*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                             | Significado                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl> | *pname* não era um valor aceito.<br/> |



## <a name="remarks"></a>Comentários

A função **glGetPointerv** retorna informações de ponteiro de matriz. O parâmetro *pname* é uma constante simbólica que especifica o tipo de ponteiro de matriz a ser retornado, e *params* é um ponteiro para um local para inserir os dados retornados.

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

 

 





