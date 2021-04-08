---
description: As funções de criptografia brutas permitem o backup de arquivos criptografados.
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: Backup e restauração de arquivos criptografados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbc5d1babbbbb92cef9e78f9a0dade702fd63d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010655"
---
# <a name="backup-and-restore-of-encrypted-files"></a>Backup e restauração de arquivos criptografados

O sistema de arquivos com criptografia (EFS) filtra a abertura de um arquivo criptografado de forma que o aplicativo que abriu o arquivo obtenha acesso às informações não criptografadas, desde que ele tenha as credenciais apropriadas para acessar o arquivo e obter a chave necessária para descriptografar o arquivo. As operações de leitura subsequentes neste arquivo resultarão em texto não criptografado. Isso é muito desejável para acesso típico a arquivos criptografados e mantém a criptografia e a descriptografia dos arquivos transparentes. No entanto, ele impede o backup de arquivos criptografados, porque se o backup for tentado com as chamadas de e/s de arquivo padrão como [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), o backup dos arquivos será a versão de texto sem formatação.

As funções de criptografia bruta são fornecidas para resolver esse problema. Os aplicativos de backup são um usuário principal pretendido para essas funções. As funções de criptografia brutas diferem de outras funções do sistema de arquivos nas funções abrir, ler e gravar permitem o acesso aos fluxos de dados criptografados brutos e também permitem a leitura/gravação do fluxo de $EFS. Portanto, o chamador das funções de criptografia bruta não precisa acessar as chaves de criptografia que descriptografam o arquivo. As seguintes APIs de criptografia bruta estão disponíveis para uso com aplicativos de backup e restauração: 

| API de criptografia bruta                                     | Descrição                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | Abra um arquivo criptografado com acesso aos dados em formato criptografado. Se o chamador não tiver acesso à chave do arquivo, o chamador precisará de [SeBackupPrivilege](/windows/desktop/SecAuthZ/authorization-constants) para exportar arquivos criptografados ou SeRestorePrivilege para importar arquivos criptografados. |
| [**CloseEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | Fechar um arquivo criptografado aberto com [ **OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | Ler um arquivo criptografado deixando seus dados no formato criptografado                                                                                                                                                                                                                   |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | Gravar um arquivo criptografado deixando seus dados no formato criptografado                                                                                                                                                                                                                  |
| [**ImportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | Retorno de chamada definido pelo aplicativo para uso com [ **WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**ExportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | Retorno de chamada definido pelo aplicativo para uso com [ **ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
