---
title: Tratamento de erros (OpenGL)
description: A função gluErrorString recupera cadeias de caracteres de erro que correspondem aos códigos de erro OpenGL ou GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Utilitário OpenGL (GLU), códigos de erro
- GLU (utilitário OpenGL), códigos de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ac3fd9010862dd9c567cb7688f7f96286cae06f7e3b0e4ffe73d3b41ca9b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035186"
---
# <a name="handling-errors-opengl"></a>Tratamento de erros (OpenGL)

A função **gluErrorString** recupera cadeias de caracteres de erro que correspondem aos códigos de erro OpenGL ou Glu. Os códigos de erro OpenGL definidos atualmente são descritos em [**glGetError**](glgeterror.md). Os códigos de erro GLU são listados em [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)e [*gluNurbsCallback*](glunurbs.md).

O valor de retorno para **gluErrorString** é um ponteiro para uma cadeia de caracteres descritiva que corresponde ao número de erro OpenGL, glu ou GLX passado no parâmetro *ErrorCode* . Os códigos de erro definidos são descritos no *manual de referência do OpenGL* , juntamente com a função ou função que pode gerá-los.

 

 




