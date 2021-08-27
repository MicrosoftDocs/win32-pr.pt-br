---
title: Função glCullFace (Gl.h)
description: A função glCullFace especifica se facetas voltadas para frente ou para trás podem ser reenviadas.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- Função glCullFace OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70fd983e9a5921d96ba487f7eb8d6f631b000019e8ff566eb1ecc79e05ce4fb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081666"
---
# <a name="glcullface-function"></a>Função glCullFace

A **função glCullFace** especifica se facetas voltadas para frente ou para trás podem ser reenviadas.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

Especifica se facetas voltadas para frente ou para trás são candidatas para ressarção. As constantes simbólicas GL \_ FRONT, GL \_ BACK e GL FRONT AND BACK são \_ \_ \_ aceitas. O valor padrão é GL \_ BACK.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glCullFace** especifica se facetas voltadas para a frente ou para trás são reenviadas (conforme especificado pelo modo *)* quando a redução de faceta está habilitada. Você habilita e desabilita a redução de faceta usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o argumento GL \_ CULL \_ FACE. As facetas incluem triângulos, retângulos, polígonos e retângulos.

A [**função glFrontFace**](glfrontface.md) especifica qual das facetas no sentido horário e anti-horário são voltadas para frente e para trás.

Se *o modo* for GL FRONT AND BACK, nenhuma faceta será desenhada, mas outros primitivos, como pontos e \_ \_ \_ linhas, serão desenhados.

As seguintes funções recuperam informações relacionadas **a glCullFace:**

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ CULL FACE \_ \_ MODE

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ CULL \_ FACE

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFrontFace**](glfrontface.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





