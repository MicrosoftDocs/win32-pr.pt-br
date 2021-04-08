---
description: Uma pequena atualização pode ser aplicada a um aplicativo por meio da reinstalação completa ou parcial do aplicativo da linha de comando ou de um programa.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Aplicando pequenas atualizações reinstalando o produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921513"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>Aplicando pequenas atualizações reinstalando o produto

Uma pequena atualização pode ser aplicada a um aplicativo por meio da reinstalação completa ou parcial do aplicativo da linha de comando ou de um programa.

**Para propagar a pequena atualização para os usuários atuais (esta é uma reinstalação completa) da linha de comando**

1.  Na linha de comando, use: **msiexec/fvomus \[** _caminho para o arquivo. msi atualizado_ *_\]_* ou **msiexec \[ /i** _caminho para atualizado o arquivo. msi_ *_\] reinstalar = todos os REINSTALLMODE = vomus_*.
2.  O arquivo. msi atualizado é armazenado em cache no computador do usuário. Observe que não é possível que o usuário reinstale o produto usando Adicionar/remover programas porque o arquivo. msi atualizado ainda não está no computador do usuário.

**Para propagar uma pequena atualização para os usuários atuais (esta é uma reinstalação completa) de um programa**

1.  A partir de um programa, chame [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) e especifique o pacote REINSTALLMODE \_ , o REINSTALLMODE \_ FILEOLDERVERSION, o REINSTALLMODE \_ MACHINEDATA, o o \_ UserData e o \_ atalho REINSTALLMODE
2.  O arquivo. msi atualizado é armazenado em cache no computador do usuário.

O método a seguir inicia uma reinstalação somente de recursos ou componentes afetados pela atualização pequena.

**Para propagar uma pequena atualização para os usuários atuais (esta é uma reinstalação parcial)**

1.  Obtenha uma lista dos nomes de recursos e componentes afetados pela atualização pequena.
2.  No prompt de comando, use: **msiexec \[ /i** _caminho para atualizado o arquivo. msi_ *_\] reinstalar = \[_* lista _\] de recursos_ **REINSTALLMODE = vomus**.
3.  O arquivo. msi atualizado é armazenado em cache no computador do usuário.

 

 



