---
title: Portando funções de separação
description: Todas as funções de separação do íris GL têm equivalentes a OpenGL, com exceção de clearhitcode. A tabela a seguir lista as funções de separação do íris GL e suas funções OpenGL equivalentes.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Portabilidade do íris GL, separação
- portando do íris GL, escolhendo
- portando para OpenGL do íris GL, escolhendo
- Portabilidade OpenGL do íris GL, separação
- seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be2cbeed54a18e7f1d3f26ec01dca2ad352aa4e190fbdc667ed75a60badec29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034806"
---
# <a name="porting-picking-functions"></a>Portando funções de separação

Todas as funções de separação do íris GL têm equivalentes a OpenGL, com exceção de **clearhitcode**. A tabela a seguir lista as funções de separação do íris GL e suas funções OpenGL equivalentes.



| Função GL de íris                | Função OpenGL                                                                           | Significado                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | Sem suporte.                                                                            | Limpa a variável global e hitcode.    |
| **pickselect**<br/>       | [**glRenderMode**](glrendermode.md) (GL \_ Select)                                       | Alterna para o modo de seleção ou de separação. |
| **endpickendselect**<br/> | [**glRenderMode**](glrendermode.md) ( \_ renderização GL)                                       | Alterna para o modo de renderização.            |
| **picksize**                    | [**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)<br/> | Define a matriz de retorno.                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glPushName**](glpushname.md)[**glPopName**](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

Para obter mais informações sobre a escolha, consulte [**gluPickMatrix**](glupickmatrix.md).

 

 





