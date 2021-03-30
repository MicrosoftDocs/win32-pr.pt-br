---
title: Obtendo informações de estado
description: Obtendo informações de estado
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, informações de estado
- OpenGL, variáveis de estado
- informações de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635641"
---
# <a name="obtaining-state-information"></a>Obtendo informações de estado

O OpenGL mantém muitas variáveis de estado que afetam o comportamento de muitas funções. Algumas dessas variáveis têm funções de consulta especializadas.



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [**glGetClipPlane**](glgetclipplane.md) | [**glGetPixelMap**](glgetpixelmap.md)             | [**glGetTexImage**](glgetteximage.md)                   |
| [**glGetLight**](glgetlight.md)         | [**glGetPolygonStipple**](glgetpolygonstipple.md) | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |
| [**glGetMap**](glgetmap.md)             | [**glGetTexEnv**](glgettexenv.md)                 | [**glGetTexParameter**](glgettexparameter.md)           |
| [**glGetMaterial**](glgetmaterial.md)   | [**glGetTexGen**](glgettexgen.md)                 |                                                          |



 

Para obter o valor de outras variáveis de estado, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetIntegerv**](glgetintegerv.md), conforme apropriado. Consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para obter informações sobre como usar essas funções. Outras funções de consulta que você talvez queira usar são [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)e [**glIsEnabled**](glisenabled.md). (Consulte [tratamento de erros](handling-errors.md) para obter mais informações sobre as funções relacionadas ao tratamento de erros.) Para salvar e restaurar conjuntos de variáveis de estado, use [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).

-   [Usando as funções de consulta](using-the-query-functions.md)
-   [Tratamento de erro](error-handling.md)
-   [Códigos de erro OpenGL](opengl-error-codes.md)
-   [Salvando e restaurando conjuntos de variáveis de estado](saving-and-restoring-sets-of-state-variables.md)
-   [Variáveis de estado OpenGL](opengl-state-variables.md)
-   [Referência de informações de estado](state-information-reference.md)

 

 




