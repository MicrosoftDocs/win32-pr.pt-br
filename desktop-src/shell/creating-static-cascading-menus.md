---
description: A partir do Windows 7, os menus em cascata são criados por meio da entrada de registro de subcomandos, da entrada de registro ExtendedSubCommandsKey ou da interface IExplorerCommand.
title: Criando menus em cascata estáticos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d812b4d3d2fb0754002cb37d72718e4fe861ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560129"
---
# <a name="creating-static-cascading-menus"></a>Criando menus em cascata estáticos

No Windows 7 e posterior, há suporte para implementação de menu em cascata por meio das configurações do registro. Antes do Windows 7, a criação de menus em cascata era possível apenas por meio da implementação da interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . No Windows 7 e posterior, você deve recorrer a soluções baseadas em código Component Object Model (COM) somente quando os métodos estáticos forem insuficientes.

A captura de tela a seguir fornece um exemplo de um menu em cascata.

![captura de tela mostrando um exemplo de um menu em cascata](images/file-assoc/filecascademenu2ndex.png)

No Windows 7 e posterior, há três maneiras de criar menus em cascata, que são descritos nas seções a seguir.

-   [Como criar menus em cascata com a entrada de registro de subcomandos](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Como criar menus em cascata com a entrada de registro ExtendedSubCommandsKey](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Como criar menus em cascata com a interface IExplorerCommand](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
