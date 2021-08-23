---
description: As funções de criptografia bruta habilitam o backup de arquivos criptografados.
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: Backup e restauração de arquivos criptografados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34308dbfc0f67a1fcf9a70f1f7a5878434018494fa1450d308fa493af78226ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766176"
---
# <a name="backup-and-restore-of-encrypted-files"></a>Backup e restauração de arquivos criptografados

O Encrypting File System (EFS) filtra a abertura de um arquivo criptografado de forma que o aplicativo que abriu o arquivo obtém acesso às informações não criptografadas, desde que ele tenha as credenciais apropriadas para acessar o arquivo e obter a chave necessária para descriptografar o arquivo. As operações de leitura subsequentes nesse arquivo produzirão texto não criptografado. Isso é muito desejável para acesso típico a arquivos criptografados e mantém a criptografia e a descriptografia dos arquivos transparentes. No entanto, isso dificulta o backup de arquivos criptografados, pois se for tentado fazer backup com as chamadas de E/S de arquivo padrão, como [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)e [**WriteFile,**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)os arquivos que foram backupados serão a versão de texto sem-texto.

As funções de criptografia bruta são fornecidas para resolver esse problema. Os aplicativos de backup são um usuário primário destinado a essas funções. As funções de criptografia bruta diferem de outras funções do sistema de arquivos nas funções abertas, de leitura e de gravação que permitem o acesso aos fluxos de dados criptografados brutos e também permitem a leitura/gravação do fluxo $EFS. Portanto, o chamador das funções de criptografia brutas não precisa acessar as chaves criptográficas que descriptografam o arquivo. As seguintes APIs de criptografia bruta estão disponíveis para uso com aplicativos de backup e restauração: 

| API de Criptografia Bruta                                     | Descrição                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | Abra um arquivo criptografado com acesso a dados em formato criptografado. Se o chamador não tiver acesso à chave do arquivo, o chamador precisará de [SeBackupPrivilege](/windows/desktop/SecAuthZ/authorization-constants) para exportar arquivos criptografados ou SeRestorePrivilege para importar arquivos criptografados. |
| [**CloseEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | Fechar um arquivo criptografado aberto com [ **OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | Ler um arquivo criptografado deixando seus dados no formato criptografado                                                                                                                                                                                                                   |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | Gravar um arquivo criptografado deixando seus dados no formato criptografado                                                                                                                                                                                                                  |
| [**ImportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | Retorno de chamada definido pelo aplicativo para uso [ **com WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**ExportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | Retorno de chamada definido pelo aplicativo para uso [ **com ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
