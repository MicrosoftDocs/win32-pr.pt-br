---
title: TaskService. método de Conexão
description: Para scripts, o se conecta a um computador remoto e associa todas as chamadas subsequentes nessa interface a uma sessão remota.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- método de Conexão Agendador de Tarefas
- método de Conexão Agendador de Tarefas, objeto TaskService
- Agendador de Tarefas de objeto TaskService, Conexão método
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e8d9491fb66d8e79b18efed363d4eb4f21bc6c5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472342"
---
# <a name="taskserviceconnect-method"></a>TaskService. método de Conexão

Para scripts, o se conecta a um computador remoto e associa todas as chamadas subsequentes nessa interface a uma sessão remota. Se o parâmetro ServerName estiver vazio, esse método será executado no computador local. Se a userId não for especificada, o token atual será usado.

## <a name="syntax"></a>Sintaxe


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do Server* \[ em, opcional\]
</dt> <dd>

O nome do computador ao qual você deseja se conectar. Se o parâmetro ServerName estiver vazio, esse método será executado no computador local.

</dd> <dt>

*usuário* \[ do em, opcional\]
</dt> <dd>

O nome de usuário que é usado durante a conexão com o computador. Se o usuário não for especificado, o token atual será usado.

</dd> <dt>

*domínio* \[ do em, opcional\]
</dt> <dd>

O domínio do usuário especificado no parâmetro *User* .

</dd> <dt>

*senha* \[ do em, opcional\]
</dt> <dd>

A senha usada para se conectar ao computador. Se o nome de usuário e a senha não forem especificados, o token atual será usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

o método **TaskService. Conexão** deve ser chamado antes de chamar qualquer um dos outros métodos [**TaskService**](taskservice.md) .

se o método de Conexão falhar, você poderá coletar o identificador de erro para localizar o significado do erro. A tabela a seguir lista os identificadores de erro e suas descrições.




| Identificador de erro | Descrição | 
|------------------|-------------|
| 0x80070005 | Acesso negado para se conectar ao serviço de Agendador de Tarefas. | 
| 0x80041315 | O serviço de Agendador de Tarefas não está em execução. | 
| 0x8007000e | O aplicativo não tem memória suficiente para concluir a operação ou o <em>usuário</em>, a <em>senha</em>ou o <em>domínio</em> tem pelo menos um valor nulo e um não nulo. | 
| 53 | Esse erro é retornado nas seguintes situações:<ul><li>O nome do computador especificado no parâmetro <em>ServerName</em> não existe.</li><li>quando você está tentando se conectar a um computador Windows Server 2003 ou Windows XP, o computador remoto não tem a exceção de firewall de compartilhamento de arquivos e impressoras habilitada ou o serviço de registro remoto não está em execução.</li><li>quando você estiver tentando se conectar a um computador Windows Vista e o computador remoto não tiver a exceção de firewall de gerenciamento de tarefas agendadas remotas habilitada e a exceção de firewall de compartilhamento de arquivos e impressoras estiver habilitada ou o serviço de registro remoto não estiver em execução.</li></ul> | 
| 50 | os parâmetros de <em>usuário</em>, <em>senha</em>ou <em>domínio</em> não podem ser especificados ao se conectar a um computador remoto Windows XP ou Windows Server 2003 de um computador Windows Vista. | 




 

se você estiver se conectando a um computador remoto Windows vista de um Windows vista, será necessário permitir a exceção de firewall de gerenciamento de tarefas agendadas remotas no computador remoto. para permitir essa exceção, clique em iniciar, painel de controle, segurança, permitir um programa por meio de Windows Firewall e marque a caixa de seleção gerenciamento remoto de tarefas agendadas. em seguida, clique no botão Ok na caixa de diálogo Windows Firewall Configurações.

se você estiver se conectando a um computador remoto Windows XP ou Windows Server 2003 de um computador Windows Vista, será necessário permitir a exceção de firewall de compartilhamento de arquivos e impressoras no computador remoto. para permitir essa exceção, clique em iniciar, painel de controle, clique duas vezes em Windows Firewall, selecione a guia exceções e, em seguida, selecione a exceção de Firewall de compartilhamento de arquivos e impressoras. em seguida, clique no botão OK na caixa de diálogo Windows Firewall. O serviço registro remoto também deve estar em execução no computador remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





