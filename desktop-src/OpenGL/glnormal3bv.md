---
title: Função glNormal3bv (Gl.h)
description: Define o vetor normal atual. | Função glNormal3bv (Gl.h)
ms.assetid: 1d9be974-93c9-45ac-89f1-92c14ff1c242
keywords:
- Função glNormal3bv OpenGL
topic_type:
- apiref
api_name:
- glNormal3bv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10578bbf22aa2cb0e3415715999018db4a3aefd39933cd802e1abbc196d5b706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795600"
---
# <a name="glnormal3bv-function"></a>Função glNormal3bv

Define o vetor normal atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glNormal3bv(
   const GLbyte *v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*v* 
</dt> <dd>

Um ponteiro para uma matriz de três elementos: as coordenadas x, y e z do novo normal atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O normal atual é definido para as coordenadas fornecidas sempre que você chama a **função glNormal3bv.**

Os argumentos de byte, curto ou inteiro são convertidos em formato de ponto flutuante usando um mapeamento linear que mapeia o valor inteiro representável mais positivo para 1,0 e o valor inteiro representável mais negativo para -1,0.

Os normais especificados usando **glNormal3bv** não precisam ter comprimento de unidade. Se a normalização estiver habilitada, os normais especificados usando **glNormal3bv** serão normalizados após a transformação. Você pode controlar a normalização usando [**glEnable e**](glenable.md) [**glDisable**](gldisable.md) com o argumento GL \_ NORMALIZE. Por padrão, a normalização está desabilitada. Você pode atualizar o normal atual a qualquer momento. Em particular, você pode chamar **glNormal3bv** entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md) As seguintes funções recuperam informações relacionadas **a glNormal3bv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CURRENT \_ NORMAL

[**glIsEnable com**](glisenabled.md) o argumento GL \_ NORMALIZE

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





