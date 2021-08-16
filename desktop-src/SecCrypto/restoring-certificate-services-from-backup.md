---
description: Mostra como as funções de backup de serviços de certificados podem ser usadas para restaurar e recuperar um banco de dados de serviços de certificados e seus arquivos associados.
ms.assetid: f4914f45-629d-4f24-8328-d7f27e8a0062
title: Restaurando serviços de certificados a partir do backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665a1aed873cdf25f24dc5a7bc8b8466a5c3ae7a6c1aaf6bec07d2e8be336e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900519"
---
# <a name="restoring-certificate-services-from-backup"></a>Restaurando serviços de certificados a partir do backup

O cenário a seguir mostra como as funções de backup de serviços de certificados podem ser usadas para restaurar e recuperar um banco de dados de serviços de certificados e seus arquivos associados. O processo de restauração envolve a gravação dos arquivos contidos em um conjunto de backup em disco. Você pode restaurar vários conjuntos de backup (um backup completo, mais zero ou mais backups incrementais), mas todas as restaurações devem ser concluídas antes de iniciar o processo de recuperação. O processo de recuperação envolve a reprodução dos serviços de certificados para garantir a consistência do arquivo de log e do banco de dados, garantindo assim a integridade do banco de dados. O cenário ilustra as chamadas de função para restaurar os conjuntos de backup e informar os serviços de certificados dos parâmetros de recuperação.

Um backup completo existente do banco de dados de serviços de certificados deve existir antes da implementação desse cenário.

1.  Carregue a biblioteca de Certadm.dll na memória (chamando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recupere o endereço de cada uma das funções necessárias no Certadm.dll (por meio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Use esses endereços ao chamar as funções nas etapas restantes.
3.  Chame [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) para determinar se os serviços de certificados estão online. Se os serviços de certificados estiverem em execução, desligue-os antes de continuar. Os serviços de certificados não devem estar online para que as operações de restauração tenham êxito.
4.  Chame [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew) para iniciar uma sessão de restauração. O identificador de contexto de backup dos serviços de certificados resultantes será usado por várias das outras funções.
5.  Determine o caminho para o local do banco de dados. Durante um cenário de backup, esse valor teria sido disponibilizado de uma chamada para [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw); Esse valor deve ter sido armazenado como parte do backup.
6.  Crie um mapa de restauração especificando o nome do banco de dados restaurado. Uma estrutura de mapeamento de restauração do banco de dados dos serviços de certificado (CSEDB \_ RSTMAPW) é usada para especificar um mapa de restauração. Defina o \_ membro **PWSZDATABASENAME** do CSEDB RSTMAPW e o \_ membro **RSTMAPW** do CSEDB pwszNewDatabaseName para o local do banco de dados determinado na etapa 5. Opcionalmente, se o banco de dados restaurado tiver um nome diferente do banco de dados de backup, defina o \_ membro **PWSZNEWDATABASENAME** do CSEDB RSTMAPW como o novo nome do banco de dados.
7.  Se você quiser garantir que as modificações feitas no banco de dados após a execução do backup não sejam reaplicadas após a conclusão da restauração do banco de dados (como parte da recuperação do banco de dados executada durante a próxima inicialização dos serviços de certificado), exclua os arquivos do banco de dados ativo do servidor de destino e dos diretórios de log.
8.  Copie os arquivos contidos no backup completo para o banco de dados ativo do servidor de destino e os diretórios de log.
9.  Chame [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw) para registrar uma operação de restauração para o backup completo. **CertSrvRestoreRegister** usa o mapa de restauração especificado na etapa 6. **CertSrvRestoreRegister** também especifica o local do banco de dados e dos logs de backup. Chamar **CertSrvRestoreRegister** forçará os serviços de certificados a tentarem uma operação de restauração na próxima vez em que for iniciado. Ele também impede que os serviços de certificados processem solicitações de certificado até que a restauração seja concluída.
10. Chame [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete), concluindo assim a atividade de registro iniciada na etapa 8. Observe que o registro de uma operação de restauração é uma instrução para que os serviços de certificados sejam seguidos quando ele é iniciado; a recuperação real ocorrerá somente depois que os serviços de certificados forem iniciados.
11. Para cada backup incremental a ser restaurado, copie os arquivos contidos no backup incremental para o diretório de log ativo do servidor de destino e, em seguida, chame [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw), seguido por uma chamada para [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete). O registro dos backups incrementais para restauração pode ocorrer em qualquer ordem, mas somente o conjunto de arquivos para um backup incremental deve ser copiado para o servidor antes de cada chamada para **CertSrvRestoreRegister**.
12. Copie os arquivos dinâmicos dos serviços de certificados para o servidor de destino. Os arquivos dinâmicos seriam identificados durante o backup quando [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) foi chamado. Pode ser necessário parar o serviço de publicação de World Wide Web para permitir a substituição dos arquivos dinâmicos.
13. Chame [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend) para encerrar a sessão de restauração.
14. Inicie o aplicativo de serviços de certificados manualmente (ou aguarde a próxima reinicialização para que ele seja iniciado automaticamente). Quando os serviços de certificados são iniciados, ele determinará se uma operação de restauração foi registrada; se uma operação de restauração tiver sido registrada, os serviços de certificados iniciarão a recuperação. Os serviços de certificados não processarão nenhuma solicitação de certificado até que a operação de recuperação seja concluída.

> [!Note]  
> Quando uma recuperação é concluída, é importante que você faça um novo backup completo do banco de dados dos serviços de certificados. Isso é necessário para truncar os arquivos de log restaurados e estabelecer um conjunto de backup básico para restaurações futuras. Os backups executados após uma restauração não podem ser misturados com backups (completos ou incrementais) feitos antes da restauração; ou seja, depois que um banco de dados de serviços de certificados for restaurado e progredido para um estado subsequente, você não poderá usar os backups de pré-restauração para restaurar o banco de dados para esse estado subsequente.

 

 

 
