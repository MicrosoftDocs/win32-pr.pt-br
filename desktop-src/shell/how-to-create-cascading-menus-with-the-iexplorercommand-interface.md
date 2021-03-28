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
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Como criar menus em cascata com a interface IExplorerCommand

Outra opção para adicionar verbos a um menu em cascata é por meio de [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Esse método habilita fontes de dados que fornecem seus comandos de módulo de comando por meio da interface [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) para usar esses comandos como verbos em um menu de atalho. No Windows 7 e posterior, você pode fornecer a mesma implementação de verbo usando a interface [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) como é possível com a interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .

## <a name="instructions"></a>Instruções


As duas capturas de tela a seguir ilustram o uso de menus em cascata na pasta **dispositivos** .

![Captura de tela que mostra um exemplo de um menu em cascata na pasta dispositivos.](images/file-assoc/filecascademenu.png)

![captura de tela mostrando um exemplo de um menu em cascata na pasta dispositivos](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a>Comentários

> [!Note]  
> Como o [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) dá suporte apenas à ativação em processo, é recomendável para uso por fontes de dados do shell que precisam compartilhar a implementação entre comandos e menus de atalho.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
