---
description: Funções usadas no gerenciamento de diretório.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Funções de gerenciamento de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bc10d0f8d7caddc1ea821c397e16edf600d92c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171145"
---
# <a name="directory-management-functions"></a>Funções de gerenciamento de diretório

As funções a seguir são usadas no gerenciamento de diretório.

## <a name="in-this-section"></a>Nesta seção



| Função                                                                      | Descrição                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | Cria um novo diretório.<br/>                                                                                                                                       |
| [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | Cria um novo diretório com os atributos de um diretório de modelo especificado.<br/>                                                                                 |
| [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | Cria um novo diretório como uma operação transacionada, com os atributos de um diretório de modelo especificado.<br/>                                                      |
| [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | Interrompe o monitoramento do identificador de notificação de alteração.<br/>                                                                                                                   |
| [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | Cria um identificador de notificação de alteração e configura as condições de filtro de notificação de alteração iniciais.<br/>                                                                |
| [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | Solicita que o sistema operacional sinalize um identificador de notificação de alteração na próxima vez que detectar uma alteração apropriada.<br/>                                         |
| [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | Recupera o diretório atual para o processo atual.<br/>                                                                                                       |
| [**ReadDirectoryChangesExW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | Recupera informações que descrevem as alterações no diretório especificado, que pode incluir informações estendidas se esse tipo de informação for especificado.<br/> |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | Recupera informações que descrevem as alterações no diretório especificado.<br/>                                                                               |
| [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | Exclui um diretório vazio existente.<br/>                                                                                                                           |
| [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | Exclui um diretório vazio existente como uma operação transacionada.<br/>                                                                                                 |
| [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | Altera o diretório atual para o processo atual.<br/>                                                                                                         |



 

 

 




