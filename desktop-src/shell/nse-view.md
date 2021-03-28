---
description: A maioria das extensões de namespace são um subconjunto do namespace do Shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Exibindo uma exibição Self-Contained de uma extensão de namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968014"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a>Exibindo uma exibição Self-Contained de uma extensão de namespace

A maioria das extensões de namespace são um subconjunto do namespace do Shell. Quando você cria um ponto de junção, conforme descrito em [especificando o local de uma extensão de namespace](nse-junction.md), o Windows Explorer permite que os usuários naveguem para dentro e para fora da extensão do namespace, assim como qualquer outra pasta. No entanto, também é possível usar o Windows Explorer para exibir apenas o conteúdo da extensão do namespace. Essa opção de exibição às vezes é chamada de *exibição com raiz*. Embora não seja comumente usado, as exibições com raiz podem ser preferíveis às exibições normais para alguns tipos de extensões.

Com uma exibição com raiz, é criada uma nova instância do Windows Explorer que exibe o conteúdo da extensão como um namespace separado. O modo de exibição de árvore de uma exibição com raiz mostra apenas as pastas que fazem parte da extensão. Os usuários não podem navegar de uma exibição com raiz para outras partes do namespace do Shell.

As extensões são implementadas da mesma maneira para exibições com raiz, como são para exibições normais. A única diferença está na maneira como o conteúdo da extensão é exibido pelo Windows Explorer. É possível até mesmo ter exibições normais e com raiz da mesma extensão.

Para abrir uma exibição de uma extensão, você deve iniciar uma instância do Explorer.exe com um sinalizador/root. Há várias maneiras diferentes de iniciar uma exibição com raiz, dependendo da natureza de sua extensão.

-   [Como usar um ponto de junção para abrir uma exibição com raiz](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [Como usar um arquivo de atalho para abrir uma exibição com raiz](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [Como exibir uma exibição com raiz de um arquivo](how-to-display-a-rooted-view-of-a-file.md)

 

 



