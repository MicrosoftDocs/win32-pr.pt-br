---
title: Restaurando um servidor de Active Directory
description: Os servidores de Active Directory devem ser restaurados offline.
ms.assetid: 91fbbdc1-0e84-4b89-8a38-4c8d0268992b
ms.tgt_platform: multiple
keywords:
- Restaurando Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 865389b4ad80ad8c3009a86a881ff4cf291a4fc1b4606e78e8ecd01ceef7c893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184289"
---
# <a name="restoring-an-active-directory-server"></a>Restaurando um servidor de Active Directory

Os servidores de Active Directory devem ser restaurados offline. O sistema deve ser reiniciado no modo de restauração dos serviços de diretório. Nesse modo, o sistema operacional está sendo executado sem Active Directory Domain Services e toda a validação do usuário ocorre por meio do SAM (Gerenciador de contas de segurança) no registro. Para restaurar Active Directory Domain Services, use as credenciais de um administrador local no controlador de domínio que é restaurado.

o chamador das funções de restauração deve ter o privilégio de acesso de **ES \_ restore \_ NAME** . Use a função [**DsSetAuthIdentity**](dssetauthidentity.md) para definir o contexto de segurança no qual as funções de backup e restauração do diretório são chamadas.

Lembre-se de que, ao restaurar Active Directory Domain Services, você também deve restaurar os outros componentes de estado do sistema.

**Para restaurar Active Directory Domain Services**

1.  Chame a função [**DsIsNTDSOnline**](dsisntdsonline.md) para determinar se Active Directory Domain Services estão em execução.
2.  Se Active Directory Domain Services não estiverem em execução, a função [**DsRestorePrepare**](dsrestoreprepare.md) será chamada para inicializar a operação de restauração e obter um identificador de contexto de backup. Se Active Directory Domain Services estiver em execução, ele não poderá ser restaurado e o aplicativo de restauração deverá falhar na operação de restauração. A função **DsRestorePrepare** requer que o token de expiração seja obtido da função [**DsBackupPrepare**](dsbackupprepare.md) durante a operação de backup.
3.  Chame a função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) para determinar os diretórios em que os arquivos devem ser restaurados. Se essa função falhar, restaure os dados de volta para o diretório de origem de backup original; Esse é o diretório do qual foi feito o backup dos dados.
4.  Chame a função [**DsRestoreRegister**](dsrestoreregister.md) para preparar o servidor de Active Directory para a operação de restauração e bloquear os diretórios de restauração.
5.  Use as funções padrão do Win32 para restaurar os arquivos. Primeiro, exclua todos os arquivos no diretório de destino; em seguida, copie os arquivos de backup para o diretório de destino.
6.  Chame a função [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) para indicar que a restauração foi concluída.
7.  Chame a função [**DsRestoreEnd**](dsrestoreend.md) para liberar todos os recursos associados ao contexto.

Após uma restauração no modo de restauração dos serviços de diretório, o controlador de domínio deve ser reiniciado no modo normal. Quando o serviço de diretório for iniciado, o controlador de domínio executará a verificação de consistência normal e o diretório restaurado será online.

Lembre-se de que a restauração de um servidor de Active Directory é sempre uma operação de duas partes. Primeiro, restaure o banco de dados para uma hora em que o backup foi feito. Em segundo lugar, replique o diretório, em que o DSA restaurado recentemente Replica atualizações de pós-backup de outros DSAs no domínio e na floresta corporativa.

um computador que executa o Windows 2000 ou Windows Server 2003, que contém uma réplica do serviço de diretório, é um controlador de domínio.

A função [**DsRestoreRegister**](dsrestoreregister.md) adiciona dados ao registro que devem sobreviver ao processo de restauração do registro para que a restauração funcione corretamente. Para garantir que esses dados do registro sejam preservados, restaure Active Directory Domain Services com as funções **DsRestore \** _ antes de reiniciar o computador depois que a função [_ *RegReplaceKey* *](/windows/desktop/api/winreg/nf-winreg-regreplacekeya) for chamada. Esse processo funciona porque o **RegReplaceKey** , na verdade, não substitui o hive do registro até que o computador seja reiniciado e os dados do registro adicionados pela função **DsRestoreRegister** sejam especificamente excluídos de serem substituídos durante uma operação de restauração do registro.

 

 