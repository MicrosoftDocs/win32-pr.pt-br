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
ms.openlocfilehash: 4ee4265341e17843dbe4752bb51e5728aa54914ec5670c08b6b7921537050a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012034"
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

 

 





