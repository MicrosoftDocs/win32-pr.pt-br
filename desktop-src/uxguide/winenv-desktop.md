---
title: Área de trabalho
description: O desktop é a área de trabalho do usuário para seus programas. Não é uma maneira de promover a conscientização do seu programa ou de sua marca. Não se preocupe.
ms.assetid: 99cb218d-9b1f-4e43-94d2-4ea74b0e10d3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 159be01b1058eac99c30b83534b7a9eafd9c4eb4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104011901"
---
# <a name="desktop"></a>Área de trabalho

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

O desktop é a área de trabalho do usuário para seus programas. Não é uma maneira de promover a conscientização do seu programa ou de sua marca. Não se preocupe!

O desktop é a área de trabalho na tela fornecida pelo Microsoft Windows, análoga a um desktop físico. Ele consiste em uma [área de trabalho](glossary.md) e uma [barra de tarefas](winenv-taskbar.md). A área de trabalho pode abranger vários monitores.

![captura de tela de uma área de trabalho típica do Windows ](images/winenv-desktop-image1.png)

Uma área de trabalho do Windows típica.

O monitor ativo é o monitor em que o programa ativo está em execução. O monitor padrão é aquele com o menu Iniciar, a barra de tarefas e a área de notificação.

## <a name="design-concepts"></a>Conceitos de design

A área de trabalho do Windows tem os seguintes pontos de acesso do programa:

-   **Área de trabalho.** A área na tela onde os usuários podem realizar seu trabalho, bem como armazenar programas, documentos e seus atalhos. Embora tecnicamente a área de trabalho inclua a barra de tarefas, na maioria dos contextos ela se refere apenas à área de trabalho.
-   **Botão Iniciar.** O ponto de acesso para todos os programas e locais especiais do Windows (documentos, imagens, música, jogos, computador, painel de controle), com as listas "usadas mais recentemente" para acesso rápido a programas e documentos usados recentemente.
-   **Início rápido. Removido do Windows 7.** Um ponto de acesso direto para programas selecionados pelo usuário.
-   **Na.** O ponto de acesso para executar programas que têm presença na área de trabalho. Embora tecnicamente a barra de tarefas abranja a barra inteira do botão Iniciar para a área de notificação, na barra de tarefas a maioria dos contextos se refere à área entre eles, contendo os botões da barra de tarefas. Essa área, às vezes, é chamada de TaskBand.
-   **Deskbands. Não recomendado.** Programas funcionais e de longa execução minimizados, como a barra de idiomas. Os programas que minimizam o deskbands não exibem botões da barra de tarefas quando minimizados.
-   **Área de notificação.** Uma fonte de curto prazo para notificações e status, bem como um ponto de acesso para recursos relacionados ao sistema e ao programa que não têm nenhuma presença na área de trabalho.

![captura de tela do botão Iniciar, barra de tarefas, miniatura ](images/winenv-desktop-image2.png)

Os pontos de acesso à área de trabalho do Windows incluem o botão Iniciar, a barra de tarefas e a área de notificação. Observe o recurso de miniatura do botão da barra de tarefas.

**A área de trabalho do Windows é um recurso compartilhado e limitado que é o ponto de entrada do usuário para o Windows. Deixe os usuários no controle.** Você deve usar suas áreas como pretendidas – qualquer outro uso deve ser considerado um abuso. Nunca os exiba como maneiras de promover a conscientização do seu programa ou de sua [marca](exper-branding.md).

Para o Windows 7, os OEMs (fabricantes originais de equipamento) e os IHVs (fornecedores independentes de hardware) podem usar o Device Stage para criar uma interface do usuário personalizada e com marca para o computador e os dispositivos, sem desobstruir as áreas de trabalho dos usuários. Os OEMs em particular podem usar o computador de estágio do dispositivo para recursos personalizados de programas, ofertas de serviço e suporte. Para obter mais informações, consulte o [Microsoft Device Experience Development Kit](https://www.microsoft.com/whdc/device/DeviceExperience/Dev-Kit.mspx).

**Se você fizer apenas uma coisa...**

-   Não se preocupe com a área de trabalho — Mantenha os usuários no controle. Se os usuários de destino provavelmente usarem seu programa com frequência, forneça uma opção durante a instalação para colocar um atalho na área de trabalho, desmarcado por padrão.

## <a name="guidelines"></a>Diretrizes

-   **Se os usuários tiverem muito probabilidade de usar seu programa com frequência, forneça uma opção durante a instalação para colocar um atalho do programa na área de trabalho.** A maioria dos programas não será usada com frequência suficiente para garantir a oferta dessa opção.
-   **Apresente a opção desmarcada por padrão.** Exigir que os usuários selecionem a opção é importante porque, uma vez que ícones indesejados estão na área de trabalho, muitos usuários são relutantes para removê-los. Isso pode levar à aglomeração de área de trabalho desnecessária.
-   **Se os usuários selecionarem a opção, forneça apenas um único atalho de programa.** Se seu produto for composto por vários programas, forneça um atalho somente para o programa principal.
-   **Coloque apenas atalhos de programa na área de trabalho.** Não coloque o programa real ou outros tipos de arquivos.

    **Correto:**

    ![captura de tela do ícone de atalho com sobreposição de seta ](images/winenv-desktop-image3.png)

    **Incorreto:**

    ![captura de tela do ícone do programa ](images/winenv-desktop-image4.png)

    No exemplo incorreto, o programa, e não um atalho, é copiado para a área de trabalho.

-   **Escolha um rótulo que possa ser exibido sem truncamento.** Os usuários não devem ver uma elipse.

    **Correto:**

    ![captura de tela do ícone de atalho com nome completo ](images/winenv-desktop-image3.png)

    **Incorreto:**

    ![captura de tela do ícone de atalho com nome truncado ](images/winenv-desktop-image5.png)

    No exemplo incorreto, o rótulo de atalho do programa é tão longo que ele é truncado.

## <a name="documentation"></a>Documentação

-   Ao fazer referência à área de trabalho, use desktop, com letras maiúsculas.
-   Ao fazer referência a atalhos da área de trabalho, use o atalho, com letras maiúsculas.

 

 