---
description: A partir Windows 7, os menus em cascata são criados por meio da entrada do Registro SubCommands, da entrada do Registro ExtendedSubCommandsKey ou da interface IExplorerCommand.
title: Criando menus em cascata estáticos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 22fdc261012697affd99b5a1491ef5829fcc5329d5570ae4e3c37dcd111b457f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456326"
---
# <a name="creating-static-cascading-menus"></a>Criando menus em cascata estáticos

No Windows 7 e posteriores, há suporte para a implementação do menu em cascata por meio das configurações do Registro. Antes Windows 7, a criação de menus em cascata era possível apenas por meio da implementação da interface [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) No Windows 7 e posterior Component Object Model es, você deve recorrer a soluções baseadas em código (COM) somente quando os métodos estáticos não são suficientes.

A captura de tela a seguir fornece um exemplo de um menu em cascata.

![captura de tela mostrando um exemplo de um menu em cascata](images/file-assoc/filecascademenu2ndex.png)

No Windows 7 e posterior, há três maneiras de criar menus em cascata, que são descritos nas seções a seguir.

-   [Como criar menus em cascata com a entrada do Registro SubCommands](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Como criar menus em cascata com a entrada do Registro ExtendedSubCommandsKey](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Como criar menus em cascata com a interface IExplorerCommand](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
