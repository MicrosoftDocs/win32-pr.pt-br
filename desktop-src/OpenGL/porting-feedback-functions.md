---
title: Portando funções de comentários
description: Com o íris GL, a maneira como os comentários são tratados difere dependendo do computador que executa o íris GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Portabilidade do íris GL, comentários
- portando do íris GL, comentários
- portando para OpenGL do íris GL, comentários
- Portabilidade do OpenGL do íris GL, comentários
- comentários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f4ab584dfbd9038d45e7d24c006857f278a9239fc6f9da4d38a75363f0d585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132628"
---
# <a name="porting-feedback-functions"></a>Portando funções de comentários

Com o íris GL, a maneira como os comentários são tratados difere dependendo do computador que executa o íris GL. O OpenGL padroniza as funções de comentários para que você possa contar com comentários consistentes entre várias plataformas de hardware. A tabela a seguir lista as funções de comentários da íris GL e suas funções OpenGL equivalentes.



| Função GL de íris | Função OpenGL                                                                                            | Significado                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| **receber**     | [**glRenderMode**](glrendermode.md) (comentários do GL \_ )                                                      | Alterna para o modo de comentários.                    |
| **endfeedback**  | [**glRenderMode**](glrendermode.md) (GL \_ renderizar)[**glFeedbackBuffer**](glfeedbackbuffer.md)<br/> | Alterna para o modo de renderização.                   |
| **passagem**  | [**glPassThrough**](glpassthrough.md)                                                                     | Coloca um marcador de token no buffer de comentários. |



 

 

 





