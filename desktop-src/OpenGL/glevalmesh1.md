---
title: Função glEvalMesh1 (Gl.h)
description: Calcula uma grade unidimensional de pontos ou linhas.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- Função glEvalMesh1 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c325134a8a8fd60afdc764eebc8a4de9bd507b5b667ebb8e1b2ab967edcd7e77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625466"
---
# <a name="glevalmesh1-function"></a>Função glEvalMesh1

Calcula uma grade unidimensional de pontos ou linhas.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

Um valor que especifica se uma malha unidimensional de pontos ou linhas deve ser calculada. As seguintes constantes simbólicas são aceitas: GL \_ POINT e GL \_ LINE.

</dd> <dt>

*i1* 
</dt> <dd>

O primeiro valor inteiro para a variável de domínio de grade i.

</dd> <dt>

*i2* 
</dt> <dd>

O último valor inteiro da variável de domínio de grade i.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | Indica que *o modo* não é um valor aceito. <br/>                                                                            |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md) <br/> |



## <a name="remarks"></a>Comentários

Use [**glMapGrid e**](glmapgrid-functions.md) [**glEvalMesh**](glevalmesh-functions.md) juntos para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espalismo de maneira eficiente. A **função glEvalMesh** passa pelo domínio inteiro de uma grade unidimensional ou bidimensional, cujo intervalo é o domínio dos mapas de avaliação especificados por [**glMap1**](glmap1.md) e [**glMap2.**](glmap2.md) O parâmetro mode determina se os vértices resultantes estão conectados como pontos, linhas ou polígonos preenchidos.

No caso unidimensional, **glEvalMesh1**, a malha é gerada como se o seguinte fragmento de código fosse executado:

[**glBegin**](glbegin.md)(*tipo*);

for (i = i1; i <= i2; i += 1)

{

[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)

}

[**glEnd**](glend.md)( );

onde

?u = (u2 u1) / n

e n, u1 e u2 são os argumentos para a função [**glMapGrid1 mais**](glmapgrid1d.md) recente. O *parâmetro type* será GL POINTS se o modo for GL POINT ou GL LINES se o modo for GL \_ \_ \_ \_ LINE. O único requisito numérico absoluto é que, se i = n, o valor calculado de i?u + u1 for exatamente u2.

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
</dt> </dl>

 

 





