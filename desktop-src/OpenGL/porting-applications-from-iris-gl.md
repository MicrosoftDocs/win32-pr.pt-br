---
title: Portando aplicativos do íris GL
description: Portando aplicativos do íris GL
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- OpenGL no Windows, portabilidade do íris GL
- portando para OpenGL, íris GL
- Portabilidade OpenGL, íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9e739b40f63bb2fd00bb62b4e5ec5566df3c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757498"
---
# <a name="porting-applications-from-iris-gl"></a>Portando aplicativos do íris GL

Esta seção lista as diferenças importantes entre o íris GL e o OpenGL e descreve as etapas básicas para portar o código do íris GL para OpenGL. Para obter uma lista completa das diferenças entre o íris GL e o Open GL, consulte [diferenças de íris GL e OpenGL](iris-gl-and-opengl-differences.md).

A portabilidade de programas do íris GL para o OpenGL para Windows requer um trabalho consideravelmente maior do que a conversão de programas OpenGL do sistema de janelas X. Embora os programas da íris GL sejam projetados para serem executados com hardware e software específicos, o OpenGL foi projetado para portabilidade entre vários sistemas.

A tabela a seguir lista algumas das principais diferenças entre os programas OpenGL e íris GL.



| Código OpenGL                                                                                                                                              | Código GL do íris                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Independente do sistema operacional; Não contém funções para janelas, manipulação de eventos, alocação/gerenciamento de buffer e assim por diante.                              | Dependente do sistema operacional; janelas de funções do sistema são misturadas com funções de renderização. Não há nenhum Gerenciador do Windows no íris GL. |
| Usa uma Convenção de nomenclatura padrão e comum. As funções OpenGL e os tipos definidos começam com um prefixo "GL" para evitar conflitos com outras bibliotecas.        | Não usa uma Convenção de nomenclatura comum para funções e tipos definidos.                                                              |
| Gerencia variáveis de estado (como cor, sombra, textura, iluminação e assim por diante) de forma direta e consistente. Não usa tabelas para carregar valores de variável de estado. | Usa tabelas para gerenciar variáveis de estado e deve associar variáveis a valores de tabela.                                                        |
| As listas de exibição não podem ser editadas.                                                                                                                          | As listas de exibição podem ser editadas.                                                                                                          |
| Não fornece um formato de arquivo para fontes.                                                                                                                | Fornece funções para lidar com fontes e cadeias de caracteres de texto e um formato de arquivo para fontes.                                                      |
| Inclui uma biblioteca GL Utility (GLU) que contém funções e rotinas adicionais (como as rotinas de renderização NURBS e quadrática).                    | Não oferece suporte à biblioteca GLU.                                                                                                     |



 

**Use o procedimento geral a seguir para portar seus programas do íris GL para OpenGL**

1.  Reescreva qualquer código que faça chamadas para um Gerenciador de janelas, configuração de janela, dispositivo ou evento, ou em que você carrega um mapa de cores para o código equivalente do Windows. Reescrever um aplicativo de um sistema operacional para outro pode ser complexo e difícil. Este assunto está além do escopo desta seção.
2.  Localize qualquer código que use funções e rotinas do íris GL. Traduza essas funções para suas funções OpenGL equivalentes. Para obter uma lista completa das funções e rotinas do íris GL e suas contrapartes do OpenGL equivalentes, consulte [funções OpenGL e seus equivalentes do íris GL](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Altere o código GL do íris conforme descrito em [problemas especiais de portagem do íris](special-iris-gl-porting-issues.md).

<!-- -->

1.  Reescreva qualquer código que faça chamadas para um Gerenciador de janelas, configuração de janela, dispositivo ou evento, ou em que você carrega um mapa de cores para o código equivalente do Windows. Reescrever um aplicativo de um sistema operacional para outro pode ser complexo e difícil. Este assunto está além do escopo desta seção.
2.  Localize qualquer código que use funções e rotinas do íris GL. Traduza essas funções para suas funções OpenGL equivalentes. Para obter uma lista completa das funções e rotinas do íris GL e suas contrapartes do OpenGL equivalentes, consulte [funções OpenGL e seus equivalentes do íris GL](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Altere o código GL do íris conforme descrito em [problemas especiais de portagem do íris](special-iris-gl-porting-issues.md).

 

 




