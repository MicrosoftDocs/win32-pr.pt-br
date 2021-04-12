---
title: função glEvalMesh1 (GL. h)
description: Computa uma grade unidimensional de pontos ou linhas.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- função glEvalMesh1 OpenGL
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
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499480"
---
# <a name="glevalmesh1-function"></a>função glEvalMesh1

Computa uma grade unidimensional de pontos ou linhas.

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

Um valor que especifica se uma malha unidimensional de pontos ou linhas deve ser computada. As seguintes constantes simbólicas são aceitas: ingl \_ Point e GL \_ line.

</dd> <dt>

*I1* 
</dt> <dd>

O primeiro valor inteiro para a variável de domínio de grade i.

</dd> <dt>

*i2* 
</dt> <dd>

O último valor inteiro para a variável de domínio de grade i.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | Indica que o *modo* não é um valor aceito. <br/>                                                                            |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md). <br/> |



## <a name="remarks"></a>Comentários

Use [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) juntos para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme. A função **glEvalMesh** percorre o domínio inteiro de uma grade de uma ou duas dimensões, cujo intervalo é o domínio dos mapas de avaliação especificados por [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md). O parâmetro mode determina se os vértices resultantes são conectados como pontos, linhas ou polígonos preenchidos.

No caso unidimensional, **glEvalMesh1**, a malha é gerada como se o fragmento de código a seguir fosse executado:

[**glBegin**](glbegin.md)(*tipo*);

for (i = i1; i <= i2; i + = 1)

{

[**glEvalCoord1**](glevalcoord1d.md)(i? u + U1)

}

[**glEnd**](glend.md)();

onde

? u = (U2 U1)/n

e n, U1 e U2 são os argumentos para a função [**glMapGrid1**](glmapgrid1d.md) mais recente. O parâmetro de *tipo* será o GL \_ Points se Mode for GL \_ Point ou GL \_ linhas se Mode for GL \_ line. O requisito numérico absoluto é que, se eu = n, o valor calculado de i? u + U1 é exatamente U2.

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
</dt> </dl>

 

 





