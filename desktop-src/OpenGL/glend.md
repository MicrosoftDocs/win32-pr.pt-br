---
title: função glEnd (GL. h)
description: As funções glBegin e glend delimitam os vértices de um primitivo ou de um grupo de primitivas como primitivos. | função glEnd (GL. h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- função glEnd OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105750460"
---
# <a name="glend-function"></a>função glEnd

As funções [**glBegin**](glbegin.md) e **glend** delimitam os vértices de um primitivo ou de um grupo de primitivas como primitivos.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | Uma função diferente de **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList** ou **glCallLists** foi chamada entre **glBegin** e o **glEnd** correspondente. A função **glEnd** foi chamada antes que o **glBegin** correspondente fosse chamado ou **glBegin** foi chamado dentro de uma / sequência **glEnd** glBegin. <br/> |



## <a name="remarks"></a>Comentários

As funções [**glBegin**](glbegin.md) e **glend** delimitam os vértices que definem um primitivo ou um grupo de primitivas como primitivos. A função **glBegin** aceita um único argumento que especifica qual dos dez primitivos os vértices compõem. Colocando *n* como uma contagem de inteiros começando em um, e *n* como o número total de vértices especificado, as interpretações são as seguintes:

-   Você pode usar apenas um subconjunto de funções OpenGL entre **glBegin** e **glEnd**. As funções que você pode usar são:

    -   [**glVertex**](glvertex-functions.md)
    -   [**glColor**](glcolor-functions.md)
    -   [**glIndex**](glindex-functions.md)
    -   [**glNormal**](glnormal-functions.md)
    -   [**glTexCoord**](gltexcoord-functions.md)
    -   [**glEvalCoord**](glevalcoord-functions.md)
    -   [**glEvalPoint**](glevalpoint.md)
    -   [**glMaterial**](glmaterial-functions.md)
    -   [**glEdgeFlag**](gledgeflag-functions.md)

    Você também pode usar [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) para executar listas de exibição que incluem apenas as funções anteriores. Se qualquer outra função OpenGL for chamada entre **glBegin** e **glEnd**, o sinalizador de erro será definido e a função será ignorada.

-   Independentemente do valor escolhido para o *modo* em **glBegin**, não há nenhum limite para o número de vértices que você pode definir entre **glBegin** e **glEnd**. Linhas, triângulos, quadrilaterals e polígonos especificados incompletamente não são desenhadas. Resultados incompletos de especificação quando um número muito pequeno de vértices são fornecidos para especificar até mesmo um único primitivo ou quando um múltiplo incorreto de vértices é especificado. O primitivo incompleto é ignorado; os primitivos completos são desenhados.
-   A especificação mínima de vértices para cada primitivo é: 

    | Número mínimo de vértices | Tipo de primitiva |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | triangle          |
    | 4                          | diamante     |
    | 3                          | polygon           |

    

     

-   Os modos que exigem um determinado múltiplo de vértices são \_ linhas GL (2), \_ triângulos GL (3), GL \_ quádruplos (4) e GL \_ Quad \_ strip (2).

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

[**glBegin**](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

