---
description: O gravador de Active Directory não requer ações especiais durante as operações de backup.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Backup e restauração do VSS do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501735"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>Backup e restauração do VSS do Active Directory

O gravador de Active Directory não requer ações especiais durante as operações de backup. O gravador fornecerá o solicitante com informações de componente e conjunto de arquivos, e o solicitante usará essas informações para decidir quais arquivos serão copiados para a mídia de backup. Não é necessário usar nenhuma API especial para fazer backup do Active Directory.

A forma como uma restauração é executada depende de o Active Directory ser restaurado como parte de uma operação de recuperação de desastre ou se a restauração é feita em um sistema no qual o Active Directory está em execução. Além disso, a idade da cópia de backup do estado de Active Directory pode ser um problema devido à Active Directory marcas de exclusão.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Restauração de Active Directory após a recuperação de desastre

Após uma falha exigindo a recuperação de desastre, o Active Directory pode ser restaurado como parte da restauração do estado do sistema operacional.

Essa operação de restauração é essencialmente uma restauração não-gravação.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Active Directory a restauração no sistema em que ele está em execução

O sistema deve ser reinicializado no modo de restauração dos serviços de diretório se o Active Directory estiver sendo executado no servidor.

O sistema operacional será executado sem o Active Directory, e toda a validação do usuário ocorrerá por meio do SAM (Gerenciador de contas de segurança) no registro. Somente o administrador tem permissão para recuperar o Active Directory.

Uma vez no modo de restauração do serviço de diretório, uma restauração do VSS pode continuar normalmente. Não há motivo para usar APIs de Active Directory do Win32 não VSS para restaurar o estado de Active Directory.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Active Directory restaura e Active Directory marcas para exclusão

Qualquer plano de recuperação deve garantir que a idade do backup não deve exceder o tempo de vida de Active Directory marca de exclusão (o padrão é 60 dias).

A restauração de um backup mais antigo que a marca para exclusão fará com que um controlador de domínio tenha objetos que não são replicados para os outros servidores.

Os objetos que não forem replicados não serão excluídos automaticamente nesse controlador de domínio (restaurado) porque as marcas para exclusão desses objetos em outras réplicas já foram excluídas.

Um administrador precisará excluir manualmente cada um dos objetos no controlador de domínio restaurado que não são replicados. Não há suporte para backups incrementais do Active Directory; um backup completo é necessário.

 

 



