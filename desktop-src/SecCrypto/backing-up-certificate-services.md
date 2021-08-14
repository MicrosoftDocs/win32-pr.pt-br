---
description: Como você pode usar as funções de backup dos Serviços de Certificados para fazer backup de um banco de dados dos Serviços de Certificados e seus arquivos associados.
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: Fazer o back-up de serviços de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeeb0881d517de538971d7eafb835ec48f3f33328e3a026b450e6719bfb23ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773082"
---
# <a name="backing-up-certificate-services"></a>Fazer o back-up de serviços de certificado

Veja a seguir um cenário que mostra como você pode usar as funções de backup dos Serviços de Certificados para fazer backup de um banco de dados dos Serviços de Certificados e seus arquivos associados.

1.  Carregue a Certadm.dll na memória (chamando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recupere o endereço de cada uma das funções necessárias no Certadm.dll (por meio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Use esses endereços ao chamar as funções nas etapas restantes.
3.  Chame [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) para determinar se os Serviços de Certificados estão online. Os Serviços de Certificados devem estar online para que as operações de backup sejam bem-sucedidas.
4.  Chame [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) para iniciar uma sessão de backup. O alça de contexto de backup dos Serviços de Certificado resultante será usado por muitas das outras funções de backup.
5.  Chame [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) para determinar o mapa de restauração. O mapa de restauração contém os caminhos a serem usados ao restaurar o backup. Salve as informações recuperadas por **CertSrvRestoreGetDatabaseLocations** em um local específico do aplicativo.
6.  Chame [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) para determinar os nomes dos arquivos de banco de dados para backup. Para cada um desses arquivos, execute as etapas 7 a 9.
7.  Chame [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) para abrir o arquivo para backup.
8.  Chame [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) para ler uma parte dos bytes do arquivo e, em seguida, chame uma rotina específica do aplicativo para armazenar os bytes em uma mídia de backup. Repita essa etapa até que todos os bytes no arquivo sejam copiados em backup.
9.  Chame [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) para fechar o arquivo.
10. Chame [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) para determinar os nomes dos arquivos de log para backup. Para cada um desses arquivos, execute as etapas 7 a 9.
11. Chame [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) para truncar os arquivos de log que foram backupados nas etapas 6 e 10. Esta etapa é opcional; No entanto, chame **CertSrvBackupTruncateLogs somente** se todos os arquivos retornados por [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) e [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) foram armazenados em backup (caso contrário, a operação de restauração falhará). Consulte a **página de referência CertSrvBackupTruncateLogs** para obter detalhes.
12. Chame [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) para determinar os nomes dos arquivos que não são de banco de dados para backup. Esses arquivos são identificados apenas pela função e devem ser armazenados em backup por outros meios.
13. Faça backup dos arquivos dinâmicos identificados na etapa 12, usando rotinas separadas das Certadm.dll.
14. Chame [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) para encerrar a sessão de backup.
15. Chame [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) conforme necessário para liberar buffers alocados por determinadas funções de backup dos Serviços de Certificados. Chamadas para [**CertSrvBackupGetBackupLogs,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)e [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) alocarão buffers que podem ser liberados por uma chamada para **CertSrvBackupFree**.
16. Libere os Certadm.dll recursos chamando [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary).

Para obter informações sobre os privilégios necessários para fazer backup do banco de dados dos Serviços de Certificados e dos arquivos [associados,](setting-the-backup-and-restore-privileges.md)consulte Configurando os privilégios de backup e restauração.

 

 
