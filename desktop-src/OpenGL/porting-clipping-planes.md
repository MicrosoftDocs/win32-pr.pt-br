---
title: Portando planos de recorte
description: O OpenGL implementa planos de recorte da mesma forma para o íris GL. Além disso, no OpenGL, você pode consultar os planos de recorte. A tabela a seguir lista as funções de plano de recorte íris GL e suas funções OpenGL equivalentes.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Portabilidade do íris GL, planos de recorte
- portando do íris GL, planos de recorte
- portando para OpenGL do íris GL, planos de recorte
- Portabilidade do OpenGL do íris GL, planos de recorte
- planos de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f314b7c6453de3b0933970b7d520a8c161d6eef4a9bb98ea891c73665fba4933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777116"
---
# <a name="porting-clipping-planes"></a>Portando planos de recorte

O OpenGL implementa planos de recorte da mesma forma para o íris GL. Além disso, no OpenGL, você pode consultar os planos de recorte. A tabela a seguir lista as funções de plano de recorte íris GL e suas funções OpenGL equivalentes.



| Função GL de íris                          | Função OpenGL                                                                               | Significado                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| **clipplane** (i, **CP \_ on**, params)     | [**glEnable**](glenable.md) (GL \_ remediador \_ )                                             | Habilita o recorte no plano i.             |
| **clipplane**(i, **CP \_ definir**, plano) | [**glClipPlane**](glclipplane.md) (GL do \_ remediador \_ , plano)                                | Define o plano de recorte.                  |
|                                           | [**glGetClipPlane**](glgetclipplane.md)                                                      | Retorna a equação do plano de recorte.         |
|                                           | [**glIsEnabled**](glisenabled.md) (GL \_ remediador \_ )                                       | Retornará true se o plano de corte i estiver habilitado. |
| **scrmask**                               | [**glScissor**](glscissor.md)                                                                | Define a caixa de tesoura.                 |
| **getscrmask**                            | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ caixa de tesoura GL \_ ) | Retorna a caixa de tesoura atual.         |



 

Para ativar o teste de tesoura, chame **glEnable** usando \_ \_ a caixa de tesoura GL como o parâmetro.

??

 

 




