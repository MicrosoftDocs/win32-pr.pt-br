---
description: Como você pode usar as funções de backup dos serviços de certificados para fazer backup de um banco de dados de serviços de certificados e de seus arquivos associados.
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: Fazendo backup dos serviços de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1be929fcf3bd9b8b9655b48758a97d19af7abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837283"
---
# <a name="backing-up-certificate-services"></a>Fazendo backup dos serviços de certificados

Veja a seguir um cenário que mostra como você pode usar as funções de backup dos serviços de certificados para fazer backup de um banco de dados de serviços de certificados e de seus arquivos associados.

1.  Carregue a biblioteca de Certadm.dll na memória (chamando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recupere o endereço de cada uma das funções necessárias no Certadm.dll (por meio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Use esses endereços ao chamar as funções nas etapas restantes.
3.  Chame [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) para determinar se os serviços de certificados estão online. Os serviços de certificados devem estar online para que as operações de backup sejam bem-sucedidas.
4.  Chame [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) para iniciar uma sessão de backup. O identificador de contexto de backup dos serviços de certificados resultantes será usado por muitas das outras funções de backup.
5.  Chame [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) para determinar o mapa de restauração. O mapa de restauração contém os caminhos a serem usados durante a restauração do backup. Salve as informações recuperadas por **CertSrvRestoreGetDatabaseLocations** em um local específico do aplicativo.
6.  Chame [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) para determinar os nomes dos arquivos de banco de dados para backup. Para cada um desses arquivos, execute as etapas 7 a 9.
7.  Chame [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) para abrir o arquivo para backup.
8.  Chame [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) para ler uma parte de bytes do arquivo e, em seguida, chame uma rotina específica do aplicativo para armazenar os bytes em um meio de backup. Repita essa etapa até que todos os bytes no arquivo sejam submetidos a backup.
9.  Chame [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) para fechar o arquivo.
10. Chame [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) para determinar os nomes dos arquivos de log para backup. Para cada um desses arquivos, execute as etapas 7 a 9.
11. Chame [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) para truncar os arquivos de log que foram copiados em backup nas etapas 6 e 10. Esta etapa é opcional; no entanto, chame **CertSrvBackupTruncateLogs** somente se todos os arquivos retornados por [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) e [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) tiverem sido submetidos a backup (caso contrário, a operação de restauração falhará). Consulte a página de referência do **CertSrvBackupTruncateLogs** para obter detalhes.
12. Chame [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) para determinar os nomes dos arquivos que não são de banco de dados para backup. Esses arquivos são identificados apenas pela função e devem ser submetidos a backup por outros meios.
13. Faça backup dos arquivos dinâmicos identificados na etapa 12, usando rotinas separadas de Certadm.dll.
14. Chame [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) para encerrar a sessão de backup.
15. Chame [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) conforme necessário para liberar buffers alocados por determinadas funções de backup dos serviços de certificados. Chamadas para [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw), [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)e [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) alocarão buffers que podem ser liberados por uma chamada para **CertSrvBackupFree**.
16. Libere os recursos de Certadm.dll chamando [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary).

Para obter informações sobre os privilégios necessários para fazer backup do banco de dados dos serviços de certificados e dos arquivos associados, consulte [definindo os privilégios de backup e restauração](setting-the-backup-and-restore-privileges.md).

 

 
