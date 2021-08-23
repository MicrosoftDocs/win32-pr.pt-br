---
description: Esta seção discute a criação de menus de atalho (contexto) e a implementação de manipuladores de menu de atalho (verbo).
title: Menus de atalho (contexto) e manipuladores de menu de atalho
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c091588ff3fefb94d7cd06656c4d7206156b03932c4876f20ad0f26aa03b8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715726"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a>Menus de atalho (contexto) e manipuladores de menu de atalho

Esta seção discute a criação de menus de atalho (contexto) e a implementação de manipuladores de menu de atalho (verbo).

Esta seção sobre tipos de arquivo e associações de arquivo é organizada da seguinte maneira:

-   [Verbos e associações de arquivo](fa-verbs.md)
-   [Escolhendo um método de menu de atalho estático ou dinâmico](shortcut-choose-method.md)
-   [Práticas recomendadas para manipuladores de menu de atalho e vários verbos](verbs-best-practices.md)
-   [Como Criar Manipuladores do Menu de Atalho](context-menu-handlers.md)
-   [Criando menus em cascata estáticos](creating-static-cascading-menus.md)
-   [Como suprimir e controlar a visibilidade de verbo](how-to-suppress-and-control-visibility.md)
-   [Como empregar o modelo de seleção de verbo](how-to-employ-the-verb-selection-model.md)
-   [Como usar atributos de item](how-to-use-item-attributes.md)
-   [Como implementar verbos personalizados para pastas por meio de Desktop.ini](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md)
-   [Como implementar a interface IContextMenu](how-to-implement-the-icontextmenu-interface.md)
-   [Referência do menu de atalho](context-menu-reference.md)

## <a name="additional-resources"></a>Recursos adicionais

Para obter informações conceituais relacionadas, consulte os seguintes tópicos:

-   [Introdução às associações de arquivo](fa-intro.md).
-   Para estender o shell com manipuladores de tipo de arquivo, consulte [criando manipuladores de extensão de shell](handlers.md).
-   Para criar um armazenamento de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](nse-implement.md).

Para obter documentação de referência relacionada, consulte os seguintes tópicos:

-   Para executar um verbo em um item de Shell, consulte o método [**InvokeVerb**](folderitem-invokeverb.md) .
-   Para recuperar uma coleção de verbos que podem ser executados em um item de Shell, consulte o método [**Verbs**](folderitem-verbs.md) .
-   Para executar uma operação em um arquivo especificado, consulte as funções [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

 

 



