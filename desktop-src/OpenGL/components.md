---
title: Componentes
description: Componentes
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL no Windows, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105782179"
---
# <a name="components"></a>Componentes

A implementação da Microsoft do OpenGL no Windows inclui os seguintes componentes:

-   O conjunto completo de comandos OpenGL atuais

    O OpenGL contém uma biblioteca de funções básicas para operações de gráficos 3D. Essas funções básicas são usadas para gerenciar a descrição da forma de objeto, transformação de matriz, iluminação, coloração, textura, recorte, bitmaps, neblina e anti-aliasing. Os nomes dessas funções principais têm um prefixo "GL".

    Muitos dos comandos OpenGL têm várias variantes, que diferem no número e no tipo de seus parâmetros. Contando todas as variantes, há mais de 300 comandos OpenGL.

-   A biblioteca do utilitário OpenGL (GLU)

    Essa biblioteca de funções auxiliares complementa as principais funções OpenGL. Os comandos gerenciam o suporte à textura, a transformação de coordenadas, o mosaico de polígono, a renderização de difira, cilindros e discos, curvas e superfícies de NURBS (não uniforme, B-spline) e tratamento de erros.

-   A biblioteca auxiliar do guia de programação OpenGL

    Essa é uma biblioteca de funções simples e independente de plataforma para gerenciar o Windows, manipular eventos de entrada, desenhar objetos 3D clássicos, gerenciar um processo em segundo plano e executar um programa. O gerenciamento de janelas e as rotinas de entrada fornecem um nível básico de funcionalidade com o qual você pode começar a programação rapidamente no OpenGL.

    Não os use, no entanto, em um aplicativo de produção. Aqui estão alguns motivos para esse aviso:

    -   O loop de mensagem está no código de biblioteca.
    -   Não há nenhuma maneira de adicionar manipuladores para mensagens adicionais do WM \* .
    -   Há muito pouco suporte para paletas lógicas.

    A biblioteca é descrita e usada no *Guia de programação OpenGL*.

-   As funções WGL

    Esse conjunto de funções conecta o OpenGL ao sistema de janelas do Windows. As funções gerenciam contextos de renderização, listas de exibição, funções de extensão e bitmaps de fontes. As funções WGL são análogas às extensões GLX que conectam OpenGL ao sistema de janelas X. Os nomes dessas funções têm um prefixo "WGL".

-   Novas funções do Windows para formatos de pixel e buffer duplo

    Essas funções dão suporte a formatos de pixel por janela e buffer duplo (para alterações de imagem suave) do Windows. Essas novas funções se aplicam somente a janelas de gráficos OpenGL.

 

 




