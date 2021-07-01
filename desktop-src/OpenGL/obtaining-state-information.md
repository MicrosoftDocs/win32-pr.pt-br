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
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120681"
---
# <a name="obtaining-state-information"></a>Obtendo informações de estado

O OpenGL mantém muitas variáveis de estado que afetam o comportamento de muitas funções. Algumas dessas variáveis têm funções de consulta especializadas.

:::row:::
    :::column:::
        [**glGetClipPlane**](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [**glGetPixelMap**](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexImage**](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetLight**](glgetlight.md)
    :::column-end:::
    :::column:::
        [**glGetPolygonStipple**](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [**glGetTexLevelParameter**](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMap**](glgetmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexEnv**](glgettexenv.md)
    :::column-end:::
    :::column:::
        [**glGetTexParameter**](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMaterial**](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [**glGetTexGen**](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

Para obter o valor de outras variáveis de estado, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetIntegerv**](glgetintegerv.md), conforme apropriado. Consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para obter informações sobre como usar essas funções. Outras funções de consulta que você talvez queira usar são [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)e [**glIsEnabled**](glisenabled.md). (Consulte [tratamento de erros](handling-errors.md) para obter mais informações sobre as funções relacionadas ao tratamento de erros.) Para salvar e restaurar conjuntos de variáveis de estado, use [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).

-   [Usando as funções de consulta](using-the-query-functions.md)
-   [Tratamento de erro](error-handling.md)
-   [Códigos de erro OpenGL](opengl-error-codes.md)
-   [Salvando e restaurando conjuntos de variáveis de estado](saving-and-restoring-sets-of-state-variables.md)
-   [Variáveis de estado OpenGL](opengl-state-variables.md)
-   [Referência de informações de estado](state-information-reference.md)

 

 




