---
title: Portando aplicativos do IRIS GL
description: Portando aplicativos do IRIS GL
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- OpenGL na Windows,portação GL iris
- portando para OpenGL, IRIS GL
- Portação openGL, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68e218e5b6f57039e364ab4e6ebc29fb1f2b2fad2e8a679b35c1368367f5f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777226"
---
# <a name="porting-applications-from-iris-gl"></a>Portando aplicativos do IRIS GL

Esta seção lista diferenças importantes entre IRIS GL e OpenGL e descreve as etapas básicas para portar código do IRIS GL para o OpenGL. Para ver uma lista completa das diferenças entre IRIS GL e Open GL, confira [Diferenças de IRIS GL e OpenGL.](iris-gl-and-opengl-differences.md)

A portabilidade de programas IRIS GL para OpenGL para Windows requer consideravelmente mais trabalho do que converter programas OpenGL do sistema de janela X. Embora os programas IRIS GL sejam projetados para executar com hardware e software específicos, o OpenGL foi projetado para portabilidade entre vários sistemas.

A tabela a seguir lista algumas das principais diferenças entre os programas OpenGL e IRIS GL.



| Código OpenGL                                                                                                                                              | Código IRIS GL                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Independente do sistema operacional; não contém funções para janelas, manipulação de eventos, alocação/gerenciamento de buffer e assim por diante.                              | Dependente do sistema operacional; funções windowing-system são misturadas com funções de renderização. Não há nenhum Gerenciador do Windows no IRIS GL. |
| Usa uma convenção de nomenização padrão e comum. As funções OpenGL e tipos definidos começam com um prefixo "gl" para evitar conflitos com outras bibliotecas.        | Não usa uma convenção de nomen entre funções e tipos definidos.                                                              |
| Gerencia variáveis de estado (como cor, cinza, textura, iluminação e assim por diante) de forma direta e consistente. Não usa tabelas para carregar valores de variável de estado. | Usa tabelas para gerenciar variáveis de estado e deve vincular variáveis a valores de tabela.                                                        |
| As listas de exibição não podem ser editadas.                                                                                                                          | Listas de exibição podem ser editadas.                                                                                                          |
| Não fornece um formato de arquivo para fontes.                                                                                                                | Fornece funções para lidar com fontes e cadeias de caracteres de texto e um formato de arquivo para fontes.                                                      |
| Inclui uma biblioteca GLU (Utilitário GL) que contém funções e rotinas adicionais (como NALTERS e rotinas de renderização quadrática).                    | Não dá suporte à biblioteca GLU.                                                                                                     |



 

**Use o procedimento geral a seguir para por portabilidade de seus programas IRIS GL para OpenGL**

1.  Reescreva qualquer código que faça chamadas a um gerenciador de janelas, configuração de janela, dispositivo ou evento ou em que você carrega um mapa de cores para código Windows equivalente. Reescrever um aplicativo de um sistema operacional para outro pode ser complexo e difícil. Esse assunto está além do escopo desta seção.
2.  Localize qualquer código que use funções e rotinas IRIS GL. Traduza essas funções para suas funções equivalentes do OpenGL. Para uma listagem completa de funções e rotinas IRIS GL e suas contrapartes equivalentes do OpenGL, consulte Funções OpenGL e [seus equivalentes DE GL IRIS](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Altere o código IRIS GL, conforme descrito [em Problemas especiais de portação DE GL do IRIS.](special-iris-gl-porting-issues.md)

<!-- -->

1.  Reescreva qualquer código que faça chamadas a um gerenciador de janelas, configuração de janela, dispositivo ou evento ou em que você carrega um mapa de cores para código Windows equivalente. Reescrever um aplicativo de um sistema operacional para outro pode ser complexo e difícil. Esse assunto está além do escopo desta seção.
2.  Localize qualquer código que use funções e rotinas IRIS GL. Traduza essas funções para suas funções equivalentes do OpenGL. Para uma listagem completa de funções e rotinas IRIS GL e suas contrapartes equivalentes do OpenGL, consulte Funções OpenGL e [seus equivalentes DE GL IRIS](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Altere o código IRIS GL, conforme descrito [em Problemas especiais de portação DE GL do IRIS.](special-iris-gl-porting-issues.md)

 

 




