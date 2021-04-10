---
title: Fazendo backup de um servidor de Active Directory
description: Um backup do Active Directory Server exige que você faça backup do banco de dados e dos logs de transação. Este tópico fornece uma explicação de como um aplicativo de backup faz backup do serviço de diretório Active Directory.
ms.assetid: 250b2f40-6d43-4aa5-a588-b0cd4839828d
ms.tgt_platform: multiple
keywords:
- fazendo backup Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5affde952ee543afe1bb9b794cce074a74382aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004819"
---
# <a name="backing-up-an-active-directory-server"></a>Fazendo backup de um servidor de Active Directory

Um backup do Active Directory Server exige que você faça backup do banco de dados e dos logs de transação. Este tópico fornece uma explicação de como um aplicativo de backup faz backup do serviço de diretório Active Directory.

O chamador dessas funções de backup deve ter o **privilégio \_ \_ nome de backup se** . Você pode usar a função [**DsSetAuthIdentity**](dssetauthidentity.md) para definir o contexto de segurança no qual as funções de backup/restauração do diretório são chamadas.

**Para fazer backup de um servidor de Active Directory, execute as seguintes etapas**

1.  Chame a função [**DsIsNTDSOnline**](dsisntdsonline.md) para determinar se Active Directory Domain Services estão em execução.
2.  Se Active Directory Domain Services estiver em execução, chame a função [**DsBackupPrepare**](dsbackupprepare.md) para inicializar um identificador de contexto de backup. Se Active Directory Domain Services não estiverem em execução, não será possível fazer backup dele e o aplicativo de backup deverá falhar na operação de backup.
3.  Chame a função [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) para obter uma lista de arquivos para fazer backup. Para liberar a memória retornada por essa função, chame a função [**DsBackupFree**](dsbackupfree.md) .
4.  Para cada nome na lista de arquivos retornada, chame a função [**DsBackupOpenFile**](dsbackupopenfile.md) seguida por chamadas repetidas para a função [**DsBackupRead**](dsbackupread.md) até que o arquivo inteiro tenha sido lido. Quando terminar de ler o arquivo, chame a função [**DsBackupClose**](dsbackupclose.md) para fechá-lo.
5.  Depois de fazer backup de todos os arquivos de banco de dados, chame a função [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) para obter uma lista de logs de transação. Essa lista é tratada da mesma forma que a lista de arquivos de banco de dados.
6.  Quando terminar de fazer backup do log de transações, chame a função [**DsBackupTruncateLogs**](dsbackuptruncatelogs.md) para excluir todos os logs de transações confirmados dos quais foi feito backup.
7.  Salve o conteúdo do token de expiração fornecido pela função [**DsBackupPrepare**](dsbackupprepare.md) . Isso pode ser salvo em um arquivo ou em alguma outra memória persistente. Esse token deve ser passado para a função [**DsRestorePrepare**](dsrestoreprepare.md) para iniciar uma operação de restauração.
8.  Libere a memória para o token de expiração passando o ponteiro de token para a função [**DsBackupFree**](dsbackupfree.md) .
9.  Por fim, chame a função [**DsBackupEnd**](dsbackupend.md) para liberar todos os recursos associados ao identificador de contexto de backup.

 

 




