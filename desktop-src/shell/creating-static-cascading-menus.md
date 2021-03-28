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
# <a name="creating-static-cascading-menus"></a><span data-ttu-id="f1053-103">Criando menus em cascata estáticos</span><span class="sxs-lookup"><span data-stu-id="f1053-103">Creating Static Cascading Menus</span></span>

<span data-ttu-id="f1053-104">No Windows 7 e posterior, há suporte para implementação de menu em cascata por meio das configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="f1053-104">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="f1053-105">Antes do Windows 7, a criação de menus em cascata era possível apenas por meio da implementação da interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="f1053-105">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="f1053-106">No Windows 7 e posterior, você deve recorrer a soluções baseadas em código Component Object Model (COM) somente quando os métodos estáticos forem insuficientes.</span><span class="sxs-lookup"><span data-stu-id="f1053-106">In Windows 7 and later, you should resort to Component Object Model (COM) code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="f1053-107">A captura de tela a seguir fornece um exemplo de um menu em cascata.</span><span class="sxs-lookup"><span data-stu-id="f1053-107">The following screen shot provides an example of a cascading menu.</span></span>

![captura de tela mostrando um exemplo de um menu em cascata](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="f1053-109">No Windows 7 e posterior, há três maneiras de criar menus em cascata, que são descritos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1053-109">In Windows 7 and later, there are three ways to create cascading menus, which are described in the following sections.</span></span>

-   [<span data-ttu-id="f1053-110">Como criar menus em cascata com a entrada de registro de subcomandos</span><span class="sxs-lookup"><span data-stu-id="f1053-110">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [<span data-ttu-id="f1053-111">Como criar menus em cascata com a entrada de registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="f1053-111">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [<span data-ttu-id="f1053-112">Como criar menus em cascata com a interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="f1053-112">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
