---
title: Guia de programação de plug-ins de interface do usuário
description: Guia de programação de plug-ins de interface do usuário
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Windows Media Player, plug-ins
- Windows Media Player, plug-ins de interface do usuário
- plug-ins Windows Media Player, interface do usuário
- plug-ins, interface do usuário
- plug-ins de interface do usuário, guia de programação
- Plug-ins de interface do usuário, guia de programação
- Guia de programação, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcba6c3c7218e504a2e8752a4d1680e4887ec5aa7bfa69744fab00b27cbee797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831476"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Guia de programação de plug-ins de interface do usuário

os dois exemplos de código descritos nesta seção demonstram o processo de implementação de um plug-in de interface do usuário personalizada, começando com o código gerado pelo assistente de plug-in Windows Media Player.

O plug-in da interface do usuário de pesquisa é um plug-in de área de metadados que fornece um botão de **pesquisa** . Quando esse botão é clicado, uma página de pesquisa é iniciada no navegador da Web padrão que contém informações sobre o artista do item de mídia atual.

a primeira etapa na criação desse plug-in é iniciar um novo projeto no Microsoft Visual C++ selecionando **Windows Media Player assistente de plug-in** na guia **projetos** . Nomeie o projeto como "Pesquisar" e clique em **OK**. Escolha **plug-in de interface do usuário** e clique em **Avançar**. Em seguida, escolha o tipo de metadados na lista de opções e clique em **Avançar**. Por fim, clique na caixa de seleção para o suporte de execução automática para que o plug-in seja carregado automaticamente e clique em **concluir**. O assistente gera os arquivos de projeto necessários, incluindo as implementações básicas da classe CSearch e a interface **IWMPPluginUI** a que ela dá suporte e a classe CPluginWindow que fornece a interface do usuário. Este é o código que será modificado para fornecer a funcionalidade de plug-in descrita nesta seção.

o último tópico nesta seção descreve como criar um plug-in de interface do usuário em segundo plano para o Windows Media Player 10 Mobile. esse plug-in usa código modificado gerado pelo assistente de plug-in Windows Media Player para criar um plug-in para o Windows Media Player 10 Mobile.

Esta seção contém os seguintes tópicos.



| Tópico                                                                                                                                            | Descrição                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implementando CSearch](implementing-csearch.md)                                                                                                 | Descreve as alterações necessárias para a classe CSearch.                                |
| [Implementando CPluginWindow](implementing-cpluginwindow.md)                                                                                     | Descreve as alterações necessárias para a classe CPluginWindow.                          |
| [criando um Plug-in de Interface do usuário para o Windows Media Player 10 Mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | descreve como criar um plug-in de iu em segundo plano para Windows Media Player 10 Mobile. |



 

 

 




