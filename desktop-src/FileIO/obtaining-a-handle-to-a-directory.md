---
description: Sempre que um processo cria ou abre um objeto de diretório, ele recebe um identificador para o objeto.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Identificadores de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764697"
---
# <a name="directory-handles"></a>Identificadores de diretório

Sempre que um processo cria ou abre um objeto de diretório, ele recebe um identificador para o objeto.

Para obter um identificador para um diretório existente, chame a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o sinalizador de semântica de backup de sinalizador de **arquivo \_ \_ \_** .

Você pode passar um identificador de diretório para as funções a seguir.



| Função                                                         | Descrição                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | Faça backup de um arquivo ou diretório, incluindo as informações de segurança.<br/>                                                                                      |
| [**BackupSeek**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | Busca adiante em um fluxo de dados acessado inicialmente usando a função [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) ou [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .<br/> |
| [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | Restaure um arquivo ou diretório cujo backup foi feito usando o [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).<br/>                                                             |
| [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | Recupera informações de arquivo para o arquivo especificado.<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | Recupera o tamanho do arquivo especificado, em bytes.<br/>                                                                                                   |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera a data e a hora em que um arquivo ou diretório foi criado, acessado e modificado pela última vez.<br/>                                                   |
| [**Getfiletype**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | Recupera o tipo de arquivo do arquivo especificado.<br/>                                                                                                        |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | Recupera informações que descrevem as alterações no diretório especificado.<br/>                                                                      |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Define a data e a hora em que o arquivo ou diretório especificado foi criado, acessado ou modificado pela última vez.<br/>                                             |



 

 

