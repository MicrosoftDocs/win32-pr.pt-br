---
title: usando com em seu aplicativo Windows
description: O módulo 1 desta série mostrou como criar uma janela e responder a mensagens de janela como o WM \_ Paint e o WM \_ Close. O módulo 2 apresenta a Component Object Model (COM).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2180d47bd0dd12c0184a2f9241ec5656c7fe711150e1d5163ca2fec9e0b28fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068026"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a>Módulo 2. Usando COM em seu programa de Windows-Based

O [módulo 1](your-first-windows-program.md) desta série mostrou como criar uma janela e responder a mensagens de janela como o [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e o [**WM \_ Close**](/windows/desktop/winmsg/wm-close). O módulo 2 apresenta a Component Object Model (COM).

COM é uma especificação para a criação de componentes de software reutilizáveis. muitos dos recursos que você usará em um programa moderno baseado em Windows contam com o COM, como o seguinte:

-   Gráficos (Direct2D)
-   Texto (DirectWrite)
-   o Windows Shell
-   O controle da faixa de faixas
-   Animação da interface do usuário

(Algumas tecnologias nessa lista usam um subconjunto de COM e, portanto, não são "puras" COM.)

COM tem uma reputação de ser difícil de aprender. E é verdade que escrever um novo módulo de software para dar suporte a COM pode ser complicado. Mas se o seu programa for estritamente um *consumidor* de com, você verá que com é mais fácil entender do que o esperado.

Este módulo mostra como chamar APIs baseadas em COM em seu programa. Ele também descreve algumas das razões por trás do design de COM. Se você entender por que o COM foi projetado como está, poderá programar com ele com mais eficiência. A segunda parte do módulo descreve algumas práticas de programação recomendadas para COM.

O COM foi introduzido em 1993 para dar suporte ao OLE (vinculação e inserção de objetos) 2,0. Às vezes, as pessoas acham que o COM e o OLE são a mesma coisa. Isso pode ser outro motivo para a percepção de que COM é difícil de aprender. O OLE 2,0 foi criado com base em COM, mas você não precisa conhecer OLE para entender COM.

COM é um *padrão binário*, não um padrão de idioma: define a interface binária entre um aplicativo e um componente de software. Como um padrão binário, o COM é neutro em linguagem, embora seja mapeado naturalmente para determinadas construções de C++. Este módulo se concentrará em três grandes metas do COM:

-   Separar a implementação de um objeto de sua interface.
-   Gerenciando o tempo de vida de um objeto.
-   Descobrindo os recursos de um objeto em tempo de execução.

## <a name="in-this-section"></a>Nesta seção

-   [O que é uma interface COM?](what-is-a-com-interface-.md)
-   [Inicializando a biblioteca COM](initializing-the-com-library.md)
-   [Códigos de erro em COM](error-codes-in-com.md)
-   [Criando um objeto em COM](creating-an-object-in-com.md)
-   [Exemplo: a caixa de diálogo abrir](example--the-open-dialog-box.md)
-   [Gerenciando o tempo de vida de um objeto](managing-the-lifetime-of-an-object.md)
-   [Solicitando um objeto para uma interface](asking-an-object-for-an-interface.md)
-   [Alocação de memória em COM](memory-allocation-in-com.md)
-   [Práticas de codificação COM](com-coding-practices.md)
-   [Tratamento de erro em COM](error-handling-in-com.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprenda a programar para Windows em C++](learn-to-program-for-windows.md)
</dt> </dl>

 

 