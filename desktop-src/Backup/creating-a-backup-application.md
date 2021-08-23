---
title: Criando um aplicativo de backup
description: Para executar a entrada ou saída em uma fita, um aplicativo de backup deve primeiro obter um identificador do dispositivo de fita. O exemplo de código a seguir mostra como usar a função CreateFile para abrir um dispositivo de fita.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- Backup de aplicativos de backup
- Criando backup de aplicativos de backup
- Backup de backup, criando aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3086e51bce928b682d3e61518de29118abdc48461a77f79e48a4a4cb4b0f2c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529476"
---
# <a name="creating-a-backup-application"></a>Criando um aplicativo de backup

Para executar a entrada ou saída em uma fita, um aplicativo de backup deve primeiro obter um identificador do dispositivo de fita. O exemplo de código a seguir mostra como usar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um dispositivo de fita.


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



Para fazer backup de uma árvore de diretórios em uma fita, um aplicativo deve usar as funções [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para atravessar a árvore de diretórios. Cada vez que um arquivo é encontrado, o aplicativo deve obter os atributos do arquivo usando a função [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) .

Se houver links físicos, um aplicativo deverá determinar o número de links e salvar o identificador exclusivo do arquivo em uma tabela para comparações futuras. Na primeira vez em que um arquivo é encontrado, o aplicativo deve usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir o arquivo e a função [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) para iniciar o backup. Em seguida, ele pode usar a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) repetidamente para transferir todas as informações no buffer usado pelo **BackupRead** para a fita. Na segunda vez que um arquivo é encontrado (verificado em relação à tabela de identificadores de arquivo quando há links físicos), o aplicativo pode gravar as informações gerais do arquivo na fita, seguido por um fluxo que tem um identificador que é um **\_ link de backup**.

Ao restaurar arquivos de fita para disco, um aplicativo deve usar as funções [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)e [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . Para cada arquivo em uma fita, o aplicativo deve usar **CreateFile** para criar um novo arquivo em disco e **BackupWrite** para começar a restaurar o arquivo. Em seguida, o aplicativo deve usar **ReadFile** repetidamente até que todas as informações do arquivo sejam lidas da fita no buffer preenchido por **BackupWrite**.

Se um dos fluxos no buffer [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) tiver um identificador de fluxo de **\_ link de backup** , o aplicativo deverá estabelecer um vínculo físico. Se os dados necessários para estabelecer o link não existirem, o **BackupWrite** falhará. O aplicativo pode usar um catálogo pré-existente para localizar e restaurar os dados originais, ou pode notificar o usuário de que os dados de arquivo a serem restaurados estão em um local diferente.

 

 