---
title: Noções básicas sobre comandos e controles
description: A separação da lógica da apresentação é a filosofia do design que inspira o sistema de apresentação de comandos do Windows Ribbon Framework \ 8212; um sistema baseado em um padrão de design onde a funcionalidade e o comportamento são implementados independentemente dos controles que expõem essa funcionalidade.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Visão geral dos comandos do Windows Ribbon
- Visão geral de comandos
- Visão geral dos controles do Windows
- Visão geral dos controles
- sistema de comandos para Windows Ribbon
- controles para a faixa de faixas do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104569239"
---
# <a name="understanding-commands-and-controls"></a>Noções básicas sobre comandos e controles

A separação da lógica da apresentação é a filosofia do design que inspira o sistema de apresentação de comando da estrutura da faixa de forma do Windows – um sistema baseado em um padrão de design onde a funcionalidade e o comportamento são implementados independentemente dos controles que expõem essa funcionalidade.

-   [Introdução](#introduction)
-   [O sistema de comandos da faixa de dasgem do Windows](#the-windows-ribbon-command-system)
    -   [Controles](#understanding-commands-and-controls)
    -   [Comandos](#understanding-commands-and-controls)
    -   [A experiência de comando em ação](#the-command-experience-in-action)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Este artigo aborda o design do sistema de comando da estrutura da faixa de faixas. Ele descreve os conceitos de comandos e controles e explora como eles funcionam em conjunto para fornecer uma experiência de comando avançada com uma série de novos recursos de interface do usuário.

## <a name="the-windows-ribbon-command-system"></a>O sistema de comandos da faixa de dasgem do Windows

Na estrutura da faixa de, os comandos e os controles são entidades independentes. Um comando é uma estrutura abstrata, sem restrições de apresentação, que representa uma tarefa ou classe específica de funcionalidade. Um controle, por outro lado, é um objeto concreto que expõe a funcionalidade de comando por meio da interface do usuário da faixa de tipos.

Essa distinção fornece a capacidade de definir comandos que são livres de detalhes da interface do usuário e que podem ser executados na intenção de uma ação sem a necessidade de gerenciar como a ação foi invocada.

### <a name="controls"></a>Controles

Os controles são os objetos de interface do usuário necessários para apresentação de comando. Eles são renderizados e gerenciados em tempo de execução pela estrutura com base na interação do usuário e em um conjunto de propriedades e comportamentos inerentes.

Conhecido como layout adaptável, a flexibilidade gerenciada pela estrutura da interface do usuário é uma das grandes vantagens da faixa de opção. Os controles da faixa de opção podem se reconfigurar automaticamente por meio de modelos de layout dependentes de estrutura ou definidos pelo desenvolvedor que são capazes de responder a vários requisitos de tempo de execução, tudo sem escrever uma única linha de código de apresentação. Para obter mais informações, consulte [Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).

Além dos benefícios do layout adaptável, vários controles de faixa de opção complexos fornecem soluções independentes para espaços de problema de interface do usuário específicos. Ao oferecer um modelo de interação sofisticado, os controles da faixa de opção, como o FontControl ou o ColorPicker, fornecem a capacidade de manipular dados em termos mais abstratos por meio de bolsas de propriedades de fontes reais ou de atributos de cor, em vez de vários subcontroles, enumerações e valores de índice de controles padrão do Windows.

### <a name="commands"></a>Comandos

Rigidamente acoplado aos controles da faixa de faixas que expõem sua funcionalidade, implementações de comando são o domínio do aplicativo host e assumem a forma de ouvintes de eventos, manipuladores de comandos e várias propriedades de comandos.

Os comandos são declarados na marcação da faixa de forma com uma ID exclusiva ou recebem uma ID gerada pelo compilador de marcação na compilação. Os comandos são associados a controles por meio de um nome de comando, mas, ao contrário dos controles, sua funcionalidade real é definida no código em que estão associados a manipuladores de comandos específicos por meio da ID de comando.

> [!Note]  
> Na compilação, essa ID é armazenada em um arquivo de cabeçalho de definição de ID que expõe comandos para seus manipuladores de comandos correspondentes no aplicativo host da faixa de faixas.

 

Cada comando tem um tipo de comando subjacente discriminado na enumeração de [**\_ COMMANDTYPE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) .

### <a name="the-command-experience-in-action"></a>A experiência de comando em ação

Os recursos desse modelo de comando são demonstrados pela barra de ferramentas de acesso rápido da faixa de lista (QAT). O QAT fornece aos usuários finais uma maneira de definir facilmente seus próprios atalhos para praticamente qualquer controle na interface do usuário da faixa de opção. Um atalho é adicionado dinamicamente ao QAT em tempo de execução quando o usuário clica com o botão direito do mouse em um controle da faixa de forma e seleciona **Adicionar à barra de ferramentas de acesso rápido** no menu de contexto.

A imagem a seguir mostra os comandos **colar** e **colar de** , representados por um controle [**SplitButton**](windowsribbon-element-splitbutton.md) , na faixa de opções do Paint do Windows 7.

![imagem do SplitButton de colagem na faixa de faixas do Microsoft Paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

A imagem a seguir mostra os mesmos comandos **Paste** e **Paste from** , ainda representados por um controle [**SplitButton**](windowsribbon-element-splitbutton.md) , na faixa de opções qat do Windows 7 Paint.

![imagem do SplitButton de colagem no qat do Microsoft Paint.](images/overviews/paint-paste-splitbutton-qat.png)

Quando um controle é hospedado pelo QAT, a nova instância do controle mantém toda a funcionalidade do controle original sem a necessidade de ouvintes de evento adicionais e manipuladores de comando para dar suporte a ele. Ambos os controles são associados ao mesmo manipulador de comando da faixa de opções por meio de um identificador de comando compartilhado. Dessa forma, a estrutura trata os dois controles como um, independentemente do que é invocado.

> [!Note]  
> Os mesmos benefícios são percebidos quando os comandos são incorporados em um [**ContextPopup**](windowsribbon-element-contextpopup.md) em tempo de design. Nesse caso, os manipuladores de comando Paste podem ser usados se o controle [**SplitButton**](windowsribbon-element-splitbutton.md) aparecer na faixa de, qat ou **ContextPopup**.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apresentando o Windows Ribbon Framework](windowsribbon-introduction.md)
</dt> <dt>

[Criando um aplicativo de faixa de faixas](windowsribbon-stepbystep.md)
</dt> <dt>

[Declarando comandos e controles com marcação de faixa de medida](windowsribbon-schema.md)
</dt> </dl>

 

 