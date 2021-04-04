---
title: função glCullFace (GL. h)
description: A função glCullFace especifica se as facetas de front-face ou voltagem para frente podem ser refeitas.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- função glCullFace OpenGL
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
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918100"
---
# <a name="glcullface-function"></a>função glCullFace

A função **glCullFace** especifica se as facetas de front-face ou voltagem para frente podem ser refeitas.

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

Especifica se as facetas voltadas para a frente ou para trás são candidatas para a remoção. As constantes simbólicas GL \_ front, GL \_ back e GL \_ front \_ e \_ back são aceitas. O valor padrão é GL de \_ volta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glCullFace** especifica se as facetas de front-face ou voltagem para frente são examinadas (conforme especificado pelo *modo*) quando a remoção da faceta está habilitada. Você habilita e desabilita a remoção de faceta usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com a face de seleção do Argument GL \_ \_ . As facetas incluem triângulos, quadrilaterals, polígonos e retângulos.

A função [**glFrontFace**](glfrontface.md) especifica qual das facetas no sentido horário e anti-horário são voltadas para frente e para trás.

Se o *modo* for GL \_ frontal \_ e \_ posterior, nenhuma faceta será desenhada, mas outros primitivos, como pontos e linhas, serão desenhados.

As funções a seguir recuperam informações relacionadas ao **glCullFace**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o Argument GL selecionar \_ \_ \_ modo facial

[**glIsEnabled**](glisenabled.md) com a face do argumento GL de \_ seleção \_

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

 

 





