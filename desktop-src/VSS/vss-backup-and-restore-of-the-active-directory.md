---
description: O autor do Active Directory não requer nenhuma ação especial durante as operações de backup.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Backup e restauração do VSS do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8312e974d705cd193eaaecdaa163a2d408836aedfb14c21ff97f72486efbf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751479"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>Backup e restauração do VSS do Active Directory

O autor do Active Directory não requer nenhuma ação especial durante as operações de backup. O autor fornecerá ao solicitante informações de componente e conjunto de arquivos, e o solicitante usa essas informações para decidir quais arquivos copiar para a mídia de backup. Não é necessário usar nenhuma APIs especial para fazer o back-up do Active Directory.

A maneira como uma restauração é executada depende se o Active Directory é restaurado como parte de uma operação de recuperação de desastre ou se a restauração é para um sistema no qual o Active Directory está em execução. Além disso, a idade da cópia de backup do estado do Active Directory pode ser um problema devido a lápis do Active Directory.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Restauração do Active Directory após a recuperação de desastre

Após uma falha que exige recuperação de desastre, o Active Directory pode ser restaurado como parte da restauração do estado do sistema operacional.

Essa operação de restauração é essencialmente uma restauração sem writerless.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Restauração do Active Directory no sistema em que ele está em execução

O sistema deverá ser reinicializado no modo de Restauração dos Serviços de Diretório se o Active Directory estiver em execução no servidor.

O sistema operacional será executado sem o Active Directory e toda a validação do usuário ocorrerá por meio do SAM (Gerenciador de Contas de Segurança) no Registro. Somente o administrador tem permissão para recuperar o Active Directory.

Uma vez no modo de Restauração do Serviço de Diretório, uma restauração do VSS pode continuar normalmente. Não há motivo para usar APIs do Active Directory não VSS Win32 para restaurar o estado do Active Directory.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Restaurações do Active Directory e tombações do Active Directory

Qualquer plano de recuperação deve garantir que a idade do backup não exceda o tempo de vida da marca de lápis do Active Directory (o padrão é 60 dias).

A restauração de um backup mais antigo que a réplica fará com que um controlador de domínio tenha objetos que não são replicados para os outros servidores.

Os objetos que não são replicados não serão excluídos automaticamente nesse controlador de domínio (restaurado) porque as marcados de exclusão desses objetos nas outras réplicas já foram excluídas.

Um administrador terá que excluir manualmente cada um dos objetos no controlador de domínio restaurado que não são replicados. Não há suporte para backups incrementais do Active Directory; um backup completo é necessário.

 

 



