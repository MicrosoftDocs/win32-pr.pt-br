---
description: Funções a serem usadas para obter e definir informações de arquivo.
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: Obtendo e configurando informações do arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837336"
---
# <a name="obtaining-and-setting-file-information"></a>Obtendo e configurando informações do arquivo

Os tópicos a seguir descrevem como obter e definir informações de arquivo.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                             | Descrição                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recuperando informações de tipo de arquivo](retrieving-file-type-information.md)<br/>                               | A função [**Getfiletype**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) recupera o tipo de um arquivo: disco, caractere (como um console), pipe ou desconhecido.<br/>                                                                                                                                               |
| [Determinando o tamanho de um arquivo](determining-the-size-of-a-file.md)<br/>                                   | A função [**GetFiles**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera o tamanho de um arquivo.<br/>                                                                                                                                                                                                      |
| [Procurando um ou mais arquivos](searching-for-one-or-more-files.md)<br/>                                 | Um aplicativo pode pesquisar o diretório atual em busca de todos os nomes de arquivo que correspondam a um determinado padrão usando as funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .<br/> |
| [Configurando e obtendo o carimbo de data/hora de um arquivo](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | Os aplicativos podem recuperar e definir a data e a hora em que um arquivo é criado, modificado pela última vez ou acessado pela última vez usando as funções [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) e [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .<br/>                                                                         |
| [Determinando a página de código do conjunto de caracteres atual](determining-the-current-character-set-code-page.md)<br/> | A função [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina se as funções de e/s de arquivo estão usando a página de código do conjunto de caracteres ANSI ou OEM.<br/>                                                                                                                               |



 

 

