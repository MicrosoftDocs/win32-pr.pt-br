---
title: Usando as funções de consulta
description: Usando as funções de consulta
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, funções de consulta
- funções de consulta OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780494"
---
# <a name="using-the-query-functions"></a>Usando as funções de consulta

Há quatro funções de consulta para obter variáveis de estado simples e uma para determinar se um estado específico está habilitado ou desabilitado:

-   [**glGetBooleanv**](glgetbooleanv.md)
-   [**glGetIntegerv**](glgetintegerv.md)
-   [**glGetFloatv**](glgetfloatv.md)
-   [**glGetDoublev**](glgetdoublev.md)
-   [**glIsEnabled**](glisenabled.md)

Os protótipos para as funções de consulta são:

**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );

**void** **glGetIntegerv**(**GLenum** *pname* , *parâmetros* de **GLint \*** );

**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );

**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );

Respectivamente, as funções de consulta obtêm variáveis de estado booliano, inteiro, ponto flutuante ou de precisão dupla. O parâmetro *pname* é uma constante simbólica que indica a variável de estado a ser retornada, e *params* é um ponteiro para uma matriz do tipo indicado no qual os dados retornados serão colocados. Os valores possíveis para *pname* são listados em [variáveis de estado OpenGL](opengl-state-variables.md). Uma conversão de tipo é executada, se necessário, para retornar a variável desejada como o tipo de dados solicitado.

O protótipo para [**glIsEnabled**](glisenabled.md) é:

**GLboolean** **glIsEnabled**(GLenum *Cap* );

Se o modo especificado por *Cap* estiver habilitado, **glIsEnabled** retornará GL \_ true. Se o modo especificado por *Cap* estiver desabilitado, **glIsEnabled** retornará GL \_ false. Os valores possíveis para *Cap* são listados em [variáveis de estado OpenGL](opengl-state-variables.md).

Outras funções especializadas retornam variáveis de estado específicas. Para descobrir quando usar essas funções, consulte variáveis de estado OpenGL e o *manual de referência OpenGL*. Para obter mais informações sobre o recurso de tratamento de erros do OpenGL e a função **glGetError** , consulte [tratamento de erros](error-handling.md).

As funções que retornam variáveis de estado específicas são:

-   [**glGetClipPlane**](glgetclipplane.md)
-   [**glGetError**](glgeterror.md)
-   [**glGetLight**](glgetlight.md)
-   [**glGetMap**](glgetmap.md)
-   [**glGetMaterial**](glgetmaterial.md)
-   [**glGetPixelMap**](glgetpixelmap.md)
-   [**glGetPolygonStipple**](glgetpolygonstipple.md)
-   [**glGetString**](glgetstring.md)
-   [**glGetTexEnv**](glgettexenv.md)
-   [**glGetTexGen**](glgettexgen.md)
-   [**glGetTexImage**](glgetteximage.md)
-   [**glGetTexLevelParameter**](glgettexlevelparameter.md)
-   [**glGetTexParameter**](glgettexparameter.md)

 

 




