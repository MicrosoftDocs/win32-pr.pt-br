---
description: Uma pequena atualização pode ser aplicada a um aplicativo reinstalando completamente ou parcialmente o aplicativo da linha de comando ou de um programa.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Aplicando pequenas atualizações reinstalando o produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb128ec3b62b3f81e8a1f9762bda715fa21e010fa4c16d16c8ca377aa4c5ce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145849"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>Aplicando pequenas atualizações reinstalando o produto

Uma pequena atualização pode ser aplicada a um aplicativo reinstalando completamente ou parcialmente o aplicativo da linha de comando ou de um programa.

**Para propagar a pequena atualização para os usuários atuais (esta é uma reinstalação completa) da linha de comando**

1.  Na linha de comando, use: **msiexec /fvomus \[** path to _updated .msi file_ or *_\]_* **msiexec /I \[** path to updated .msi _file_ *_\] REINSTALL=ALL REINSTALLMODE=vomus_*.
2.  O arquivo .msi é armazenado em cache no computador do usuário. Observe que não é possível que o usuário reinstale o produto usando Adicionar/Remover Programas porque o arquivo .msi atualizado ainda não está no computador do usuário.

**Para propagar uma pequena atualização para os usuários atuais (esta é uma reinstalação completa) de um programa**

1.  Em um programa, chame [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) e especifique \_ REINSTALLMODE PACKAGE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE USERDATA e \_ REINSTALLMODE \_ SHORTCUT
2.  O arquivo .msi é armazenado em cache no computador do usuário.

O método a seguir inicia uma reinstalação apenas dos recursos ou componentes afetados pela pequena atualização.

**Para propagar uma pequena atualização para os usuários atuais (esta é uma reinstalação parcial)**

1.  Obtenha uma lista dos nomes de recursos e componentes afetados pela pequena atualização.
2.  No prompt de comando, use: **caminho \[ msiexec /I** para o arquivo _.msi_ *_\] atualizado REINSTALL= \[_*_Lista \]_ de recursos **REINSTALLMODE=vomus**.
3.  O arquivo .msi é armazenado em cache no computador do usuário.

 

 



