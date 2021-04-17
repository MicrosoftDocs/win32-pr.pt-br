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
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748420"
---
# <a name="porting-picking-functions"></a>Portando funções de separação

Todas as funções de separação do íris GL têm equivalentes a OpenGL, com exceção de **clearhitcode**. A tabela a seguir lista as funções de separação do íris GL e suas funções OpenGL equivalentes.



| Função GL de íris                | Função OpenGL                                                                           | Significado                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | Não há suporte.                                                                            | Limpa a variável global e hitcode.    |
| **pickselect**<br/>       | [**glRenderMode**](glrendermode.md) (GL \_ Select)                                       | Alterna para o modo de seleção ou de separação. |
| **endpickendselect**<br/> | [**glRenderMode**](glrendermode.md) ( \_ renderização GL)                                       | Alterna para o modo de renderização.            |
| **picksize**                    | [**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)<br/> | Define a matriz de retorno.                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glPushName**](glpushname.md)[**glPopName**](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

Para obter mais informações sobre a escolha, consulte [**gluPickMatrix**](glupickmatrix.md).

 

 





