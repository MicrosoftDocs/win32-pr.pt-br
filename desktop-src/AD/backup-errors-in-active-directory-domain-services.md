---
title: Erros de backup no Active Directory Domain Services
description: Este tópico lista os valores de retorno de erro de backup para funções no Active Directory Domain Services.
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Active Directory erros de backup
- Erros de backup do serviço de Domínio do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9b38ba9f28e47fd95e69a923e953d59fdd4d37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453478"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Erros de backup no Active Directory Domain Services

Este tópico lista os valores de retorno de erro de backup para funções no Active Directory Domain Services.



| Valor                                      | Descrição                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hrNyi**<br/>                       | A função não está implementada.<br/>                                                                                                                                                  |
| **hrInvalidParam**<br/>              | O parâmetro não é válido.<br/>                                                                                                                                                       |
| **hrError**<br/>                     | Ocorreu um erro interno.<br/>                                                                                                                                                       |
| **hrInvalidHandle**<br/>             | O identificador não é válido.<br/>                                                                                                                                                          |
| **hrRestoreInProgress**<br/>         | O processo de restauração está em andamento.<br/>                                                                                                                                               |
| **hrAlreadyOpen**<br/>               | O arquivo especificado está aberto.<br/>                                                                                                                                                       |
| **hrInvalidRecips**<br/>             | Os destinatários não são válidos. <br/>                                                                                                                                                    |
| **hrCouldNotConnect**<br/>           | Não é possível fazer backup. Não foi detectada uma conexão com o servidor de backup especificado ou o serviço que você está tentando fazer backup não está em execução.<br/>                                       |
| **hrRestoreMapExists**<br/>          | Existe um mapa de restauração para o componente especificado. Um mapa de restauração pode ser especificado ao executar uma restauração completa.<br/>                                                                  |
| **hrIncrementalBackupDisabled**<br/> | Outro aplicativo modificou o banco de dados do serviço de diretório do Windows NT/Windows 2000, de modo que os backups subsequentes falharão. Para corrigir isso, execute um backup completo.<br/> |
| **hrLogFileNotFound**<br/>           | Não é possível executar um backup incremental porque um arquivo de log do banco de dados do serviço de diretório do Windows NT/Windows 2000 não foi encontrado.<br/>                                        |
| **hrCircularLogging**<br/>           | O componente de serviço de diretório do Windows NT/Windows 2000 está configurado para usar logs de banco de dados circular. Não é possível fazer backup incremental. Execute um backup completo.<br/>       |
| **hrNoFullRestore**<br/>             | Os bancos de dados não foram restaurados neste computador. Você não pode restaurar um backup incremental até que um backup completo tenha sido restaurado.<br/>                                            |
| **hrCommunicationError**<br/>        | Ocorreu um erro de comunicação ao tentar executar um backup local.<br/>                                                                                                       |
| **hrFullBackupNotTaken**<br/>        | Você deve executar um backup completo para poder executar um backup incremental.<br/>                                                                                                      |
| **hrMissingExpiryToken**<br/>        | O token de expiração está ausente. Não é possível restaurar sem os dados de expiração.<br/>                                                                                                                  |
| **hrUnknownExpiryTokenFormat**<br/>  | O token de expiração está em um formato irreconhecível.<br/>                                                                                                                                      |
| **hrContentsExpired**<br/>           | O conteúdo do DS no backup está desatualizado. Restaure com uma cópia recente.<br/>                                                                                                            |



 

## <a name="see-also"></a>Consulte Também

[Êxito](success.md), [erros do sistema em Active Directory Domain Services](system-errors-in-active-directory-domain-services.md), [erros do Gerenciador de diretório](directory-manager-errors.md), erros de [log e recuperação em funções no Active Directory Domain Services](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md), [retornam valores para funções no Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)


 

 





