---
title: Guia de programação de plug-ins de interface do usuário
description: Guia de programação de plug-ins de interface do usuário
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Windows Media Player, plug-ins
- Windows Media Player, plug-ins de interface do usuário
- Plug-ins do Windows Media Player, interface do usuário
- plug-ins, interface do usuário
- plug-ins de interface do usuário, guia de programação
- Plug-ins de interface do usuário, guia de programação
- Guia de programação, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d417d246e92a642711e8cb02f77ff3795d47c995
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822802"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Guia de programação de plug-ins de interface do usuário

Os dois exemplos de código descritos nesta seção demonstram o processo de implementação de um plug-in de interface do usuário personalizada, começando com o código gerado pelo assistente de plug-in do Windows Media Player.

O plug-in da interface do usuário de pesquisa é um plug-in de área de metadados que fornece um botão de **pesquisa** . Quando esse botão é clicado, uma página de pesquisa é iniciada no navegador da Web padrão que contém informações sobre o artista do item de mídia atual.

A primeira etapa na criação desse plug-in é iniciar um novo projeto no Microsoft Visual C++ selecionando **Assistente de plug-in do Windows Media Player** na guia **projetos** . Nomeie o projeto como "Pesquisar" e clique em **OK**. Escolha **plug-in de interface do usuário** e clique em **Avançar**. Em seguida, escolha o tipo de metadados na lista de opções e clique em **Avançar**. Por fim, clique na caixa de seleção para o suporte de execução automática para que o plug-in seja carregado automaticamente e clique em **concluir**. O assistente gera os arquivos de projeto necessários, incluindo as implementações básicas da classe CSearch e a interface **IWMPPluginUI** a que ela dá suporte e a classe CPluginWindow que fornece a interface do usuário. Este é o código que será modificado para fornecer a funcionalidade de plug-in descrita nesta seção.

O último tópico nesta seção descreve como criar um plug-in de interface do usuário em segundo plano para o Windows Media Player 10 Mobile. Esse plug-in usa código modificado gerado pelo assistente de plug-in do Windows Media Player para criar um plug-in para o Windows Media Player 10 Mobile.

Esta seção contém os seguintes tópicos.



| Tópico                                                                                                                                            | Descrição                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implementando CSearch](implementing-csearch.md)                                                                                                 | Descreve as alterações necessárias para a classe CSearch.                                |
| [Implementando CPluginWindow](implementing-cpluginwindow.md)                                                                                     | Descreve as alterações necessárias para a classe CPluginWindow.                          |
| [Criando um plug-in de interface do usuário para o Windows Media Player 10 Mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | Descreve como criar um plug-in de interface do usuário em segundo plano para o Windows Media Player 10 Mobile. |



 

 

 




