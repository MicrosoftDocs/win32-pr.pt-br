---
title: Portando greset
description: O OpenGL substitui a função GL de íris, greset, pelas funções, glPushAttrib e glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Portabilidade do íris GL, variáveis de estado
- portando do íris GL, variáveis de estado
- portando para OpenGL do íris GL, variáveis de estado
- Portabilidade do OpenGL do íris GL, variáveis de estado
- variáveis de estado
- Portabilidade do íris GL, função greset
- portando do íris GL, função greset
- portando para OpenGL do íris GL, função greset
- Portabilidade OpenGL do íris GL, função greset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364181"
---
# <a name="porting-greset"></a>Portando greset

O OpenGL substitui a função GL de íris, **greset**, pelas funções, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md). Use essas funções para salvar e restaurar grupos de variáveis de estado. Por exemplo,

``` syntax
void glPushAttrib( GLbitfield mask );
```

Este exemplo usa uma constante de bits ou de uma operação simbólica, indicando quais grupos de variáveis de estado enviar por push para uma pilha de atributos. Cada constante refere-se a um grupo de variáveis de estado. A tabela a seguir mostra os grupos de atributos com seus nomes de constantes simbólicas equivalentes. Para obter uma lista completa das variáveis de estado OpenGL associadas a cada constante, consulte [**glPushAttrib**](glpushattrib.md).



| Atributo                       | Constante                  |
|---------------------------------|---------------------------|
| valor de limpeza do buffer de acumulação | BIT de buffer do GL \_ Accum \_ \_    |
| buffer de cores                    | \_bit do \_ buffer de cores GL \_    |
| atual                         | BIT do GL \_ atual \_          |
| buffer de profundidade                    | \_bit de \_ buffer de profundidade GL \_    |
| enable                          | \_bit de habilitação GL \_           |
| avaliadores                      | \_bit de Val EGL \_             |
| neblina                             | \_bit de neblina GL \_              |
| Configuração da base da \_ lista GL \_          | \_bit da lista GL \_             |
| variáveis de dica                  | \_bit de dica GL \_             |
| variáveis de iluminação              | \_bit de iluminação GL \_         |
| modo de desenho de linha               | \_bit de linha gl \_             |
| variáveis de modo de pixel            | \_bit do \_ modo de pixel GL \_      |
| variáveis de ponto                 | \_bit de ponto GL \_            |
| polygon                         | \_bit do polígono GL \_          |
| Stipple de polígono                 | \_STIPPLE de polígono do GL \_ \_ |
| tesoura                         | BIT GL de \_ tesoura \_          |
| buffer de estêncil                  | \_bit de \_ buffer do estêncil GL \_  |
| textura                         | \_bit de textura GL \_          |
| transformação                       | \_bit de transformação GL \_        |
| visor                        | \_bit GL viewport \_         |
|                                 | GL \_ todos \_ os \_ bits de Atrib.     |



 

Para restaurar os valores das variáveis de estado para aquelas salvas com o último [**glPushAttrib**](glpushattrib.md), basta chamar [**glPopAttrib**](glpopattrib.md). As variáveis que você não salvou permanecerão inalteradas. A pilha de atributos tem uma profundidade finita de pelo menos 16.

 

 




