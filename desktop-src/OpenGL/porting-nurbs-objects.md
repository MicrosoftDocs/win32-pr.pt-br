---
title: Portando objetos NURBS
description: O OpenGL trata a NURBS como objetos, semelhante ao modo como ele trata quadrics você cria um objeto NURBS e, em seguida, especifica como ele deve ser renderizado. A tabela a seguir lista as funções OpenGL GLU para gerenciar objetos NURBS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Portabilidade do íris GL, objetos NURBS
- portando de objetos íris GL, NURBS
- portando para OpenGL do íris GL, objetos NURBS
- Portabilidade OpenGL do íris GL, objetos NURBS
- Objetos NURBS
- NURBS (B racional não uniforme-spline)
- B-spline racional não uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6990d2292399cb1ccaf00ba6ec42d680c5ace887b2495daf8640db2da30ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132405"
---
# <a name="porting-nurbs-objects"></a>Portando objetos NURBS

O OpenGL trata a NURBS como objetos, semelhante ao modo como ele trata quadrics: você cria um objeto NURBS e, em seguida, especifica como ele deve ser renderizado. A tabela a seguir lista as funções OpenGL GLU para gerenciar objetos NURBS.



| Função OpenGL GLU                                      | Significado                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)       | Cria um novo objeto NURBS.                                    |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) | Exclui um objeto NURBS.                                        |
| [*gluNurbsCallback*](glunurbs.md)                       | Associa um retorno de chamada com um objeto NURBS, para tratamento de erros. |



 

Ao portar o código NURBS do íris GL para OpenGL, tenha em mente os seguintes pontos:

-   Pontos de controle NURBS são floats, não duplos.
-   O parâmetro Stride é contado em floats, não em bytes.
-   Se você estiver usando a iluminação e não estiver especificando normais, chame [**glEnable**](glenable.md) com o GL \_ auto \_ normal como o parâmetro para gerar normais automaticamente.

??

 

 




