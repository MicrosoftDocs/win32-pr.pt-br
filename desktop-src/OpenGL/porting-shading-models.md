---
title: Modelos de sombreamento de portador
description: Como o íris GL, o OpenGL permite alternar entre sombreamento suave (Gouraud) e sombreamento simples. A tabela a seguir lista as funções de pontilhamento e sombreamento da íris GL e suas funções OpenGL equivalentes.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Portabilidade do íris GL, sombreamento
- portando do íris GL, sombreamento
- portando para OpenGL do íris GL, sombreamento
- Portabilidade do OpenGL do íris GL, sombreamento
- sombreamento suave
- Sombreamento Gouraud
- sombreamento simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292440"
---
# <a name="porting-shading-models"></a>Modelos de sombreamento de portador

Como o íris GL, o OpenGL permite alternar entre sombreamento suave (Gouraud) e sombreamento simples. A tabela a seguir lista as funções de pontilhamento e sombreamento da íris GL e suas funções OpenGL equivalentes.



| Função GL de íris                                   | Função OpenGL                                                                                    | Significado                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel**(simples)                               | [**glShadeModel**](glshademodel.md) (GL \_ simples)                                                  | O sombreamento simples.           |
| **shademodel**(GOURAUD)                            | **glShadeModel**(GL \_ suave)                                                                     | O sombreamento suave.         |
| **obter**                                          | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modelo de sombreamento GL \_ )      | Retorna o modelo de sombra atual. |
| **pontilhamento (DT**) de pontilhamento \_ (DT  \_ desativado) <br/> | [**glEnable**](glenable.md) ( \_ pontilhamento GL [**) glDisable**](gldisable.md)( \_ pontilhamento GL)<br/> | Ativa/desativa o pontilhamento.      |



 

??

 

 





