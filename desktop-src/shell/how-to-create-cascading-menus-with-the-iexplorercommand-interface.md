---
description: 'Outra opção para adicionar verbos a um menu em cascata é por meio de IExplorerCommand:: EnumSubCommands.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Criar menus em cascata com a interface IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104560954"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="5696e-103">Como criar menus em cascata com a interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="5696e-103">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="5696e-104">Outra opção para adicionar verbos a um menu em cascata é por meio de [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="5696e-104">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="5696e-105">Esse método habilita fontes de dados que fornecem seus comandos de módulo de comando por meio da interface [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) para usar esses comandos como verbos em um menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="5696e-105">This method enables data sources that provide their command module commands through the [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) interface to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="5696e-106">No Windows 7 e posterior, você pode fornecer a mesma implementação de verbo usando a interface [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) como é possível com a interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="5696e-106">In Windows 7 and later, you can provide the same verb implementation using the [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) interface as you can with the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span>

## <a name="instructions"></a><span data-ttu-id="5696e-107">Instruções</span><span class="sxs-lookup"><span data-stu-id="5696e-107">Instructions</span></span>


<span data-ttu-id="5696e-108">As duas capturas de tela a seguir ilustram o uso de menus em cascata na pasta **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="5696e-108">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Captura de tela que mostra um exemplo de um menu em cascata na pasta dispositivos.](images/file-assoc/filecascademenu.png)

![captura de tela mostrando um exemplo de um menu em cascata na pasta dispositivos](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a><span data-ttu-id="5696e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5696e-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5696e-112">Como o [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) dá suporte apenas à ativação em processo, é recomendável para uso por fontes de dados do shell que precisam compartilhar a implementação entre comandos e menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="5696e-112">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5696e-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5696e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5696e-114">**IExplorerCommand**</span><span class="sxs-lookup"><span data-stu-id="5696e-114">**IExplorerCommand**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[<span data-ttu-id="5696e-115">**IExplorerCommandProvider**</span><span class="sxs-lookup"><span data-stu-id="5696e-115">**IExplorerCommandProvider**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[<span data-ttu-id="5696e-116">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="5696e-116">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
