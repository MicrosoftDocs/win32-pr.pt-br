---
description: Outra opção para adicionar verbos a um menu em cascata é por meio de IExplorerCommand::EnumSubCommands.
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Criar menus em cascata com a interface IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed12cf78dc4b5f6a77bbd00b06897b49474a401
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436091"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Como criar menus em cascata com a interface IExplorerCommand

Outra opção para adicionar verbos a um menu em cascata é por [**meio de IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Esse método permite que fontes de dados que fornecem seus comandos de módulo de comando por meio da interface [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) use esses comandos como verbos em um menu de atalho. No Windows 7 e posteriores, você pode fornecer a mesma implementação de verbo usando a interface [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) como você pode com a interface [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)

## <a name="instructions"></a>Instruções


As duas capturas de tela a seguir ilustram o uso de menus em cascata na **pasta Dispositivos.**

![Captura de tela que mostra um exemplo de um menu em cascata na pasta dispositivos.](images/file-assoc/FileCascadeMenu.png)

![captura de tela mostrando um exemplo de um menu em cascata na pasta dispositivos](images/file-assoc/cascadeDevices2.png)

## <a name="remarks"></a>Comentários

> [!Note]  
> Como [**o IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) dá suporte apenas à ativação em processo, é recomendável usar por fontes de dados do Shell que precisam compartilhar a implementação entre comandos e menus de atalho.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**Icontextmenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
