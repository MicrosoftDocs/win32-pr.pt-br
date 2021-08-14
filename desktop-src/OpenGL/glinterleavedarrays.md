---
title: Função glInterleavedArrays (Gl.h)
description: A função glInterleavedArrays especifica e habilita simultaneamente várias matrizes intercaladas em uma matriz de agregação maior.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- Função glInterleavedArrays OpenGL
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
ms.openlocfilehash: ce3b37186614fa431585c1e5a932edab946afd6d881ba1cf8eb5c5690220f603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938557"
---
# <a name="glinterleavedarrays-function"></a>Função glInterleavedArrays

A **função glInterleavedArrays** especifica e habilita simultaneamente várias matrizes intercaladas em uma matriz de agregação maior.

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

O tipo de matriz a ser habilitada. O parâmetro pode assumir um dos seguintes valores simbólicos: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL \_ \_ C4F \_ N3F V3F, GL \_ T2F \_ V3F, GL \_ T4F \_ V4F, GL \_ T2F \_ C4UB \_ V3F, GL \_ \_ T2F \_ C3F V3F, GL \_ T2F \_ N3F \_ V3F, GL \_ T2F \_ \_ C4F N3F \_ V3F ou GL \_ T4F \_ C4F \_ N3F \_ V4F.

</dd> <dt>

*Passo* 
</dt> <dd>

O deslocamento em bytes entre cada elemento de matriz de agregação.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para o primeiro elemento de uma matriz de agregação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Name                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *format* não era um valor aceito.<br/>                                                                                        |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *stride* era um valor negativo.<br/>                                                                                             |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

Com a **função glInterleavedArrays,** você pode especificar e habilitar simultaneamente várias matrizes de cor, normal, textura e vértice intercaladas cujos elementos fazem parte de um elemento de matriz de agregação maior. Para algumas arquiteturas de memória, isso é mais eficiente do que especificar as matrizes separadamente.

Se o *parâmetro stride* for zero, os elementos da matriz de agregação serão armazenados consecutivamente; caso *contrário, os* bytes de distância ocorrem entre os elementos da matriz de agregação.

O *parâmetro* format serve como uma chave que descreve como extrair matrizes individuais da matriz de agregação:

-   Se *format* contiver um T, as coordenadas de textura serão extraídas da matriz intercalada.
-   Se C estiver presente, os valores de cor serão extraídos.
-   Se N estiver presente, as coordenadas normais serão extraídas.
-   As coordenadas de vértice sempre são extraídas.
-   Os dígitos 2, 3 e 4 denotam quantos valores são extraídos.
-   F indica que os valores são extraídos como valores de ponto flutuante.
-   Se o 4UB seguir o C, as cores também poderão ser extraídas como 4 bytes não assinados. Se uma cor for extraída como 4 bytes não assinados, o elemento de matriz de vértice a seguir está localizado no primeiro endereço alinhado de ponto flutuante possível.

Se você chamar **glInterleavedArrays** ao compilar uma lista de exibição, ela não será compilada na lista, mas será executada imediatamente.

Não é possível incluir chamadas **para glInterleavedArrays** **em glDisableClientState** entre chamadas para [**glBegin**](glbegin.md) e a chamada correspondente para **glEnd**.

> [!Note]  
> A **função glInterleavedArrays** só está disponível no OpenGL versão 1.1 ou posterior.

 

A **função glInterleavedArrays** é implementada no lado do cliente sem protocolo. Como os parâmetros de matriz de vértice são de estado do lado do cliente, eles não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e **glPopAttrib.** Em vez disso, use [**glPushClientAttrib**](glpushclientattrib.md) e **glPopClientAttrib.**

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

 

 





