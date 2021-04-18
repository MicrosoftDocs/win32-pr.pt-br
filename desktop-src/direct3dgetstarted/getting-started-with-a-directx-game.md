---
title: Introdução ao DirectX para Windows
description: A criação de um jogo do Microsoft DirectX para Windows é um desafio para um novo desenvolvedor. Aqui, examinamos rapidamente os conceitos envolvidos e as etapas que você deve seguir para começar a desenvolver um jogo usando DirectX e C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105796173"
---
# <a name="get-started-with-directx-for-windows"></a>Introdução ao DirectX para Windows

A criação de um jogo do Microsoft DirectX para Windows é um desafio para um novo desenvolvedor. Aqui, examinamos rapidamente os conceitos envolvidos e as etapas que você deve seguir para começar a desenvolver um jogo usando DirectX e C++.

Vamos começar.

## <a name="what-skills-do-you-need"></a>De quais habilidades você precisa?

Para desenvolver um jogo no DirectX para Windows, você deve ter algumas habilidades básicas. Especificamente, você deve ser capaz de:

-   Leia e escreva código C++ moderno (o C++ 11 ajuda mais) e familiarize-se com os princípios e padrões de design básicos de C++, como modelos e o modelo de fábrica. Você também deve estar familiarizado com bibliotecas C++ comuns como a biblioteca de modelos padrão e, especificamente, com os operadores de conversão, tipos de ponteiro e as estruturas de dados da biblioteca de modelos padrão (como std:: vector).
-   Entenda a geometria básica, a trigonometria e a Algebra linear. Grande parte do código que você encontrará nos exemplos pressupõe que você compreenda essas formas de matemática e suas regras comuns.
-   Familiaridade com com, especialmente [**Microsoft:: WRL:: ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (ponteiro inteligente).
-   Entenda as bases da tecnologia gráfica e gráfica, especialmente os gráficos 3D. Embora o próprio DirectX tenha sua própria terminologia, ele ainda se baseia em uma compreensão bem estabelecida dos princípios gerais de gráficos 3D.
-   Entenda o conceito de um loop de mensagem, pois você estará implementando um loop que escuta o sistema operacional Windows.

## <a name="and-were-off"></a>E estamos desligados!

Pronto para começar? Vamos examinar antes de nosso início. Você:

-   Uma instalação atualizada e funcional do Windows 8.1.
-   Uma instalação do [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Um espírito intrépido e um desejo de saber mais sobre o desenvolvimento de jogos DirectX!

## <a name="next-steps"></a>Próximas etapas



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Trabalhar com recursos do dispositivo DirectX](work-with-dxgi.md)                                           | Saiba como usar DXGI para criar um dispositivo gráfico virtualizado e criar e configurar uma cadeia de permuta.     |
| [Entender o pipeline de renderização do Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md) | Saiba como se conectar à classe de recursos do dispositivo DirectX e desenhar usando o pipeline de gráficos do Direct3D. |
| [Trabalhar com sombreadores e recursos de sombreador](work-with-shaders-and-shader-resources.md)               | Saiba como escrever programas de sombreador HLSL para estágios de pipeline de gráficos do Direct3D.                            |



 

 

 