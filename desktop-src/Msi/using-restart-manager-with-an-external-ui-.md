---
description: Windows Installer os desenvolvedores podem preparar seu pacote de instalação para trabalhar com o Gerenciador de reinicialização seguindo as diretrizes descritas em usando o Windows Installer com o Gerenciador de reinicialização.
ms.assetid: 777f8864-b3d2-43c7-9296-1118f3595d7b
title: Usando o Gerenciador de reinicialização com uma interface do usuário externa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f112884669b173b40f3806c48cf8e05308c5b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164505"
---
# <a name="using-restart-manager-with-an-external-ui"></a>Usando o Gerenciador de reinicialização com uma interface do usuário externa

Windows Installer os desenvolvedores podem preparar seu pacote de instalação para trabalhar com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) seguindo as diretrizes descritas em [usando o Windows Installer com o Gerenciador de reinicialização](using-windows-installer-with-restart-manager.md).

Especifique o \_ tipo de mensagem INSTALLLOGMODE RMFILESINUSE ao chamar a função [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) ou [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) para habilitar o manipulador de interface de usuário externa. Em seguida, Windows Installer envia uma \_ mensagem INSTALLMESSAGE RMFILESINUSE para uso por manipuladores de interface do usuário externos que dão suporte ao [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md).

O manipulador de interface do usuário externo deve lidar com as informações contidas em mensagens do INSTALLMESSAGE \_ RMFILESINUSE. Se nenhuma interface de usuário registrada ou interna manipular a \_ mensagem INSTALLMESSAGE RMFILESINUSE, Windows Installer enviará uma \_ mensagem INSTALLMESSAGE FILESINUSE para uso por manipuladores externos existentes que dão suporte a INSTALLMESSAGE FILESINUSE \_ mensagens e a caixa de diálogo [FILESINUSE](filesinuse-dialog.md) .

A interface do usuário externa pode retornar os valores listados na tabela a seguir.



| Valor de retorno da interface do usuário externa | Ação realizada pelo Windows Installer                                                                                                                                                                                                                                                                                                              |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDOK                     | O botão **OK** foi pressionado pelo usuário. O Windows Installer solicitará que o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) desligue e reinicie os aplicativos que mantêm os arquivos em uso no momento.                                                                                                                                               |
| IDCANCEL                 | O botão **Cancelar** foi pressionado. Cancele a instalação.                                                                                                                                                                                                                                                                                    |
| IDIGNORE                 | O botão **ignorar** foi pressionado. Ignorar e continuar a instalação. Uma reinicialização será necessária no final da instalação.                                                                                                                                                                                                            |
| IDNO                     | O botão **não** foi pressionado. Se o pacote tiver uma caixa de diálogo [MsiRMFilesInUse](msirmfilesinuse-dialog.md) , envie uma mensagem 1610. Para obter mais informações, consulte [Windows Installer mensagens de erro](windows-installer-error-messages.md). Se o pacote não tiver uma caixa de diálogo MsiRMFilesInUse, envie uma \_ mensagem INSTALLMESSAGE FILESINUSE. |
| IDRETRY                  | O botão de **repetição** foi pressionado. Envie a \_ mensagem INSTALLMESSAGE FILESINUSE.                                                                                                                                                                                                                                                                 |
| -1                       | Um erro. Encerre a instalação.                                                                                                                                                                                                                                                                                                                |



 

 

 
