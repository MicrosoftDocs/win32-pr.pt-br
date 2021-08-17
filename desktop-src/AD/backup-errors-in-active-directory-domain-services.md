---
title: Erros de backup no Active Directory Domain Services
description: Este tópico lista os valores de retorno de erro de backup para funções Active Directory Domain Services.
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Erros de backup do Active Directory
- Domínio do Active Directory de backup do serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5038b1d3a7a1f24c2e3b8dbf137aa2722073650b878e1d6a1dfdec8cac399a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024133"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Erros de backup no Active Directory Domain Services

Este tópico lista os valores de retorno de erro de backup para funções Active Directory Domain Services.



| Valor                                      | Descrição                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hrNyi**<br/>                       | A função não é implementada.<br/>                                                                                                                                                  |
| **hrInvalidParam**<br/>              | O parâmetro não é válido.<br/>                                                                                                                                                       |
| **hrError**<br/>                     | Ocorreu um erro interno.<br/>                                                                                                                                                       |
| **hrInvalidHandle**<br/>             | O handle não é válido.<br/>                                                                                                                                                          |
| **hrRestoreInProgress**<br/>         | O processo de restauração está em andamento.<br/>                                                                                                                                               |
| **hrAlreadyOpen**<br/>               | O arquivo especificado está aberto.<br/>                                                                                                                                                       |
| **hrInvalidRecips**<br/>             | Os destinatários não são válidos. <br/>                                                                                                                                                    |
| **hrCouldNotConnect**<br/>           | Não é possível fazer backup. Uma conexão com o servidor de backup especificado não foi detectada ou o serviço que você está tentando fazer backup não está em execução.<br/>                                       |
| **hrRestoreMapExists**<br/>          | Existe um mapa de restauração para o componente especificado. Um mapa de restauração pode ser especificado ao executar uma restauração completa.<br/>                                                                  |
| **hrIncrementalBackupDisabled**<br/> | Outro aplicativo modificou o banco de dados Windows NT/Windows 2000 Directory Service especificado, de forma que quaisquer backups subsequentes falharão. Para corrigir isso, execute um backup completo.<br/> |
| **hrLogFileNotFound**<br/>           | Não é possível executar um backup incremental porque não foi possível encontrar um arquivo de log Windows NT/Windows 2000 Directory Service.<br/>                                        |
| **hrCircularLogging**<br/>           | O Windows NT/Windows 2000 Directory Service especificado está configurado para usar logs de banco de dados circulares. Não é possível fazer backup incrementalmente. Executar um backup completo.<br/>       |
| **hrNoFullRestore**<br/>             | Os bancos de dados não foram restaurados neste computador. Não é possível restaurar um backup incremental até que um backup completo seja restaurado.<br/>                                            |
| **hrCommunicationError**<br/>        | Ocorreu um erro de comunicação ao tentar executar um backup local.<br/>                                                                                                       |
| **hrFullBackupNotTaken**<br/>        | Você deve executar um backup completo antes de executar um backup incremental.<br/>                                                                                                      |
| **hrMissingExpiryToken**<br/>        | O token de expiração está ausente. Não é possível restaurar sem os dados de expiração.<br/>                                                                                                                  |
| **hrUnknownExpiryTokenFormat**<br/>  | O token de expiração está em um formato irreconhecível.<br/>                                                                                                                                      |
| **hrContentsExpired**<br/>           | O conteúdo do DS no backup está desa datado. Restaurar com uma cópia recente.<br/>                                                                                                            |



 

## <a name="see-also"></a>Consulte Também

[Êxito,](success.md) [erros do sistema no Active Directory Domain Services](system-errors-in-active-directory-domain-services.md), erros do Gerenciador de [Diretórios,](directory-manager-errors.md)Erros de registro em log e recuperação em funções no [Active Directory Domain Services](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md), valores de retorno para funções [no Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)


 

 





