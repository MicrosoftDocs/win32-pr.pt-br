---
title: função glEdgeFlagPointer (GL. h)
description: A função glEdgeFlagPointer define uma matriz de sinalizadores de borda.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- função glEdgeFlagPointer OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644826"
---
# <a name="gledgeflagpointer-function"></a>função glEdgeFlagPointer

A função **glEdgeFlagPointer** define uma matriz de sinalizadores de borda.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Stride* 
</dt> <dd>

O deslocamento de byte entre sinalizadores de borda consecutivos. Quando *Stride* é zero, os sinalizadores de borda são totalmente empacotados na matriz.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para o primeiro sinalizador de borda na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                             | Significado                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl> | *Stride* ou *Count* era negativo.<br/> |



## <a name="remarks"></a>Comentários

A função **glEdgeFlagPointer** especifica o local e os dados de uma matriz de sinalizadores de borda boolianos a serem usados durante a renderização. O parâmetro *Stride* determina o deslocamento de bytes de um sinalizador de borda para o próximo, que habilita a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas. Em algumas implementações, armazenar os vértices e os atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas.

Uma matriz de sinalizador de borda é habilitada quando você especifica a \_ constante de matriz do sinalizador de borda GL \_ \_ com [**glEnableClientState**](glenableclientstate.md). Quando habilitado, [**glDrawArrays**](gldrawarrays.md) ou [**glArrayElement**](glarrayelement.md) usa a matriz de sinalizador de borda. Por padrão, a matriz de sinalizador de borda é desabilitada.

Use **glDrawArrays** para construir uma sequência de primitivos (todos do mesmo tipo) de um vértice predefinido e matrizes de atributo de vértice. Use **glArrayElement** para especificar primitivos indexando vértices e atributos de vértice, e [**glDrawElements**](gldrawelements.md) para construir uma sequência de primitivos indexando vértices e atributos de vértice.

Você não pode incluir **glEdgeFlagPointer** em listas de exibição.

Quando você especifica uma matriz de sinalizador de borda usando **glEdgeFlagPointer**, os valores de todos os parâmetros de matriz do sinalizador de borda da função são salvos em um estado do lado do cliente e os elementos estáticos da matriz podem ser armazenados em cache. Como os parâmetros de matriz de sinalizador de borda estão em um estado do lado do cliente, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) não salvam nem restauram seus valores.

Embora chamar **glEdgeFlagPointer** em um par [**glBegin**](glbegin.md) / [**glend**](glend.md) não gere um erro, os resultados são indefinidos.

As funções a seguir recuperam informações relacionadas à função **glEdgeFlagPointer** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Edge \_ flag de \_ matriz \_ Stride

 contagem de matriz de \_ sinalizador de borda GLGET com Argument GL \_ \_ \_

[](glgetpointerv.md) ponteiro de matriz do \_ sinalizador de borda GLGETPOINTERV com Argument GL \_ \_ \_

[](glisenabled.md) matriz de sinalizador de borda glIsEnabled com Argument GL \_ \_ \_

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





