---
title: função glInterleavedArrays (GL. h)
description: A função glInterleavedArrays especifica e habilita simultaneamente várias matrizes intercaladas em uma matriz agregada maior.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- função glInterleavedArrays OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369346"
---
# <a name="glinterleavedarrays-function"></a>função glInterleavedArrays

A função **glInterleavedArrays** especifica e habilita simultaneamente várias matrizes intercaladas em uma matriz agregada maior.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*format* 
</dt> <dd>

O tipo de matriz a ser habilitado. O parâmetro pode assumir um dos seguintes valores simbólicos: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL \_ C4F N3F V3F \_ \_ , GL \_ T2F \_ V3F, GL \_ t4f \_ V4F, GL \_ T2F \_ C4UB \_ V3F, GL \_ T2F \_ C3F V3F \_ , GL \_ T2F \_ N3F V3F \_ , GL \_ T2F \_ C4F \_ N3F V3F \_ ou GL \_ t4f \_ \_ \_ C4F N3F V4F.

</dd> <dt>

*Stride* 
</dt> <dd>

O deslocamento em bytes entre cada elemento de matriz agregada.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para o primeiro elemento de uma matriz de agregação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *formato* não era um valor aceito.<br/>                                                                                        |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *Stride* era um valor negativo.<br/>                                                                                             |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Com a função **glInterleavedArrays** , você pode especificar e habilitar simultaneamente várias matrizes de cores intercaladas, normal, de textura e de vértice cujos elementos fazem parte de um elemento de matriz agregada maior. Para algumas arquiteturas de memória, isso é mais eficiente do que especificar as matrizes separadamente.

Se o parâmetro *Stride* for zero, os elementos da matriz de agregação serão armazenados consecutivamente; caso contrário, ocorrerão bytes de *Stride* entre os elementos de matriz agregada.

O parâmetro *Format* serve como uma chave que descreve como extrair matrizes individuais da matriz agregada:

-   Se o *formato* contiver um T, as coordenadas de textura serão extraídas da matriz intercalada.
-   Se C estiver presente, os valores de cor serão extraídos.
-   Se N estiver presente, as coordenadas normais serão extraídas.
-   As coordenadas de vértice são sempre extraídas.
-   Os dígitos 2, 3 e 4 denotam quantos valores são extraídos.
-   F indica que os valores são extraídos como valores de ponto flutuante.
-   Se 4UB seguir a C, as cores também podem ser extraídas como 4 bytes não assinados. Se uma cor for extraída como 4 bytes não assinados, o elemento de matriz de vértices a seguir estará localizado no primeiro endereço alinhado de ponto flutuante possível.

Se você chamar **glInterleavedArrays** durante a compilação de uma lista de exibição, ela não será compilada na lista, mas será executada imediatamente.

Você não pode incluir chamadas para **glInterleavedArrays** em **glDisableClientState** entre chamadas para [**glBegin**](glbegin.md) e a chamada correspondente para **glEnd**.

> [!Note]  
> A função **glInterleavedArrays** só está disponível no OpenGL versão 1,1 ou posterior.

 

A função **glInterleavedArrays** é implementada no lado do cliente sem protocolo. Como os parâmetros de matriz de vértice são um estado do lado do cliente, eles não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**. Em vez disso, use [**glPushClientAttrib**](glpushclientattrib.md) e **glPopClientAttrib** .

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





