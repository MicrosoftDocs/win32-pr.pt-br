---
title: Começar a trabalhar com o DirectX para Windows
description: Criar um jogo do Microsoft DirectX para Windows é um desafio para um novo desenvolvedor. Aqui, analisamos rapidamente os conceitos envolvidos e as etapas que você deve seguir para começar a desenvolver um jogo usando DirectX e C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c93944b29546746f88b3edcacaefeeeacde0784e51f82c74f4cd462bc62025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986996"
---
# <a name="get-started-with-directx-for-windows"></a>Começar a trabalhar com o DirectX para Windows

Criar um jogo do Microsoft DirectX para Windows é um desafio para um novo desenvolvedor. Aqui, analisamos rapidamente os conceitos envolvidos e as etapas que você deve seguir para começar a desenvolver um jogo usando DirectX e C++.

Vamos começar.

## <a name="what-skills-do-you-need"></a>De quais habilidades você precisa?

Para desenvolver um jogo no DirectX para Windows, você deve ter algumas habilidades básicas. Especificamente, você deve ser capaz de:

-   Leia e escreva um código C++ moderno (o C++11 ajuda mais) e familiarizar-se com os princípios básicos de design e padrões do C++, como modelos e o modelo de fábrica. Você também deve estar familiarizado com bibliotecas C++ comuns, como a Biblioteca de Modelos Padrão, e especificamente com os operadores de seleção, tipos de ponteiro e as estruturas de dados da biblioteca de modelos padrão (como std::vector).
-   Entender geometria básica, trigonometria e álgebra linear. Grande parte do código que você encontrará nos exemplos pressu que você entende essas formas de matemática e suas regras comuns.
-   Tenha familiaridade com COM— [**especialmente Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (ponteiro inteligente).
-   Entenda os fundamentos da tecnologia de elementos gráficos e gráficos, especialmente gráficos 3D. Embora o Próprio DirectX tenha sua própria terminologia, ele ainda se baseia em uma compreensão bem estabelecida dos princípios gerais de elementos gráficos 3D.
-   Entenda o conceito de um loop de mensagem, pois você implementará um loop que escuta o Windows operacional.

## <a name="and-were-off"></a>E estamos desligados!

Pronto para começar? Vamos analisar antes de continuarmos. Você:

-   Uma instalação atualizada e em funcionamento do Windows 8.1.
-   Uma instalação do [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Um cérebro intrípido e um desejo de saber mais sobre o desenvolvimento de jogos do DirectX!

## <a name="next-steps"></a>Próximas etapas



| Tópico                                                                                                   | Descrição                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Trabalhar com recursos do dispositivo DirectX](work-with-dxgi.md)                                           | Saiba como usar o DXGI para criar um dispositivo gráfico virtualizado e criar e configurar uma cadeia de permuta.     |
| [Entender o pipeline de renderização do Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md) | Saiba como conectar-se à classe de recursos do dispositivo DirectX e desenhar usando o pipeline de gráficos direct3D. |
| [Trabalhar com sombreadores e recursos de sombreador](work-with-shaders-and-shader-resources.md)               | Saiba como escrever programas de sombreador HLSL para estágios de pipeline de gráficos direct3D.                            |



 

 

 