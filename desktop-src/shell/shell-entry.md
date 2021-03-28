---
description: A interface do usuário do Windows fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional.
title: Shell do Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967988"
---
# <a name="windows-shell"></a>Shell do Windows

A interface do usuário do Windows fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional. Os mais numerosos e familiares desses objetos são as pastas e os arquivos que residem nas unidades de disco do computador. Também há uma série de objetos virtuais que permitem ao usuário executar tarefas como enviar arquivos para impressoras remotas ou acessar a lixeira. O Shell organiza esses objetos em um namespace hierárquico e fornece aos usuários e aplicativos uma maneira consistente e eficiente de acessar e gerenciar objetos.

## <a name="shell-development-scenarios"></a>Cenários de desenvolvimento do Shell

Os cenários de desenvolvimento a seguir estão relacionados ao desenvolvimento de aplicativos:

-   Estendendo o Shell, que consiste em criar uma fonte de dados (versus consumir o modelo de dados do Shell)
-   Implementando um subconjunto das tarefas da fonte de dados do Shell
-   Suporte a bibliotecas e exibições de itens no Windows Explorer
-   Usando a caixa de diálogo arquivo comum
-   Implementando itens do painel de controle
-   Gerenciando notificações

Os cenários de desenvolvimento a seguir estão relacionados à propriedade do formato de arquivo:

-   Implementando um subconjunto das tarefas da fonte de dados do Shell
-   Implementando qualquer manipulador
-   Suporte à pesquisa na área de trabalho

Os cenários de desenvolvimento a seguir estão relacionados à propriedade de armazenamento de dados:

-   Suporte à pesquisa de desktop e OpenSearch
-   Implementando um subconjunto das tarefas da fonte de dados do Shell (pastas virtuais)
-   Suporte a bibliotecas no Windows Explorer

O cenário de desenvolvimento a seguir está relacionado ao suporte do dispositivo:

-   Execução automática e reprodução automática

## <a name="windows-shell-sdk-documentation"></a>Documentação do SDK do shell do Windows

Esta documentação é dividida em três seções principais:

-   O [Guia do desenvolvedor do Shell](intro.md) fornece material conceitual sobre como o Shell funciona e como usar a API do Shell em seu aplicativo.
-   A seção de [referência do Shell](shell-reference-bumper.md) documenta os elementos de programação que compõem as várias APIs do Shell.
-   [Exemplos de shell](samples-entry.md) fornece links para exemplos de código relacionados.

A tabela a seguir fornece uma descrição da seção de referência do Shell. Salvo indicação em contrário, todos os elementos de programação são documentados em C++ não gerenciado.



| Seção                                                               | Descrição                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Classes de Shell](classes.md)                                          | Esta seção descreve a seleção de classes de shell do Windows.                                                                 |
| [Interfaces do Shell](interfaces.md)                                    | Esta seção descreve as interfaces do Windows Shell Component Object Model (COM).                                    |
| [Funções do Shell](functions.md)                                      | Esta seção descreve as funções do shell do Windows.                                                                  |
| [Funções de retorno de chamada do Shell](callbacks.md)                             | Esta seção descreve os modelos de funções de retorno de chamada do shell do Windows.                                               |
| [Constantes, enumerações e sinalizadores do Shell](consts-enums-flags.md)    | Esta seção descreve as constantes do shell do Windows, as enumerações e os sinalizadores usados nas APIs do Shell.                  |
| [Funções do utilitário Lightweight do Shell](shlwapi.md)                    | Esta seção descreve as funções do utilitário Windows Shell Lightweight fornecidas no Shlwapi.dll.                      |
| [Macros do Shell](macros.md)                                            | Esta seção descreve as macros do utilitário de shell do Windows.                                                             |
| [Mensagens e notificações do Shell](messages.md)                      | Esta seção descreve as mensagens e notificações enviadas por elementos do shell do Windows.                         |
| [Objetos do Shell para scripts e Microsoft Visual Basic](objects.md) | Esta seção descreve os objetos do Windows implementados pelo shell para uso no script e no Microsoft Visual Basic. |
| [Objetos do Shell para C++](objects-cpp.md)                              | Esta seção descreve os objetos C++ do Windows implementados pelo shell.                                             |
| [Esquemas de Shell](schemas.md)                                          | Esta seção descreve a biblioteca, a propriedade e os esquemas de manifesto de transferência usados pelo shell do Windows.                   |
| [Estruturas do Shell](structures.md)                                    | Esta seção descreve as estruturas de shell do Windows usadas nas APIs do Shell.                                          |



 

 

 



